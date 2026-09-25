---
type: meta
title: Clinical Trials — Pending Addition
summary: Trials referenced in ingested wiki sources but not yet added as entity/source pages. Review and decide which to ingest. When added, move to trials.md and delete from this file.
tags:
  - trial
  - pending
  - meta
created: 2026-05-04
last_updated: 2026-09-21 (session 6)
---
# Clinical Trials — Pending Addition

> Trials explicitly mentioned in ingested wiki sources that do not yet have their own entity or source pages. Review each entry and decide whether to add to the wiki. When a trial is added, create its entity and source stub pages, add it to [[trials]], and delete it from this file.

---

## Pending Trials

Three groups, tracked separately:
- **Group A — named only**: mentioned in an ingested source, no registry clip and no results paper in hand yet. Nothing to create.
- **Group B — registry page in hand, status active** (see below, after Group A): a clinicaltrials.gov/DRKS page has been clipped and the trial's entity page already created from it (per `_tasks/ingest.md`'s registry-only-ingest rule) — the registry confirms an active status (Recruiting, Active-not-recruiting, or Completed-but-unpublished) and there is still no results/design paper, so it stays here rather than graduating to `trials.md`. Once a results paper is ingested, the trial is removed from this file entirely and gets its `trials.md` row.
- **Group C — registry page in hand, status uncertain** (see below, after Group B): same as Group B, but the registry's own status field is Unknown, Terminated, Withdrawn, or Suspended — i.e. the registry itself cannot confirm the trial is still progressing. A results paper may never materialize. Distinct from Group B because "awaiting results" (Group B's framing) overstates how likely a result is to arrive; the correct follow-up is periodic re-checking of the registry status, not passive waiting.

## Group A — Named Only (No Clipper, No Results Paper)

*(All entries processed as of 2026-05-12, session 12. New trials will appear here as new sources are ingested.)*

### Added 2026-05-14 (session 19) — from Borlaug 2023 JACC Scientific Statement, Table 5 (source: [[borlaug2023statement]])

