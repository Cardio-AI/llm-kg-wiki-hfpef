Purpose: audit the wiki for broken links, missing citations, and stale/inconsistent content.
Outputs: report appended to `wiki/log.md` (same convention as the build report in `_tasks/html-generation.md`).

---

This task is **diagnostic and report-only** — it identifies and reports issues with suggested fixes; it does not apply fixes itself (a separate ingest/edit pass does that, using the lint report as its punch list).

Report as a single combined numbered list — one list covering all categories below, not one list per category — each entry tagged with its category and a suggested fix:
- Contradictions between pages — classify each as one of: different population/scope · different measurement method · genuine dispute · superseding source. **Never silently resolve a contradiction by blending, averaging, or picking one claim over the other** — flag it, don't merge it away.
- Orphan pages (no inbound `[[wikilink]]`s pointing to them)
- Concepts mentioned but lacking their own page
- Claims potentially outdated by newer sources already in the wiki (a newer ingested source contradicts or supersedes an older claim — this does not mean searching outside the wiki for new literature)
- Pages not matching their template format (missing required sections from `_templates/*.md`, or missing `page-type`/`Aliases`/`References` per CLAUDE.md)
- Redundant text: same table or paragraph appearing in ≥2 pages without a cross-reference; report which page should be the canonical home and which others should be reduced to a cross-reference (report only — the actual edit happens in a follow-up pass)
- Missing citations: factual claims without `(source: citekey)` inline (same format `ingest.md` uses for body citations); mark `[needs source]` if not fixable
- Stub sources: pages with `[not yet ingested]` or `[Expand on paper ingest]` placeholders; list separately as a missing-references report within the same `wiki/log.md` entry
- `wiki/citations.md` drift: citekeys appearing in wiki pages but missing from the citation registry
