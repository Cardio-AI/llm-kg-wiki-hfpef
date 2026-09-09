Purpose: generate a graph visualization for any wiki node showing that node, its cross-referenced nodes, and the connections among those cross-references.

Output: `html/<node-name>-graph.svg` and `html/<node-name>-graph.html` (interactive), written together by default from one invocation, unless the triggering message asks for SVG only.

---

# Invocation parameters

All optional, stated in the message that triggers the task. Unspecified parameters use the defaults below.

| Parameter | Values | Default | Meaning |
|---|---|---|---|
| `mode` | `ego` \| `connected` | `ego` | `ego` = 1-hop neighborhood of the target node (original behavior). `connected` = multi-hop traversal outward from the target node. |
| `depth` | integer | `3` | Max hops to traverse. Only meaningful in `connected` mode. |
| `min-degree` | integer | none (no filtering) | Drop nodes whose connection count is below this, before layout. |
| `degree-scope` | `global` \| `local` | `global` | What `min-degree` counts against — see Threshold filtering below. |

---

# Rules
1. Source-of-truth is `wiki/` markdown — never modify it during this task
2. One SVG + one HTML per node per invocation; re-running overwrites safely (idempotent)
3. Cross-references are `[[wikilinks]]` found anywhere in the target page body
4. Only show inter-ref edges that are explicitly confirmed by reading both pages — do not infer
5. **Size cutoffs, split by mode, always applied at the proposal stage (step 2/3) so the table the user confirms already matches what gets drawn — never truncate silently after confirmation:**
   - `ego` mode: if more than 20 cross-references exist, limit to the 20 most-linked (by appearance count in the source page). Note the cutoff in the proposal and the build comment.
   - `connected` mode: after depth traversal and any `min-degree` filtering, if the candidate set exceeds 150 nodes, truncate by BFS order (nodes closer to the origin are kept first). Note the cutoff in the proposal and the build comment.