| Trial                         | Full Title / Intervention                                                                                                                                                                                                                                            | Population                         | NCT         | Notes                                                                                                                                                                                             |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CAMEO-SEMA                    | Semaglutide vs. placebo in HFpEF with obesity                                                                                                                                                                                                                        | LVEF ≥50%, BMI ≥30, NT-proBNP ≥300 | [verify]    | Symptomatic and hemodynamic endpoints                                                                                                                                                             |
| CAMEO-DAPA                    | Dapagliflozin vs. placebo in HFpEF                                                                                                                                                                                                                                   | LVEF ≥50%                          | [verify]    | Companion to CAMEO-SEMA                                                                                                                                                                           |
| ~~HuMAIN~~                    | ~~INGESTED~~ — HuMAIN = HU6 (mitochondrial uncoupler small molecule, NOT bioartificial kidney); NCT05284617; Phase 2A; pandey2025humain ([[pandey2025humain]]); moved to [[trials]]                                                                                  | —                                  | NCT05284617 | Removed from pending                                                                                                                                                                              |
| ~~SPIRRIT~~                   | ~~INGESTED~~ — entity [[spirrit]] and source [[lund2024spirrit]] created (session 30); full design from Lund et al. Eur J Heart Fail 2024;26:2453–2463; NCT02901184; moved to [[trials]]                                                                             | —                                  | NCT02901184 | Removed from pending                                                                                                                                                                              |
| ~~PARAGLIDE-HF~~              | ~~INGESTED~~ — entity [[paraglide-hf]] and sources [[mentz2023paraglide]], [[fudim2024paraglide]], [[nouhravesh2025paraglide]], [[rambarat2025paraglide]] created; NCT03988634 (corrected from NCT04164043); moved to [[trials]]                                     | LVEF >40%, WHF                     | NCT03988634 | Removed from pending                                                                                                                                                                              |
| CADENCE                       | Cardiac resynchronization therapy vs. device pacing in HFpEF with AF                                                                                                                                                                                                 | HFpEF + AF + pacing indication     | [verify]    | Pacing strategy                                                                                                                                                                                   |
| PH-HFpEF                      | Macitentan vs. placebo in HFpEF with pulmonary hypertension                                                                                                                                                                                                          | HFpEF + elevated PVR               | [verify]    | Pulmonary vascular phenotype                                                                                                                                                                      |
| ~~INABLE-Training~~           | ~~INGESTED~~ — INABLE-Training is inorganic sodium nitrite (40 mg TID) + exercise vs. placebo + exercise (NOT ivabradine); NCT02713126; Borlaug 2024, Mayo Clin Proc 2024;99(2):206–217; entity in [[trials]] and source [[borlaug2024inable]]; removed from pending | —                                  | NCT02713126 | Removed from pending — entry description was incorrect                                                                                                                                            |
| KNO3CK OUT HFpEF              | Inorganic nitrate vs. placebo in HFpEF                                                                                                                                                                                                                               | LVEF ≥50%                          | [verify]    | Tests NO/cGMP pathway; same mechanistic target as NEAT-HFpEF, INDIE                                                                                                                               |
| RESPONDER (renal denervation) | Renal denervation in HFpEF                                                                                                                                                                                                                                           | LVEF ≥50%, hypertension            | [verify]    | Sympathetic mechanism target — **name collision warning**: distinct from `[[responder-hf]]` (Corvia atrial-shunt successor to REDUCE LAP-HF II, NCT05233358), already an entity page in this wiki |
| ~~RELIEVE-HF~~                | ~~INGESTED~~ — **the NCT04583527 / "successor to REDUCE LAP-HF II" description above was wrong.** Actual RELIEVE-HF = V-Wave Ltd interatrial shunt, NCT03499236, N=508; safe but neutral overall, harmful in preserved-LVEF stratum (HR 3.24 mortality); entity [[relieve-hf]] and source [[stone2024relievehf]] created; moved to [[trials]] | — | NCT03499236 | Removed from pending — entry NCT/description were incorrect |
| FROST-HF                      | Splanchnic nerve modulation (REBALANCE-HF 2.0)                                                                                                                                                                                                                       | HFpEF                              | [verify]    | Blinded phase of splanchnic ablation                                                                                                                                                              |
| RELAXIN-LA                    | Serelaxin (relaxin-2) targeting LA stiffness                                                                                                                                                                                                                         | HFpEF with LA myopathy             | [verify]    | LA myopathy phenotype                                                                                                                                                                             |
| ENDEAVOR                      | Exercise training + pharmacotherapy combination                                                                                                                                                                                                                      | HFpEF                              | [verify]    | Combination phenotype                                                                                                                                                                             |
| HERMES                        | Hemodynamic exercise response — mechanistic study                                                                                                                                                                                                                    | HFpEF                              | [verify]    | Observational/mechanistic                                                                                                                                                                         |
| CoIPET                        | Coronary physiology in invasive CPET                                                                                                                                                                                                                                 | HFpEF with CMD                     | [verify]    | CMD phenotype                                                                                                                                                                                     |
| ~~REBALANCE-HF~~              | ~~INGESTED~~ — entity [[rebalance-hf]] and source [[fudim2024rebalance]] created; NCT04592445 confirmed; sham-controlled RCT published JAMA Cardiol 2024;9(12):1143–1153; exercise PCWP −5.4 mmHg (P=0.003); moved to [[trials]]                                     | HFpEF                              | NCT04592445 | Removed from pending                                                                                                                                                                              |
| AIM HIGHer                    | IV iron + exercise in HFpEF with iron deficiency                                                                                                                                                                                                                     | LVEF ≥50%, iron deficiency         | [verify]    | Iron deficiency phenotype                                                                                                                                                                         |
| HERACLES-HFpEF                | Ranolazine in HFpEF with ischaemia                                                                                                                                                                                                                                   | HFpEF + coronary disease           | [verify]    | Ischaemic phenotype                                                                                                                                                                               |
| IRONMET-HFpEF                 | Metformin + iron in HFpEF                                                                                                                                                                                                                                            | HFpEF + T2DM/iron deficiency       | [verify]    | Metabolic phenotype combo                                                                                                                                                                         |
| AMETHYST                      | Aldosterone synthase inhibitor in HFpEF                                                                                                                                                                                                                              | LVEF ≥50%, elevated aldosterone    | [verify]    | MRA-alternative mechanism                                                                                                                                                                         |

