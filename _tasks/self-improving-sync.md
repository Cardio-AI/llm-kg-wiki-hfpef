Purpose: propagate canonical knowledge updates to derived artifacts.
Outputs: edits to the derived artifacts listed below, plus a log entry in `wiki/log.md`.

---
# Rules
When a canonical page (see CLAUDE.md Governance Terms) has a **substantive content change** — a claim, number, or conclusion changed, not just a `last_updated` bump or typo fix:
1. identify dependent pages, using the Dependency Sources below
2. identify which of those are now stale (see definition below)
3. update stale derived artifacts with a **targeted patch** of the affected section(s) only — do not regenerate the whole artifact from scratch, since that risks destroying unrelated content
4. update timestamps (`last_updated` in frontmatter)
5. log changes to `wiki/log.md`

**Staleness:** a derived artifact is stale when a canonical page it depends on (via a wikilink or its `derived_from` list) had a substantive content change since the artifact's own `last_updated`. Frontmatter-only edits to the canonical page do not trigger staleness.

---
# Dependency Sources
Use:
- `[[wiki-links]]` found in the derived artifact's body
- `derived_from:` frontmatter metadata — a list of citekeys and/or canonical-page file paths the artifact was built from (this field is used in `question-answering.md`'s Query Page Structure and should be populated the same way in `compare.md`/`summarize.md` outputs)

---
# Derived Artifacts
Possible stale artifacts:
- summaries (`wiki/summaries/`, see [[summarize]])
- comparisons (`wiki/comparisons/`, see [[compare]])
- queries (`wiki/queries/`, see [[question-answering]])
- html (`html/`, see [[html-generation]])

---
# Canonical Priority
Canonical wiki pages override derived artifacts.
Never propagate changes upstream from summaries/queries/html back into a canonical page — canonical pages are only updated directly, by the ingest task or a direct user-directed edit.
