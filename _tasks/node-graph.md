Purpose: generate a vector graphic (SVG) for any wiki node showing that node, its cross-referenced nodes, and the connections among those cross-references.

Output: `html/<node-name>-graph.svg`

---

# Rules
1. Source-of-truth is `wiki/` markdown — never modify it during this task
2. One SVG per node; re-running overwrites safely (idempotent)
3. Cross-references are `[[wikilinks]]` found anywhere in the target page body
4. Only show inter-ref edges that are explicitly confirmed by reading both pages — do not infer
5. If more than 20 cross-references exist, limit to the 20 most-linked (by appearance count in the source page) — apply this cutoff at the proposal stage (step 2/3), so the table the user confirms already matches what gets drawn; note the cutoff in the build comment

---

# Workflow

**This task is always interactive. Do not write the SVG until the user has confirmed the proposal in step 3.**

1. **Identify target node** — the file path is given (e.g. `wiki/entities/sglt2-inhibitors.md`). Derive `<node-name>` from the filename (strip directory and `.md`).

2. **Extract and analyse**:
   - Read the target page. Collect every unique `[[link-name]]` or `[[link-name|display]]`. Resolve each to its actual file path under `wiki/`. Record the display label (first `# Heading` in the linked file, or the link-name itself if the file does not exist).
   - For each resolved cross-reference page, read it and find which other cross-references it links to. Record only confirmed edges (both ends are in the cross-reference set).
   - Propose cluster groupings (up to 6 clusters, each with a short uppercase label). If the user already specified clusters in the message that invoked this task, use those instead of proposing new ones.
   - Propose a short descriptor for each inter-ref edge (e.g. "companion trial", "secondary analysis", "evidence base"). Keep descriptors ≤4 words. Descriptors are always proposed and always rendered (step 6) — there is no mode where they're turned off.

3. **Present proposal to user and wait for confirmation** — format as follows:

   **Cross-references** (table: display label | file | appearance count)

   **Inter-ref connections** (table: from | to | proposed descriptor)

   **Proposed clusters** (table: cluster label | members)

   Ask the user to confirm or request changes to: the cross-reference list, the connection descriptors, and the cluster assignments. Do not proceed until the user explicitly confirms.

4. **Apply user changes** — if the user edits any part of the proposal (removes nodes, renames clusters, changes descriptors, reassigns cluster members, or defines clusters from scratch), update the proposal accordingly. Re-present only the changed sections and ask for final confirmation.

5. **Compute layout**:
   - Canvas: 1500 × 1000 px
   - Central node: (750, 500)
   - Cross-ref ring radius: 320 px
   - Distribute nodes within each cluster at equal angular spacing; spread clusters around the ring so no two cluster centers are closer than 60°
   - For each node at polar angle θ, place label at radius + 60 px in the same radial direction; set `text-anchor` to `start` (right half, cos θ > 0.15), `end` (left half, cos θ < −0.15), or `middle` (top/bottom)
   - Split labels longer than 18 characters across two `<tspan>` lines

6. **Write SVG** with these layers (bottom to top):
   - White background rect
   - Cluster labels: font-size 9, fill `#d1d5db`, letter-spacing 1.5, uppercase
   - Inter-ref edges: `stroke="#cbd5e1"` width 1 opacity 0.6
   - Spoke edges (center → each cross-ref): `stroke="#475569"` width 1.5 opacity 0.35
   - Cross-ref circles: r 30, `fill="#f8fafc"` `stroke="#94a3b8"` stroke-width 1.5
   - Cross-ref labels: `fill="#94a3b8"` font-size 12
   - Central node circle: r 50, `fill="#1e3a5f"`
   - Central node label: `fill="#ffffff"` font-size 13 font-weight 700; split to two `<tspan>` lines if longer than 10 characters
   - Render each edge descriptor as a small label at the midpoint of its edge, `fill="#cbd5e1"` font-size 9, `text-anchor="middle"`, behind node circles

7. **No external dependencies** — pure SVG, no JavaScript, no CDN. All coordinates pre-computed.
