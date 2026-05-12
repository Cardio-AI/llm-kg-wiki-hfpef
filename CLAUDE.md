# HFpEF Wiki
Personal knowledge base maintained by Claude. Based on Karpathy's LLM Wiki pattern.

**Scope:** Heart failure with preserved ejection fraction — physiology, clinical trials, interventions, AI/ML.  
**Division of labor:** Claude maintains and synthesizes. Human curates sources, asks questions, guides priorities.

## Folder Structure

```
_config/          integration configs (Zotero API credentials)
_templates/       page templates: source, study, concept, entity
inbox/            unprocessed notes — Claude helps triage
raw/              source documents — NEVER MODIFY

wiki/
  index.md        table of contents
  overview.md     high-level summary, active debates, gaps — updated on every ingest
  timeline.md     chronological evolution of HFpEF understanding — updated on every ingest
  log.md          append-only operations record
  contradictions.md  tensions between sources and pages
  sources/        one summary page per ingested document (named by citekey)
  entities/       named things: drugs, trials, biomarkers, guidelines, tools
  concepts/       mechanisms, relationships, diagnostic criteria
```

## Core Tasks

### Ingest
1. Read the full source document
2. Analyze: key entities, concepts, core arguments, connections to existing wiki, contradictions
3. **Discuss analysis with user before writing anything**
4. Zotero: read `_config/zotero.md` for credentials. Search Zotero by DOI or title. If not found, add it. Retrieve or generate citekey (`AuthorYearKeyword`).
5. Write pages:
   - `wiki/sources/<citekey>.md` — use `_templates/study.md` for clinical studies, `_templates/source.md` for all others
   - Create/update concept pages in `wiki/concepts/`
   - Create/update entity pages in `wiki/entities/`
6. Link densely with `[[wiki-links]]`
7. When updating an existing page, migrate it to the current template structure if it still uses the old `## Content` format
8. `## History` on concept pages requires ≥2 sources to be meaningful; if only one source exists, write what's known and mark `[expand as sources added]`
9. Update: `wiki/index.md`, `wiki/log.md`, `wiki/overview.md`, `wiki/contradictions.md`, `wiki/timeline.md`

One source may touch 10–15 wiki pages. That is normal.

### Question Answering
1. Read `wiki/index.md` to find relevant pages
2. Read those pages; synthesize answer with citations (`[[page]]`, `source: filename.pdf`)
3. For "how did thinking on X evolve?" — consult `wiki/timeline.md` and the `## History` sections on relevant concept pages; trace evidence chronologically
4. If not in wiki: say so clearly, offer to save an open-question note to `inbox/`
5. If the answer is valuable: offer to save it as a new wiki page

### Lint
Report as a numbered list with suggested fixes:
- Contradictions between pages
- Orphan pages (no inbound links)
- Concepts mentioned but lacking their own page
- Claims potentially outdated by newer sources
- Pages not matching their template format
- Redundant text: same table or paragraph appearing in ≥2 pages without a cross-reference; canonical home should be identified and others reduced to a cross-reference
- Missing citations: factual claims without `(source: …)` inline; mark `[needs source]` if not fixable
- Stub sources: pages with `[not yet ingested]` or `[Expand on paper ingest]` placeholders; list in missing-references report
- `wiki/citations.md` drift: citekeys appearing in wiki pages but missing from the citation registry

## Page Format & Naming
- **Files:** kebab-case (e.g. `diastolic-dysfunction.md`); source pages named by citekey (e.g. `Shah2022HFpEF.md`)
- **Templates:** `_templates/source.md` · `_templates/study.md` · `_templates/concept.md` · `_templates/entity.md`
- **Linking:** Every page ≥2 wiki-links; entities link to concepts; concepts link to entities and sources

## Citation
- Every factual claim inline: `(source: filename.pdf)`
- Two sources disagree: note on the page and in `wiki/contradictions.md`
- Unsourced claims: mark `[needs source]`
- Every page frontmatter must include:
```yaml
sources:
  - file: raw/filename.pdf
    citekey: AuthorYearKeyword   # e.g. Shah2022HFpEF
```
Citekeys are stable and Zotero-synced. Format: `AuthorYearKeyword`.

### Citation Lookup Rule
When the user asks "what is the source for X?", "give me the reference for Y", or asks for a citation by citekey:
1. Read `wiki/citations.md` to find the citekey
2. Return the full formatted reference from the **Full Formatted References** section
3. If the citekey is not in `wiki/citations.md`, say so and offer to add it

The canonical citation for any source is always the entry in `wiki/citations.md`, not the frontmatter of individual pages (which may be abbreviated).

## Writing Style
- Dense, precise, scientific — no padding
- Explicit about uncertainty and evidence quality
- Historical development: when a concept has evolved, trace prior → current understanding with dates in `## History` sections on concept pages, and update `wiki/timeline.md`
- Standard tags: `mechanism` · `trial` · `diagnosis` · `treatment` · `biomarker` · `imaging` · `guideline` · `ml-ai` · `open-question`

### Clinical Trials Overview Rule
Maintain `wiki/trials.md` as the master clinical trials registry and `wiki/trials-pending.md` as the staging list.

**On every ingest:** After processing a source, scan for clinical trial names that do not yet have entity or source pages in the wiki. For each such trial:
1. Add an entry to `wiki/trials-pending.md` with: full title, abbreviation, intervention, condition/LVEF threshold, study ID (NCT or equivalent), journal reference, which wiki source mentions it, and 1–4 descriptive sentences.

**When a new trial is added to the wiki** (entity + source pages created):
1. Add a row to the appropriate table in `wiki/trials.md`
2. Remove the entry from `wiki/trials-pending.md`
3. Update `wiki/index.md` and `wiki/log.md`

**`wiki/trials.md` required columns:** Abbreviation · Full Title · Intervention/Treatment · Condition (with LVEF threshold) · Study ID (NCT number) · Start · Completion · Wiki links

Mark NCT numbers not confirmed from an ingested PDF as `[verify on ingest]`.

## Rules
- Never modify `raw/`
- Always update `index.md` and `log.md` after any change
- Ask before categorizing anything uncertain