---

### Added 2026-05-19 (session 29) — from Sauer 2026 ESC Heart Failure review (source: [[sauer2026pharmacological]])

*(BALANCED-HF and EASi-HF moved to Group B below on 2026-09-21 — entity pages created from their registry clips.)*

> **Note:** NCT numbers marked [verify] require verification against clinicaltrials.gov. Several of these trials may have updated status or have been published by 2026. Add PDFs to `raw/` and promote to `trials.md` on ingest.

---

### Added 2026-05-19 (session 30) — from Lund 2024 SPIRRIT-HFpEF design paper, Table 1 (source: [[lund2024spirrit]])

| Trial | Full Title / Intervention | Population | NCT | Notes |
|---|---|---|---|---|
| ~~SOGALDI-PEF~~ | ~~INGESTED~~ — completed, N=108, results published JACC Heart Fail 2025 (Ferreira et al.); entity [[sogaldi-pef]] and source [[ferreira2025sogaldipef]] created; moved to [[trials]] | — | NCT05676684 | Removed from pending |
| ~~CONFIRMATION-HF~~ | ~~Registry clip added~~ — real registry has **no LVEF eligibility restriction** (any-EF, not "HFpEF; LVEF ≥45%" as originally listed here); entity [[confirmation-hf]] created; moved to Group B below | — | NCT06024746 | Moved to Group B |

*(REDEFINE-HF moved to Group B below on 2026-09-21 — entity page created from its registry clip.)*

---

### Added 2026-09-21 (session — from user-supplied `raw/study_libary.xlsx`, German/European HFpEF cohort & registry library)

Cross-checked all 25 studies in the spreadsheet against the wiki: 10 already fully covered (MyoVasc, MyoMobile, TORCH/TORCH-Plus, EMPEROR-Preserved, Decipher HFpEF-DZHK12, OptimEx-Clin, Ex-DHF, OptimEx-LTF follow-up, CABA-HFpEF — all with entity + `trials.md` row + source). The 15 below were untracked; added here. Priority tier reflects HFpEF-relevance + data readiness, per CLAUDE.md's HFpEF-relevance-governs-depth rule — not chronological order.

