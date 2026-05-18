# HFpEF Wiki
Personal ontology-aware knowledge base maintained by Claude. Based on Karpathy's LLM Wiki pattern.

**Scope:** Heart failure with preserved ejection fraction — physiology, clinical trials, interventions, AI/ML.  
**Division of labor:** Claude maintains and synthesizes. Human curates sources, asks questions, guides priorities.

**Purpose:**
- canonical medical knowledge graph
- semantic retrieval system
- evolving research memory
- static HTML publishing pipeline
- agent-readable + human-readable knowledge base

---

## Core Principles
1. One concept = one canonical page
2. Aliases normalize semantic duplicates
3. Markdown in `/wiki` is source-of-truth
4. HTML/graph artifacts are compiled outputs
5. Every derived artifact tracks provenance
6. Changes propagate to dependent artifacts

## Folder Structure

```
_config/          integration configs (Zotero API credentials)
_tasks/           executable task instructions
_templates/       page templates: source, study, concept, entity

inbox/            unprocessed notes — Claude helps triage
raw/              source documents — NEVER MODIFY

wiki/
	citations.md
	contradictions.md  tensions between sources and pages
	index.md           table of contents
	log.md             append-only operations record
	overview.md        high-level summary, active debates, gaps — updated on every ingest
	timeline.md        chronological evolution of HFpEF understanding — updated on every ingest
	trials.md          list of all trials known
	trials-pending.md  list of trials not yet ingested

	sources/        one summary page per ingested document (named by citekey)
	entities/       named things: drugs, trials, biomarkers, guidelines, tools
	concepts/       mechanisms, relationships, diagnostic criteria
	queries/
	summaries/
	comparisons/

graph/
	entities.json
	aliases.json
	relations.json
	derivations.json

html/
```

## Core Tasks

- [[ingest]] — read a PDF, update wiki pages, propagate to registry files
- [[question-answering]] — answer questions from canonical wiki; save as query pages
- [[summarize]] — synthesize one topic/source into `wiki/summaries/`
- [[compare]] — side-by-side analysis of trials/guidelines → `wiki/comparisons/`
- [[html-generation]] — compile `wiki/` markdown → `html/` site + `graph/` JSON artifacts
- [[self-improving-sync]] — propagate canonical page changes to derived artifacts
- [[lint]] — audit wiki for broken links, missing citations, stale content

## Page Format & Naming
- **Files:** kebab-case (e.g. `diastolic-dysfunction.md`); source pages named by citekey (e.g. `Shah2022HFpEF.md`)
- **Templates:** `_templates/source.md` · `_templates/study.md` · `_templates/concept.md` · `_templates/entity.md`
- **Linking:** Every page ≥2 wiki-links; entities link to concepts; concepts link to entities and sources

## Canonical Entity Rule

**One concept = one canonical page.** Aliases, abbreviations, IDs, and alternate names must converge to one entity.

**Before creating any page:** Search existing pages for semantic overlap (abbreviations, alternate spellings, synonyms). If overlap >85%: update the existing page + add alias — do NOT create a new page. Never create: duplicate semantic entities · abbreviation-only duplicates · capitalization or pluralization variants · renamed-trial duplicates.

Always resolve aliases BEFORE creating pages, graph edges, summaries, or HTML artifacts.

**Aliases block** — required on every entity and concept page, immediately after the summary blockquote:

```
## Aliases
| Alias | Type | Notes |
|---|---|---|
| ATTR-CM | abbreviation | common clinical shorthand |
| TTR cardiomyopathy | alternate-name | older terminology |
| NCT000123456 | Trial-ID | registered on clinicaltrials.gov |
```

Alias types: `abbreviation` · `acronym` · `old-name` · `slang` · `research-name` · `misspelling` · `Trial-ID`

**Canonical naming:** Prefer descriptive filenames (e.g. `transthyretin-amyloid-cardiomyopathy.md`) except where the abbreviation is universal clinical standard (e.g. `sglt2-inhibitors.md`). Abbreviations go in the Aliases block.

## Citation & Evidence

- Every factual claim inline: `(source: filename.pdf)`
- Two sources disagree: note on the page and in `wiki/contradictions.md`; contradiction must propagate to concept pages, summaries, comparisons, and queries
- Unsourced claims: mark `[needs source]`
- Every page frontmatter:
```yaml
sources:
  - file: raw/filename.pdf
    citekey: AuthorYearKeyword   # e.g. Shah2022HFpEF
```
Citekeys are stable and Zotero-synced. Format: `AuthorYearKeyword`.

**Citation lookup:** When asked for a reference or citekey — read `wiki/citations.md`, return the full APA entry from **Full Formatted References**. If missing, say so and offer to add it. Canonical citation is always `citations.md`, not page frontmatter.

## Writing Style
- Dense, precise, scientific — no padding
- Explicit about uncertainty and evidence quality
- Historical development: trace prior → current understanding with dates in `## History` sections; update `wiki/timeline.md`
- Standard tags: `mechanism` · `trial` · `diagnosis` · `treatment` · `biomarker` · `imaging` · `guideline` · `ml-ai` · `open-question`

## Clinical Trials Rule

Maintain `wiki/trials.md` (master registry) and `wiki/trials-pending.md` (staging).

**On every ingest:** Scan for trial names without wiki pages. For each: add to `wiki/trials-pending.md` with full title, abbreviation, intervention, population/LVEF threshold, NCT number, source citekey, and 1–4 sentences.

**When a trial gets entity + source pages:** move it from `trials-pending.md` to `trials.md`. Required columns: Abbreviation · Full Title · Intervention · Condition (LVEF threshold) · NCT · Start · Completion · Wiki links. Mark unconfirmed NCT numbers `[verify on ingest]`.

## Rules
- Never modify `raw/`
- Always update `index.md` and `log.md` after any change
- Ask before categorizing anything uncertain
