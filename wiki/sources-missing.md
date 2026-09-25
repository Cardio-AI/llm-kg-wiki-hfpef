---
type: meta
title: Missing Source Pages — Standalone Papers Referenced Without a Page
summary: Citekeys/papers named in wiki prose (History sections, background mentions, "as shown by X et al...") that have no wiki/sources/ page and aren't a trial/study captured elsewhere. Not auto-created — for manual review.
tags:
  - meta
  - pending
  - sources
created: 2026-07-14
last_updated: 2026-09-21 (session 4)
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
| Rosch S, Kresoja KP, Besler C, Fengler K, Schober AR, von Roeder M, Lucke C, Gutberlet M, Thiele H, Rommel KP, Lurz P. Characteristics of heart failure with preserved ejection fraction across the range of left ventricular ejection fraction. Circulation. 2022;146:506–518. | capone2026hfpefpht.md | Cited repeatedly (ref #16) for prior RV-EMB metabolomic findings (glucose-6-phosphate, pyruvate, BCAA levels) in HFpEF from the same Leipzig investigator group (Rommel, Lurz) — used as the comparator baseline for Capone 2026's obesity-vs-HFpEF distinction; DOI not visible in the reference list as formatted, [needs source] | Medium-high — same authors/programme as already-ingested [[rommel2016stiffmap]], directly informs interpretation of [[capone2026hfpefpht]]'s glycolysis findings |
| Vaduganathan M, Docherty KF, Claggett BL, et al. SGLT-2 inhibitors in patients with heart failure: a comprehensive meta-analysis of five randomised controlled trials. Lancet. 2022;400(10354):757–767. doi:10.1016/S0140-6736(22)01429-5 | vaduganathan2025finegltsecondary.md | Cited (ref #14) as the definitive SGLT2i-in-HF meta-analysis; directly relevant to this wiki's SGLT2i coverage but not yet a standalone source page (SGLT2i evidence currently synthesised via [[minisy2025sglt2]] and trial-specific pages) | Medium-high — landmark 5-trial pooled meta-analysis, would strengthen [[sglt2-inhibitors]] |
| Ferreira JP, Zannad F, Filippatos G, Schueler E, Steubl D, Zeller C, Januzzi JL, Pocock S, Packer M, et al. Mineralocorticoid receptor antagonists and sodium-glucose cotransporter 2 inhibitors in patients with heart failure and preserved ejection fraction. Eur Heart J. 2022;43(11):1129–1137. doi:10.1016/j.jacc.2022.01.029 (as printed in the citing paper's own reference list — journal is Eur Heart J but the DOI prefix reads `10.1016/j.jacc`, [needs source] to confirm the real DOI on ingest, not assumed corrected) | vaduganathan2025finegltsecondary.md | Cited (ref #15) as prior pooled evidence for the MRA+SGLT2i combination question in HFpEF — same clinical question this wiki tracks via [[confirmation-hf]] and [[balanced-hf]] | Medium-high — directly relevant to the MRA+SGLT2i combination-therapy thread |
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
| Backhaus 2025, Sci Rep 15:4090 (doi:10.1038/s41598-025-87032-5) | backhaus2021hfpefstress.md | HFpEF-Stress cohort follow-up: serial CMR shows diastolic-dysfunction progression relates to impaired RV deformation | Medium — same cohort, mechanistic extension |
| Schulz 2024, Radiol Cardiothorac Imaging 6(4):e230344 (doi:10.1148/ryct.230344) | backhaus2021hfpefstress.md | HFpEF-Stress cohort: CMR-derived aortic stiffness associated with early HFpEF stages/progression | Medium — same cohort |
| Backhaus 2024, Circ Cardiovasc Imaging 17(7):e016424 (doi:10.1161/CIRCIMAGING.123.016424) | backhaus2021hfpefstress.md | HFpEF-Stress cohort: LA roof enlargement as a distinct HFpEF feature | Medium — same cohort; directly relevant to [[left-atrial-remodelling]] |
| Backhaus 2024, Int J Cardiol 404:131949 (doi:10.1016/j.ijcard.2024.131949) | backhaus2021hfpefstress.md | HFpEF-Stress cohort: prognostic/diagnostic implications of impaired rest and exercise-stress LA compliance | Medium — same cohort; extends the ingested primary paper's LA-mechanics findings |
| Backhaus 2024, J Cardiovasc Magn Reson 26(1):101032 (doi:10.1016/j.jocmr.2024.101032) | backhaus2021hfpefstress.md | HFpEF-Stress cohort: rest/exercise-stress estimated PCWP by free-breathing real-time CMR | Medium — same cohort; directly extends the ingested paper's noninvasive-PCWP-estimation angle |
| Zile 2026, JACC Cardiovasc Imaging 19(1):1–15 (doi:10.1016/j.jcmg.2025.08.005) | stone2024relievehf.md | RELIEVE-HF mechanistic follow-up: basis for the differential HFrEF-vs-HFpEF interatrial shunt treatment effect | High — would directly explain the HFpEF-harm signal flagged in [[contradictions]] #39 |
| Stone 2026, Circ Heart Fail (online ahead of print, doi:10.1161/CIRCHEARTFAILURE.125.014100) | stone2024relievehf.md | RELIEVE-HF: individual-patient outcome modelling after interatrial shunt treatment | Medium — same trial, secondary modelling analysis |
| Ferreira 2026, JACC Heart Fail (online ahead of print, doi:10.1016/j.jchf.2026.103111) | ferreira2025sogaldipef.md | SOGALDI-PEF secondary analysis: renin/aldosterone and treatment response to dapagliflozin, spironolactone, and combination | Medium-high — same trial, would clarify the mechanistic driver of the primary NT-proBNP result |

## Flagged for verification, not action
- **MAYOR-HFpEF** (mentioned in `hfpef-phenotypes.md`, "Anker 2023: Biomarker + Clinical Phenotyping, N=300+") — this cohort name doesn't recur anywhere else, and `Anker2023HFpEFPhenotype` is otherwise described elsewhere as a consensus/scientific-statement document, not a primary cohort study. Possible naming error in the citing page — worth checking against the original source before treating as a real gap.

## Follow-up needed: 3 meta-analyses not yet transcribed into `sources-pending-from-meta-analyses.md`
The discovery pass surfaced large component-study tables inside these already-ingested reviews that haven't been broken out into that registry's per-meta-analysis section format yet (unlike Lee2024, Lin2023CMD, Kaddoura2024, Fu2024, vanDeBovenkamp2025, Ammar2025, and now Yi2025AI — done 2026-09-18, see `sources-pending-from-meta-analyses.md` → "From Yi 2025"):
- `mahmood2024guidelines.md` — comparator trials (STOP-HF, PONTIAC, REACH-HFpEF) — partially covered above
- `masri2026attrcm.md` — ATTR-CM drug/gene-therapy trials — partially covered above
- `bohmke2022nonpharm.md` — nonpharmacological/nutrition trial components — partially covered above

Say the word if you want these transcribed into new `## From <source>` sections of `wiki/sources-pending-from-meta-analyses.md` following its existing format.
