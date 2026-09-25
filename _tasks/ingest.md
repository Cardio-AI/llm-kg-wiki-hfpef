Purpose: read a source document and integrate it into the canonical wiki.
Outputs: `wiki/sources/`, plus updates to `wiki/concepts/`, `wiki/entities/`, and the registry files listed in step 9.

---

1. Read the full source document. "Source document" means a file the user has pointed to in `raw/`, or text/a document the user has pasted or attached directly in the conversation — if neither is available, ask the user for it rather than proceeding.
2. Analyze: key entities, concepts, core arguments, connections to existing wiki, contradictions. This analysis can stay as working notes (no separate file needed) — its purpose is to inform step 3's discussion.
3. **Discuss analysis with user before writing anything** — cover: key entities found, concepts updated, contradictions identified, gaps remaining. Proceed to step 4 once the user gives explicit go-ahead (e.g. "proceed," "looks good," "go ahead") or approves specific items; if the user requests changes, incorporate them before writing anything.
4. Zotero: read `_config/zotero.md` for credentials. Search Zotero by DOI or title. If not found, add it. Retrieve or generate citekey (`AuthorYearKeyword` — Keyword is one short word capturing the paper's topic, e.g. `Shah2022HFpEF`; if that citekey already exists for a different paper, disambiguate with a second word, e.g. `Shah2022HFpEFBiomarkers`). Citekey + DOI only in frontmatter/body — never the local `raw/` path (gitignored, local-only). Inline body citations use CLAUDE.md's `(source: citekey)` format.
5. Write pages:
   - `wiki/sources/<citekey>.md` — use `_templates/study.md` for clinical studies (RCTs, cohort studies, meta-analyses, registries, case series — anything reporting original clinical data), `_templates/source.md` for everything else (guidelines, scientific statements, reviews, mechanistic/basic-science papers)
   - Create/update concept pages in `wiki/concepts/` (see CLAUDE.md's entity-vs-concept definition and alias-resolution procedure before creating a new page)
   - Create/update entity pages in `wiki/entities/` (same check)
6. Link densely with `[[wiki-links]]`
7. When updating an existing page, migrate it to the current template structure if it still uses the old `## Content` format (a page with a single generic `## Content` heading instead of the template's named sections is the old format).
8. `## History` on concept pages requires ≥2 sources to be meaningful; if only one source exists, write what's known and mark `[expand as sources added]`
9. Update the full registry set — every ingest touches all of these, not a subset:
   - `wiki/index.md`, `wiki/log.md`, `wiki/overview.md`, `wiki/contradictions.md` (new tensions only), `wiki/timeline.md`
   - `wiki/citations.md` — new citekey row in the Ingested Sources table + its Full Formatted Reference entry
   - `wiki/tags-overview.md` — if the source's tags introduce any tag not already in this file, or change any existing tag's page count, update the relevant row(s)/add new row(s); this is the step most often forgotten — check it every time, not just when it feels like "a lot of new tags"
   - `wiki/trials.md` / `wiki/trials-pending.md` — if the source is a named clinical trial: either add a full row to `trials.md` (entity + source pages exist) or, if the trial is only named in passing (not itself being ingested), add/update its `trials-pending.md` entry
   - `wiki/sources-missing.md` — scan the source's own reference list (Source Interlinking Rule, CLAUDE.md) for on-topic papers that already have a wiki page (link bidirectionally via `Cites:`/`Cited by:` under `## Connections`) and for on-topic papers that don't (add a row here, not just an inline `[needs ingest]` note on the new page — this file is the single tracking location)

## Registry-only ingest (clipper pages, no results paper)

A clinicaltrials.gov/DRKS "clipper" page (a browser-saved registry page — recognisable by frontmatter fields `title`, `source` [the registry URL], `created` [the clip/access date]) is, by itself, enough to create the trial's **entity page**, even with no results paper in `raw/`:

- Create `wiki/entities/<trial-slug>.md` only — **no** `wiki/sources/` page (there is nothing to summarise yet).
- `sources:` frontmatter uses the trial's own NCT/DRKS ID as citekey, with `doi: null  # registry page only, no results published — see <url>`.
- Only what the registry page states goes in — sponsor, design, phase, eligibility, endpoints, enrolment. Never fill gaps from background knowledge.
- The trial is **not** added to `wiki/trials.md`. `trials.md` is reserved for trials with an actual results/design paper backing them. `trials-pending.md` tracks three groups for exactly this reason — read the registry's own status field and route accordingly:

**Group B — status active** (Recruiting, Active-not-recruiting, or Completed-but-unpublished): the ordinary case — an active trial, just no results paper yet.
- Body carries a `**Registration source:** <page title>, ClinicalTrials.gov/DRKS, <url>, accessed <clip's `created:` date>` line, and a prominent `## Status` note: "**No results published — needs ingest** once a primary results paper becomes available."
- Move the trial from `trials-pending.md` Group A to Group B (do **not** remove it from the file).

**Group C — status Unknown, Terminated, Withdrawn, or Suspended**: the registry itself cannot confirm the trial is still progressing — treat this as materially different from Group B, not a variant of it. A results paper may never appear.
- `## Status` states the actual status and its last-known-active date (e.g. "Unknown status (last known: Recruiting, 2024-03)"), not the ordinary "no results yet" phrasing.
- If the registry's stated dates/timeline conflict with any other source the user has supplied for the same trial (e.g. a spreadsheet), note the discrepancy as `[needs source]` — do not guess which is right.
- Move the trial from `trials-pending.md` Group A directly to Group C (never to Group B).

Either way: once a real results paper is later ingested, create the `wiki/sources/` page as normal, add the full row to `trials.md`, and **remove the trial from `trials-pending.md` entirely** — the registry-only entity page graduates into a normal fully-sourced page at that point (add the results citekey alongside the registry one in its `sources:` list). If a Group C trial's status is later re-confirmed as active before a results paper exists, move it to Group B instead.

**Never fabricate.** This applies to ingest as much as any other task (see CLAUDE.md's global no-fabrication rule) — do not fill in a specific fact (an NCT number, a numeric result, a population detail) from background/training knowledge just because the source document doesn't state it. Mark `[needs source]` and leave it for the user to supply instead.

One source touching 10–15 wiki pages has happened before and is not a red flag — it's not a target to hit, just an observation that dense cross-linking is expected.