6. `connected` mode traverses `[[wikilinks]]` in both directions (the origin page's own outbound links, and pages elsewhere in the wiki that link to it) — treat the wiki graph as undirected for reachability. The goal is everything related to the topic, not just what the origin page happens to cite.
7. No external dependencies in either output — pure SVG / vanilla JS only, no CDN, no framework. All SVG coordinates pre-computed, matching the existing `html-generation.md` "no external CDN" convention.

---

# Threshold filtering (`min-degree`)

Applied after the candidate node set is built (ego cross-refs, or the connected-mode BFS result) and before the final size cutoff in Rule 5. The origin/target node is always exempt from the threshold, regardless of its own degree.

- **`degree-scope: global`** (default) — degree = count of distinct other pages anywhere under `wiki/` with a confirmed `[[link]]` to or from this page. Compute by scanning `wiki/**/*.md` for wikilinks referencing the page, and the page's own outbound links. If `graph/relations.json` exists and looks current, it may be used as a shortcut for this count — never depend on it being present, since `graph/` is gitignored and only regenerated on demand by `html-generation`.
- **`degree-scope: local`** — degree = count of edges connecting this node to other nodes already in this specific drawing's candidate set (i.e. degree within the subgraph being built, not the whole wiki).

---

# Workflow

**This task is always interactive. Do not write any output file until the user has confirmed the proposal in step 3.**

1. **Identify target node** — the file path is given (e.g. `wiki/entities/sglt2-inhibitors.md`). Derive `<node-name>` from the filename (strip directory and `.md`).

2. **Extract and analyse**:
   - **`ego` mode**: Read the target page. Collect every unique `[[link-name]]` or `[[link-name|display]]`. Resolve each to its actual file path under `wiki/`. Record the display label (first `# Heading` in the linked file, or the link-name itself if the file does not exist).
   - **`connected` mode**: BFS outward from the target page following wikilinks in both directions (Rule 6), up to `depth` hops. Record each discovered node's hop distance from the origin (the smallest hop count at which it was reached, if reachable by multiple paths).
   - Apply `min-degree` filtering (see above) if requested, then the Rule 5 size cutoff for the mode in use.
   - For each resolved node in the final candidate set, read it and find which other candidate-set nodes it links to. Record only confirmed edges (both ends are in the set) — this covers both spoke edges (origin to each direct neighbor) and inter-ref edges (between non-origin nodes).
   - For every edge (spoke and inter-ref alike):
     - Propose a short descriptor (e.g. "companion trial", "secondary analysis", "evidence base"), ≤4 words. Always proposed, always rendered — there is no mode where descriptors are turned off.
     - In `connected` mode, record the edge's hop distance from the origin (the hop count of its farther endpoint).
     - Classify one evidence-relation tag from this fixed vocabulary:
       - `contradicts` — both endpoint pages are named together in the same numbered entry in `wiki/contradictions.md`. This is a lookup against that file, not a judgment call.
       - `strongly-supports` — endpoints share a citekey in their `sources:` frontmatter, or one page's summary directly corroborates a specific claim made on the other.
       - `partially-supports` — topically or mechanistically related, directionally consistent, but not directly corroborating (e.g. same drug class, adjacent mechanism, related but distinct endpoints).
       - `neutral` — structural or topical link only, no explicit evidentiary relationship between the two pages. This is the fallback and matches the pre-existing default rendering.
   - Propose cluster groupings (up to 6 clusters, each with a short uppercase label). If the user already specified clusters in the message that invoked this task, use those instead of proposing new ones.

3. **Present proposal to user and wait for confirmation** — format as follows:

   **Nodes** (table: display label | file | hop-distance [connected mode only] | degree [only if `min-degree` requested] | included/dropped-by-threshold)

   **Edges** (table: from | to | descriptor | hop-distance [connected mode only] | evidence tag)

   **Proposed clusters** (table: cluster label | members)

   Note any Rule 5 truncation explicitly (which nodes were cut and why).

   Ask the user to confirm or request changes to: the node list, the connection descriptors, the evidence-relation tags, and the cluster assignments. Do not proceed until the user explicitly confirms.

4. **Apply user changes** — if the user edits any part of the proposal (removes nodes, renames clusters, changes descriptors, reclassifies an evidence tag, reassigns cluster members, or defines clusters from scratch), update the proposal accordingly. Re-present only the changed sections and ask for final confirmation.

5. **Compute layout**:
   - Canvas: 1500 × 1000 px
   - Central node: (750, 500)
   - Cross-ref ring radius: 320 px. In `connected` mode, place each additional hop tier on its own ring: hop 1 at 320px, hop 2 at 470px, hop 3+ at 620px.
   - Distribute nodes within each cluster (and, in `connected` mode, within each hop ring) at equal angular spacing; spread clusters around the ring so no two cluster centers are closer than 60°
   - For each node at polar angle θ, place label at radius + 60 px in the same radial direction; set `text-anchor` to `start` (right half, cos θ > 0.15), `end` (left half, cos θ < −0.15), or `middle` (top/bottom)
   - Split labels longer than 18 characters across two `<tspan>` lines
   - This layout is computed once and shared verbatim between the SVG and HTML renderers in steps 6 and 7, so the two outputs stay visually consistent.

6. **Write SVG** (`html/<node-name>-graph.svg`) with these layers (bottom to top):
   - White background rect
   - Cluster labels: font-size 9, fill `#d1d5db`, letter-spacing 1.5, uppercase
   - Edges, styled by the two independent channels below, drawn behind node circles
   - Cross-ref circles: r 30, `fill="#f8fafc"` `stroke="#94a3b8"` stroke-width 1.5
   - Cross-ref labels: `fill="#94a3b8"` font-size 12
   - Central node circle: r 50, `fill="#1e3a5f"`
   - Central node label: `fill="#ffffff"` font-size 13 font-weight 700; split to two `<tspan>` lines if longer than 10 characters
   - Edge descriptor label at the midpoint of each edge, `fill="#cbd5e1"` font-size 9, `text-anchor="middle"`, behind node circles
   - Legend block in a canvas corner decoding both edge channels below

   **Edge channel 1 — width/opacity by hop distance** (`ego` mode: all edges are hop 1, so this channel is constant, matching prior behavior):
   - Hop 1: width 2.5, opacity 0.6
   - Hop 2: width 1.5, opacity 0.45
   - Hop 3+: width 0.75, opacity 0.3

   **Edge channel 2 — color/style by evidence tag** (independent of channel 1; combine both on every edge):
   - `contradicts`: `stroke="#dc2626"`, dashed (`stroke-dasharray="4 3"`)
   - `strongly-supports`: `stroke="#16a34a"`, solid
   - `partially-supports`: `stroke="#475569"`, solid — this and the next tag are the pre-existing default colors, so untagged/default-tier edges render exactly as before
   - `neutral`: `stroke="#cbd5e1"`, solid

7. **Write interactive HTML** (`html/<node-name>-graph.html`), single self-contained file:
   - Inline `<svg>` using the identical coordinates and edge styling from steps 5 and 6 (same visual result as the SVG file, embedded directly in the page rather than referenced).
   - Inline `<style>` and inline vanilla `<script>` — no external CDN, no framework (Rule 7).
   - Per-node data embedded as a `<script type="application/json" id="node-data">` block: `{file, label, summary, tags, entity_type_or_page_type, html_link}`. `summary` is the page's frontmatter/blockquote summary. `html_link` is the relative path to `html/<path>/index.html` if that compiled file exists on disk at build time; omit the key entirely if it doesn't (best-effort — do not produce a dead link, and do not treat a missing compiled site as an error for this task).
   - No `fetch()` or network calls of any kind — everything needed is inline, so the file works opened directly via `file://` with no server.
   - Click behavior: clicking a node circle opens a plain absolutely-positioned popup (vanilla JS, no library) showing that node's label, summary, tags, and a "Read full page" link when `html_link` is present. Clicking outside the popup or pressing Escape closes it.
   - Fixed legend panel decoding both edge channels (hop-distance widths, evidence-tag colors), same content as the SVG legend.
