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

## Governance Terms

Recurring terms used across every task file — defined once here, not restated per task.

- **Canonical page:** the single authoritative wiki page for a topic — a page in `wiki/concepts/`, `wiki/entities/`, or `wiki/sources/`. Everything in `wiki/summaries/`, `wiki/comparisons/`, `wiki/queries/`, and `html/` is a *derived artifact* — never canonical, always subordinate to the canonical page(s) it was built from (see [[self-improving-sync]]).
- **Entity vs. concept:** an **entity** is a discrete, individually named thing — a drug, trial, guideline, biomarker/score, comorbidity, institution, or a named disease phenotype treated as an object (e.g. `hfpef.md` is an entity page, since HFpEF is the named phenotype itself). A **concept** is a mechanism, process, relationship, or diagnostic framework that isn't one discrete named thing (e.g. `diastolic-dysfunction.md` is a concept/mechanism page — it describes a process, not a named object). When unsure, ask: "is this a *thing* or a *process/relationship*?"
- **Alias resolution (the actual search procedure behind the Canonical Entity Rule below):** before creating any new page, search existing `wiki/entities/` and `wiki/concepts/` page titles and `## Aliases` tables for the term — including abbreviations, alternate spellings, and old names. If a ≥85% semantic-overlap match exists, update that page and add an alias row; do not create a new page.

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
- [[node-graph]] — generate SVG cross-reference graph for any wiki node → `html/<node-name>-graph.svg`
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

- Every factual claim inline: `(source: citekey)` — never a raw filename or path (`raw/` is gitignored and not part of the public repo)
- Two sources disagree: note on the page and in `wiki/contradictions.md`; contradiction must propagate to concept pages, summaries, comparisons, and queries
- Unsourced claims: mark `[needs source]` in body prose. This applies to *every* task (ingest, question-answering, summarize, compare, lint) — grounding discipline is global, not specific to any one task.

**What needs a citation vs. what doesn't** — never fabricate, and never fill a gap from background/training knowledge even when confident it's correct. But not every sentence is a "fact claim" requiring a citekey. Three tiers:

1. **OK to state without a wiki citation** — logical/definitional relations and broad, textbook-level ontological scaffolding that isn't specific to this wiki's evidence base:
   - `"is"` establishing a logical/identity relation (e.g. "cardiac muscle" is another word for "myocardium")
   - grammatical/etymological facts ("atrial" is the adjective of the anatomical "atrium"; plural "atria")
   - generic definitional statements that could apply to any textbook ("a cardiac disease is a condition that affects the heart"; "a heart valve is a structure that regulates blood flow between chambers")
2. **Borderline — needs a wiki mention/link, not a full citation** — statements that define a wiki-specific category or frame a concept in terms of this wiki's subject matter, e.g. "HFpEF is a type of heart failure often characterized by diastolic dysfunction." Link to the canonical page ([[hfpef]], [[diastolic-dysfunction]]) rather than treating it as bare background knowledge.
3. **NOT OK without an explicit `(source: citekey)`** — any specific biomedical fact: an association, anatomy fact, mechanism, treatment, biomarker, or trial result. E.g. "hypertension can contribute to heart failure," "diastolic dysfunction can lead to elevated filling pressures," "obesity is a risk factor for HFpEF," "SGLT2 inhibitors are used for HFpEF." If the wiki doesn't cover it, mark `[needs source]` or `[not covered in wiki — needs ingest]` — do not answer from memory even if the fact is well-established medically.

`[needs source]` syntax: bare `[needs source]` inline in body prose for an unsourced claim; `doi: null  # needs source — see wiki/citations-doi-review.md` in frontmatter when a citekey exists but its DOI hasn't been verified. `wiki/citations-doi-review.md` tracks all pending DOI verifications — check it before marking a new DOI gap.

- Every page frontmatter:
```yaml
sources:
  - citekey: AuthorYearKeyword   # e.g. Shah2022HFpEF
    doi: 10.xxxx/xxxxx           # or null if unverified — see wiki/citations-doi-review.md
```
Citekeys are stable and Zotero-synced. Format: `AuthorYearKeyword`.

**Non-source pages** (concepts/entities/comparisons/summaries/queries/index/overview/contradictions/trials-pending) must end with a `## References` section listing the full formatted DOI reference (pulled from `wiki/citations.md` → Full Formatted References) for every citekey cited on that page.

**Source pages** (`wiki/sources/*.md`) replace the old `**File:** raw/...` line with a `**Full citation:**` line followed by the same formatted-reference text.

**Citation lookup:** When asked for a reference or citekey — read `wiki/citations.md`, return the full APA entry from **Full Formatted References**. If missing, say so and offer to add it. Canonical citation is always `citations.md`, not page frontmatter.

## Writing Style
- Dense, precise, scientific — no padding
- Explicit about uncertainty and evidence quality
- Historical development: trace prior → current understanding with dates in `## History` sections; update `wiki/timeline.md`
- Standard tags: `mechanism` · `trial` · `diagnosis` · `treatment` · `biomarker` · `imaging` · `guideline` · `ml-ai` · `open-question`

## Page Type Taxonomy

**Each markdown file in `wiki/` must have exactly one page-type tag in frontmatter:**
- `source-summary-page` — ingested source document summary (named by citekey)
- `concept-page` — mechanistic or physiological concept, relationships
- `entity-page` — named thing (drug, trial, biomarker, guideline, tool)
- `mechanism-page` — molecular or cellular mechanism (subset of concept; use when mechanism warrants standalone depth)
- `phenotype-page` — patient or disease phenotype (e.g. HFpEF subtypes, patient cohorts)

**Frontmatter example:**
```yaml
page-type: entity-page
```

Meta pages (`type: meta` — registry/tracking files like `trials.md`, `trials-pending.md`, `sources-missing.md`, `candidate-pages-review.md`), comparisons, queries, and index pages (index.md, overview.md, etc.) are exempt. Tag audit via lint task.

**`entity_type` (entity pages only, separate field from `page-type`):** narrows what kind of thing an entity page describes. Values in active use: `trial` · `drug` · `guideline` · `comorbidity` · `disease` · `study` · `imaging-tool` · `diagnostic-tool` · `phenotype` · `registry` · `score` · `treatment-approach` · `intervention`. Also reserved for future use (declared, not yet assigned to any page): `biomarker` · `institution`. Pick the closest match; propose a new value only if none of these fit.

## Clinical Trials Rule

Maintain `wiki/trials.md` (master registry) and `wiki/trials-pending.md` (staging).

**On every ingest:** Scan for trial names without wiki pages. For each: add to `wiki/trials-pending.md` with full title, abbreviation, intervention, population/LVEF threshold, NCT number, source citekey, and 1–4 sentences.

**When a trial gets entity + source pages:** move it from `trials-pending.md` to `trials.md`. Required columns: Abbreviation · Full Title · Intervention · Condition (LVEF threshold) · NCT · Start · Completion · Wiki links. Mark unconfirmed NCT numbers `[verify on ingest]`.

## Rules
- Never modify `raw/`
- `raw/` is gitignored — never re-add PDFs to git; ingest still reads/writes local `raw/` files, but citekey + DOI is the only thing that reaches committed wiki pages
- Always update `index.md` and `log.md` after any change
- Ask before categorizing anything uncertain
- **Never fabricate, in any task.** The Citation & Evidence sourcing taxonomy above is a global rule, not specific to question-answering — it governs ingest, summarize, compare, and lint equally. Do not fill a specific fact (an NCT number, a numeric result, a mechanism claim) from background/training knowledge during ingest either; mark `[needs source]` and leave it for the user to supply instead.