| Trial | Full Title / Intervention | Population | NCT | Notes |
|---|---|---|---|---|
| ~~HFpEF-stress-DZHK17~~ | ~~INGESTED~~ — entity [[hfpef-stress-trial]] and source [[backhaus2021hfpefstress]] created; moved to [[trials]] | — | NCT03260621 | Removed from pending |
| ~~STIFFMAP~~ | ~~INGESTED~~ — entity [[stiffmap]] and source [[rommel2016stiffmap]] created; moved to [[trials]] | — | NCT02459626 | Removed from pending |
| ~~HFpEF-PHT (STIFFMAP substudy)~~ | ~~INGESTED~~ — real title "Right Ventricular Function and Pulmonary Hypertension in HFpEF"; not literally a STIFFMAP substudy, but same Leipzig programme; entity [[hfpef-pht]] and source [[capone2026hfpefpht]] created; N=23 biopsy sub-cohort (19 HFpEF/4 NFO), not N=45 as originally listed; moved to [[trials]] | — | NCT05055180 | Removed from pending |
| ~~MAPPED~~ | ~~Registry clip added~~ — real registry status is **"Unknown"** (last known: Recruiting, 2024-03), not "completed 03.2019–12.2024" as originally listed here (that date range does not match the registry's own 2024-03 registration date — discrepancy unresolved, [needs source]); entity [[mapped]] created; moved to Group C below, **not** Group B (status uncertain, may never publish) | — | NCT06316661 | Moved to Group C |
| DiabetesOmic | Omics study (details unspecified in library) | Unspecified — no population/EF/N recorded | none listed | **Tier 3 — medium, verify relevance.** Linked paper: ScienceDirect, pii S2001037025001710 — read first to determine HFpEF-relevance and correct entity type before creating a page |
| EMPATHY-HF | Drug vs. placebo interventional trial | HF (EF criteria not specified); N=1,364; ongoing 03.2022–12.2025 | NCT05776043 | **Tier 3 — medium, verify relevance.** Population not confirmed HFpEF-specific in the source data — check on ingest |
| Gutenberg Health Study | Representative population cohort | General population, age 45–85; N=15,000; 2007–2027 | none | **Tier 4 — medium, background/epi source.** Not a disease-specific trial; worth a page only once a specific HFpEF-relevant substudy paper is identified |
| Hamburg City Health Study (HCHS) | Representative population cohort | General population, age 45–74; N=45,000; 2016–2028 | NCT03934957 | **Tier 4 — medium, background/epi source.** Same logic as Gutenberg Health Study |
| UK Biobank | Representative population cohort | General population, age 40–69; N=500,000; 2006–2036 | none | **Tier 4 — medium, background/epi source.** Same logic; very large N makes it a strong candidate once an HFpEF-specific derived paper is found |
| NAKO | Representative population cohort (German national cohort) | General population, age 20–69; N=200,000; 2014–2024+ | none | **Tier 4 — medium, background/epi source.** Same logic |
| ~~TRAIN-HFpEF-PH~~ | ~~INGESTED~~ — design/protocol paper found (Paleviciuté 2023, *Trials*); entity [[train-hfpef-ph]] and source [[paleviciute2023trainhfpefph]] created; N=90 target, primary completion est. 2025 Q4; moved to [[trials]] | — | NCT05464238 | Removed from pending |
| Preserve-Synch-DZHK30 | Pacemaker-induced cardiomyopathy study | Pacemaker-induced cardiomyopathy, LVEF ≥40%; N=200; just started 09.2025 | DRKS00037542 | **Tier 5 — low, watch-list.** Just started; no data yet; borderline HFmrEF/HFpEF EF range but niche etiology |

*(EXCALIBUR-HFpEF moved to Group B below on 2026-09-21 — entity page created from its registry clip.)*
| TRICI-HF-DZHK24 | Drug interventional trial, HF with tricuspid regurgitation | **HFrEF**, not HFpEF; N=360; ongoing 03.2022–07.2026 | NCT04634266 | **Tier 6 — low, off-topic population.** Paper already published (PubMed 40785632) but population is HFrEF — out of primary wiki scope; relevant only as an HFrEF comparator if a page later needs one |
| CMR-ICD-DZHK23 | Interventional study, non-ischaemic dilatative cardiomyopathy | Non-ischaemic DCM, LVEF ≥35% (not HFpEF); N=760; ongoing 01.2021–11.2027 | NCT04558723 | **Tier 6 — low, off-topic population.** EF range and etiology are outside HFpEF scope |

---

### Added 2026-09-21 (session — from Khidihir & Kalra 2026 Curr Atheroscler Rep finerenone review, source: [[khidihir2026finerenone]])

| Trial | Full Title / Intervention | Population | NCT | Notes |
|---|---|---|---|---|
| FINE-FOCUS | Finerenone effect on myocardial fibrosis and cardiac structure/function, with ¹⁸F-FAPI-PET/CT fibrosis substudy | Symptomatic HF, LVEF ≥40% | NCT07583173 | Multicentre, randomised, double-blind, placebo-controlled; mechanistic imaging trial |
| FINE-REMODEL | Finerenone effect on cardiac remodelling imaging endpoints in diabetic kidney disease + HF | Diabetic kidney disease + HF, LVEF ≥40% | NCT07442448 | Mechanistic imaging trial; 6-month endpoint per review |
| FINE-MECH | Finerenone mechanistic imaging trial (complementary to FINE-FOCUS/FINE-REMODEL) | Not fully specified in source review | NCT07270367 | Design detail not otherwise specified in [[khidihir2026finerenone]]; verify on ingest |

---

## Group B — Registry Page In Hand (Entity Page Created, No Results Paper Yet)

A clinicaltrials.gov/DRKS registry page has been clipped for each of these and used to create a full entity page (`doi: null`, sourced from the registry page itself — see `_tasks/ingest.md`'s registry-only-ingest rule). None have a results or design paper yet, so they are **not** in `wiki/trials.md`. Once a results paper is ingested, remove the row here, create the `wiki/sources/` page, and add the `trials.md` row as normal.

| Trial | Entity Page | Registry ID | Registry Status (as of 2026-09-21) | Notes |
|---|---|---|---|---|
| EXCALIBUR-HFpEF | [[excalibur-hfpef]] | DRKS00039892 | Recruiting (started 2026-01-27) | HFpEF, LVEF >40%; N=200 target; app-based exercise coaching vs. standard care; Heidelberg/Mainz |
| BalanceD-HF | [[balanced-hf]] | NCT06307652 | Recruiting | Balcinrenone/dapagliflozin vs. dapagliflozin; N=3,850 (est.); AstraZeneca; EF eligibility not stated on registry page — [needs source] |
| EASi-HF Preserved | [[easi-hf]] | NCT06424288 | Recruiting | Vicadrostat + empagliflozin vs. placebo + empagliflozin; HFpEF/HFmrEF, LVEF ≥40%; N=6,000 (est.); Boehringer Ingelheim |
| REDEFINE-HF | [[redefine-hf]] | NCT06008197 | Recruiting | Finerenone vs. placebo in post-ADHF hospitalisation; HFpEF/HFmrEF, LVEF ≥40%; N=5,200 (est.); Colorado Prevention Center |
| CONFIRMATION-HF | [[confirmation-hf]] | NCT06024746 | Recruiting | Finerenone + empagliflozin vs. usual care, open-label, in hospitalized HF; **any-EF (no LVEF restriction on registry)**, not HFpEF-restricted; N=1,500 (est.); Colorado Prevention Center/Bayer |

---

## Group C — Registry Page In Hand, Status Uncertain (Unknown/Terminated/Withdrawn/Suspended — May Never Produce a Results Paper)

A clipped registry page exists and an entity page has been created from it (same sourcing pattern as Group B), but the registry's own status field is **Unknown, Terminated, Withdrawn, or Suspended** rather than an active status — the registry itself cannot confirm the trial is still progressing, so a results paper may never appear. Do not treat these the same as Group B's "just waiting on results" framing. Appropriate follow-up is periodic re-checking of the registry record, not passive waiting; if a status is later re-confirmed as active (Recruiting/Active-not-recruiting/Completed), move the row to Group B instead.

| Trial | Entity Page | Registry ID | Registry Status (as of date checked) | Notes |
|---|---|---|---|---|
| MAPPED | [[mapped]] | NCT06316661 | **Unknown status** (last known: Recruiting, 2024-03; not updated since — checked 2026-09-21) | CMR microvascular/fibrosis study in two HFpEF phenogroups vs. controls; N=60 (est.); Istituto Auxologico Italiano, Milan. Source spreadsheet's stated "03.2019–12.2024" recruiting window does not match the registry's own 2024-03 registration date — discrepancy unresolved, [needs source] |

---

## How to Add a Trial

**With a results/design paper (full ingest):**
1. Create `wiki/entities/<trial-abbreviation-lowercase>.md` (entity template)
2. Create `wiki/sources/<citekey>.md` (study template)
3. Add to appropriate section of [[trials]] (master overview table)
4. Add citekey to [[citations]]
5. Link from relevant entity/concept pages
6. Remove this entry from `trials-pending.md`
7. Update `wiki/log.md`

**With only a registry clip, no paper yet, status active (registry-only ingest — see `_tasks/ingest.md`):**
1. Create `wiki/entities/<trial-abbreviation-lowercase>.md` only (no source page)
2. `sources:` uses the NCT/DRKS ID as citekey, `doi: null` + comment pointing to the registry URL
3. Move the entry from Group A to Group B above (do **not** add to `wiki/trials.md`, do **not** remove from this file)
4. Update `wiki/log.md`
5. When a results paper later appears: do the full-ingest steps above, and only then remove the trial from this file entirely

**With only a registry clip, status Unknown/Terminated/Withdrawn/Suspended (see `_tasks/ingest.md`):**
1. Same entity-page creation as Group B (step 1–2 above), but the `## Status` section states the actual registry status and last-known-active date instead of the ordinary "no results yet" phrasing, and flags that a results paper may never appear
2. Move the entry from Group A directly to Group C above (do **not** add to `wiki/trials.md`, do **not** add to Group B)
3. Update `wiki/log.md`
4. If the registry status is later re-confirmed as active: move the row from Group C to Group B. If a results paper appears: do the full-ingest steps above and remove the trial from this file entirely
