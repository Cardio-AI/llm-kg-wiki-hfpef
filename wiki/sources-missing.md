---
type: meta
title: Missing Source Pages — Standalone Papers Referenced Without a Page
summary: Citekeys/papers named in wiki prose (History sections, background mentions, "as shown by X et al...") that have no wiki/sources/ page and aren't a trial/study captured elsewhere. Not auto-created — for manual review.
tags:
  - meta
  - pending
  - sources
created: 2026-07-14
last_updated: 2026-07-15
---
# Missing Source Pages

> Scope: this file catches standalone papers named in wiki prose that aren't (a) a named clinical trial with its own entity-page candidate (see `wiki/candidate-pages-review.md` — trials like SERVE-HF, GUIDE-HF get a full entity page, not a bare source stub here), (b) a component study sitting inside an already-ingested meta-analysis's own reference list (that's `wiki/sources-pending-from-meta-analyses.md`'s job), or (c) already tracked in `wiki/trials-pending.md`.

**Registry cross-check confirmed near-zero true gaps at the citekey level**: all 155 citekeys in `wiki/citations.md` have a corresponding `wiki/sources/` page (5 apparent mismatches were duplicate citekey rows for the same paper, not real gaps — e.g. `d'amario2019cmd` ≡ `damario2019cmd.md`). Two corrections to the discovery pass's own findings: **PARAMOUNT** (`solomon2012paramount.md`) and **HEART Camp** (`alonso2022heartcamp.md`) both already have source pages — they were false positives from agents that hadn't seen the full source-page list. **Update 2026-07-15:** both now also have entity pages (`paramount-trial.md`, `heart-camp.md`) and full `trials.md` rows — fully resolved, not just source-page-only anymore.

**Known Stub Sources** (already tracked in `wiki/citations.md`, not a fresh gap): `Armstrong2020VICTORIA`, `Cleland2006PEPCHF` — HFrEF-context or no-PDF-obtained stubs, see `wiki/citations.md` → Stub Sources.

---

## Standalone papers worth considering for individual ingest

| Paper (as named in prose) | Mentioned in | Context | Priority |
|---|---|---|---|
| McMurray et al., JACC 2023 | paraglide-hf.md | Primary PARAGLIDE-HF results paper (NT-proBNP ratio of change 0.85, 95% CI 0.73–0.999) — only the design paper (mentz2023paraglide) and secondary analyses (fudim2024paraglide, nouhravesh2025paraglide, rambarat2025paraglide) are currently ingested, not the primary results paper itself | Medium-high — primary trial-results gap, found during 2026-09-17 citation-coverage lint pass |
| Selker et al. 2019 | zeid2025myomobile.md | Methodological source for the "EE2" efficacy/effectiveness trial design used by MyoMobile | Low — methodology reference, not a clinical outcome |
| Peterson et al. (GWTG-HF risk score derivation) | boralkar2019nlr.md | GWTG-HF risk score calculation method | Low — score-derivation paper, score itself already used elsewhere |
| Bermea 2024 (ML-derived HFpEF screening score) | achten2025screening.md | Compared against HFpEF-ABA score; "not validated broadly, proof-of-concept only" | Low |
| EDIFY trial (ivabradine) | anker2023hfpefphenotype.md | Negative trial for chronotropic incompetence — **`wiki/concepts/chronotropic-incompetence.md` now exists (created 2026-07-15)**, so ingesting this would directly enrich a live page rather than a hypothetical candidate | Medium-high (upgraded) |
| myPACE RCT (personalized accelerated pacing) | anker2023hfpefphenotype.md | Positive trial for chronotropic incompetence — same upgraded relevance as EDIFY | Medium-high (upgraded) |
| PICNIC trial (nutritional supplementation, hospitalised HF) | bohmke2022nonpharm.md | HR 0.45 for composite clinical endpoint | Low-medium |
| EFFORT trial (nutritional intervention) | bohmke2022nonpharm.md | HF subgroup adjusted OR 0.44 for 30-day mortality | Low-medium |
| SODIUM-HF (NCT02012179) | bohmke2022nonpharm.md | N=806 sodium-restriction trial, neutral primary composite | Low-medium |
| STOP-HF trial | mahmood2024guidelines.md | BNP-guided general-practice management, reduced CV outcomes | Low-medium |
| PONTIAC trial | mahmood2024guidelines.md | NT-proBNP screening in diabetics, reduced CV outcomes | Low-medium |
| BATTLESCARRED, TIME-CHF, GUIDE-IT | horiuchi2022npguided.md | NP-guided therapy trials (HFrEF-predominant populations); age-stratified effect (BATTLESCARRED) | Low — mostly HFrEF context |
| DIAST-CHF | morfino2022biomarkers.md | sST2 prognostic value substudy (N=142) | Low |
| D-HART1 pilot (anakinra, open-label, 2015) | vantassell2017dhart2.md | Precursor pilot to D-HART2 (already ingested as vantassell2018dhart2) | Low — superseded by its own follow-up trial |
| Ex-DHF pilot (Edelmann 2011, N=64) / PARIS-1 (Kitzman 2010, N=49) | mirzai2025exercise.md | Early exercise-training pilot RCTs, distinct from `edelmann2013aldodhf`/`edelmann2025exdhf` | Low — superseded by larger follow-up trials already ingested |
| BEACON study (NTLA-2001, CRISPR base-editing) | masri2026attrcm.md | Phase 1/2 gene-editing approach for ATTR-CM, distinct from the 3 approved-drug candidates in the review file | Medium — emerging modality, promising early data |
| NEURO-TTR (inotersen) / CARDION trials (eplontersen) | masri2026attrcm.md | Earlier/alternative RNA-targeting ATTR-CM approaches | Low-medium |

## Flagged for verification, not action
- **MAYOR-HFpEF** (mentioned in `hfpef-phenotypes.md`, "Anker 2023: Biomarker + Clinical Phenotyping, N=300+") — this cohort name doesn't recur anywhere else, and `Anker2023HFpEFPhenotype` is otherwise described elsewhere as a consensus/scientific-statement document, not a primary cohort study. Possible naming error in the citing page — worth checking against the original source before treating as a real gap.

## Follow-up needed: 3 meta-analyses not yet transcribed into `sources-pending-from-meta-analyses.md`
The discovery pass surfaced large component-study tables inside these already-ingested reviews that haven't been broken out into that registry's per-meta-analysis section format yet (unlike Lee2024, Lin2023CMD, Kaddoura2024, Fu2024, vanDeBovenkamp2025, Ammar2025, and now Yi2025AI — done 2026-09-18, see `sources-pending-from-meta-analyses.md` → "From Yi 2025"):
- `mahmood2024guidelines.md` — comparator trials (STOP-HF, PONTIAC, REACH-HFpEF) — partially covered above
- `masri2026attrcm.md` — ATTR-CM drug/gene-therapy trials — partially covered above
- `bohmke2022nonpharm.md` — nonpharmacological/nutrition trial components — partially covered above

Say the word if you want these transcribed into new `## From <source>` sections of `wiki/sources-pending-from-meta-analyses.md` following its existing format.
