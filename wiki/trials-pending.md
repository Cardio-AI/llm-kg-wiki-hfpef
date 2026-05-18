---
type: meta
title: Clinical Trials — Pending Addition
summary: Trials referenced in ingested wiki sources but not yet added as entity/source pages. Review and decide which to ingest. When added, move to trials.md and delete from this file.
tags:
  - trial
  - pending
  - meta
created: 2026-05-04
last_updated: 2026-05-15
---
# Clinical Trials — Pending Addition

> Trials explicitly mentioned in ingested wiki sources that do not yet have their own entity or source pages. Review each entry and decide whether to add to the wiki. When a trial is added, create its entity and source stub pages, add it to [[trials]], and delete it from this file.

---

## Pending Trials

*(All entries processed as of 2026-05-12, session 12. New trials will appear here as new sources are ingested.)*

### Added 2026-05-14 (session 19) — from Borlaug 2023 JACC Scientific Statement, Table 5 (source: [[borlaug2023statement]])

| Trial | Full Title / Intervention | Population | NCT | Notes |
|---|---|---|---|---|
| CAMEO-SEMA | Semaglutide vs. placebo in HFpEF with obesity | LVEF ≥50%, BMI ≥30, NT-proBNP ≥300 | [verify] | Symptomatic and hemodynamic endpoints |
| CAMEO-DAPA | Dapagliflozin vs. placebo in HFpEF | LVEF ≥50% | [verify] | Companion to CAMEO-SEMA |
| ~~HuMAIN~~ | ~~INGESTED~~ — HuMAIN = HU6 (mitochondrial uncoupler small molecule, NOT bioartificial kidney); NCT05284617; Phase 2A; pandey2025humain ([[pandey2025humain]]); moved to [[trials]] | — | NCT05284617 | Removed from pending |
| SPIRRIT | Spironolactone in HFpEF | LVEF ≥45%, NT-proBNP elevated | NCT02901184 | Ongoing; will clarify MRA class effect vs. TOPCAT |
| SPIRIT-HF | Spironolactone in HFpEF | LVEF ≥45% | NCT04727073 | Companion spironolactone trial |
| ~~PARAGLIDE-HF~~ | ~~INGESTED~~ — entity [[paraglide-hf]] and sources [[mentz2023paraglide]], [[fudim2024paraglide]], [[nouhravesh2025paraglide]], [[rambarat2025paraglide]] created; NCT03988634 (corrected from NCT04164043); moved to [[trials]] | LVEF >40%, WHF | NCT03988634 | Removed from pending |
| CADENCE | Cardiac resynchronization therapy vs. device pacing in HFpEF with AF | HFpEF + AF + pacing indication | [verify] | Pacing strategy |
| PH-HFpEF | Macitentan vs. placebo in HFpEF with pulmonary hypertension | HFpEF + elevated PVR | [verify] | Pulmonary vascular phenotype |
| ~~INABLE-Training~~ | ~~INGESTED~~ — INABLE-Training is inorganic sodium nitrite (40 mg TID) + exercise vs. placebo + exercise (NOT ivabradine); NCT02713126; Borlaug 2024, Mayo Clin Proc 2024;99(2):206–217; entity in [[trials]] and source [[borlaug2024inable]]; removed from pending | — | NCT02713126 | Removed from pending — entry description was incorrect |
| KNO3CK OUT HFpEF | Inorganic nitrate vs. placebo in HFpEF | LVEF ≥50% | [verify] | Tests NO/cGMP pathway; same mechanistic target as NEAT-HFpEF, INDIE |
| RESPONDER | Renal denervation in HFpEF | LVEF ≥50%, hypertension | [verify] | Sympathetic mechanism target |
| RELIEVE-HF | Interatrial shunt device | HFpEF/HFmrEF | NCT04583527 | Successor to REDUCE LAP-HF II; PVR-stratified enrollment |
| FROST-HF | Splanchnic nerve modulation (REBALANCE-HF 2.0) | HFpEF | [verify] | Blinded phase of splanchnic ablation |
| RELAXIN-LA | Serelaxin (relaxin-2) targeting LA stiffness | HFpEF with LA myopathy | [verify] | LA myopathy phenotype |
| CABA-HFpEF | Catheter ablation vs. rate control in HFpEF with AF | HFpEF + AF | NCT05508256 | Already in trials.md; repeat reference in Table 5 |
| ENDEAVOR | Exercise training + pharmacotherapy combination | HFpEF | [verify] | Combination phenotype |
| HERMES | Hemodynamic exercise response — mechanistic study | HFpEF | [verify] | Observational/mechanistic |
| CoIPET | Coronary physiology in invasive CPET | HFpEF with CMD | [verify] | CMD phenotype |
| REBALANCE-HF | Splanchnic nerve ablation (open-label phase positive) | HFpEF | [verify] | Blinded RCT phase ongoing |
| AIM HIGHer | IV iron + exercise in HFpEF with iron deficiency | LVEF ≥50%, iron deficiency | [verify] | Iron deficiency phenotype |
| HERACLES-HFpEF | Ranolazine in HFpEF with ischaemia | HFpEF + coronary disease | [verify] | Ischaemic phenotype |
| IRONMET-HFpEF | Metformin + iron in HFpEF | HFpEF + T2DM/iron deficiency | [verify] | Metabolic phenotype combo |
| REHAB-HFpEF | Rehabilitation-based exercise programme | LVEF ≥50%, recent HHF | [verify] | Post-discharge exercise |
| AMETHYST | Aldosterone synthase inhibitor in HFpEF | LVEF ≥50%, elevated aldosterone | [verify] | MRA-alternative mechanism |

> **Note:** NCT numbers marked [verify] require verification against clinicaltrials.gov. Several of these trials may have updated status or have been published by 2026. Add PDFs to `raw/` and promote to `trials.md` on ingest.

---

## How to Add a Trial

1. Create `wiki/entities/<trial-abbreviation-lowercase>.md` (entity template)
2. Create `wiki/sources/<citekey>.md` (study template)
3. Add to appropriate section of [[trials]] (master overview table)
4. Add citekey to [[citations]]
5. Link from relevant entity/concept pages
6. Remove this entry from `trials-pending.md`
7. Update `wiki/log.md`
