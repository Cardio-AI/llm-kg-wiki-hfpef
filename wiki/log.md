# Change Log

## 2026-04-30 (session 1)
- Ingested: raw/2021-ESC-Guidelines-Heart-Failure.pdf (McDonagh2021ESC)
- Created:
  - wiki/sources/mcdonagh2021esc.md
  - wiki/entities/hfpef.md
  - wiki/entities/hfmref.md
  - wiki/entities/hfref.md
  - wiki/entities/sglt2-inhibitors.md
  - wiki/entities/sacubitril-valsartan.md
  - wiki/entities/spironolactone.md
  - wiki/entities/paragon-hf.md (stub)
  - wiki/entities/topcat.md (stub)
  - wiki/entities/charm-preserved.md (stub)
  - wiki/entities/i-preserve.md (stub)
  - wiki/concepts/hf-phenotype-classification.md
  - wiki/concepts/hfpef-diagnosis.md
  - wiki/concepts/hfpef-treatment-gap.md
  - wiki/concepts/diastolic-dysfunction.md
  - wiki/concepts/natriuretic-peptides.md
- Updated:
  - wiki/index.md (initial population)
  - wiki/overview.md (initial population)
  - wiki/contradictions.md (initial population)

## 2026-04-30 (session 2 — template migration + content fixes + study stubs)

### Template migration (all pages migrated from old ## Content format to current templates)
- wiki/sources/mcdonagh2021esc.md — migrated to source template
- wiki/entities/hfpef.md — migrated to entity template
- wiki/entities/hfref.md — migrated to entity template
- wiki/entities/hfmref.md — migrated to entity template
- wiki/entities/sglt2-inhibitors.md — migrated to entity template
- wiki/entities/sacubitril-valsartan.md — migrated to entity template
- wiki/entities/spironolactone.md — migrated to entity template
- wiki/entities/paragon-hf.md — migrated to entity template; added link to source stub
- wiki/entities/topcat.md — migrated to entity template; added link to source stub
- wiki/entities/charm-preserved.md — migrated to entity template; added link to source stub
- wiki/entities/i-preserve.md — migrated to entity template; added link to source stub
- wiki/concepts/hf-phenotype-classification.md — migrated to concept template
- wiki/concepts/diastolic-dysfunction.md — migrated to concept template
- wiki/concepts/hfpef-diagnosis.md — migrated to concept template
- wiki/concepts/hfpef-treatment-gap.md — migrated to concept template
- wiki/concepts/natriuretic-peptides.md — migrated to concept template

### Content fixes (per user remarks)
- hfpef.md: Added mL/m² to LA volume index >40 threshold; added [[atrial-fibrillation]] hyperlink; added E/e' >13 cut-off (sens 46%, spec 86%); added AF NP thresholds (>365/>105 pg/mL); added TR velocity >2.8 m/s row
- hfpef-diagnosis.md: Same Table 9 fixes; AF thresholds throughout
- hfref.md: Removed repetition; restructured to entity template (Description / Role in HFpEF / Evidence / Status)
- hf-phenotype-classification.md: Diagnostic pathway converted to decision tree (ASCII); removed duplicate sentence in Clinical Relevance section
- diastolic-dysfunction.md: Removed duplicate E/e' accuracy statement from Contradictions (already in Evidence table); cleaned Relationship to HFpEF Heterogeneity

### New entity pages created
- wiki/entities/atrial-fibrillation.md — new entity: AF as cause/consequence of HFpEF; adjusted diagnostic thresholds
- wiki/entities/echocardiography.md — new imaging entity: role, markers, benefits/drawbacks in HFpEF
- wiki/entities/cardiac-mri.md — new imaging entity: gold standard LVEF; tissue characterisation; second-line in HFpEF

### New study stub pages created (wiki/sources/)
- solomon2019paragon.md — PARAGON-HF
- pitt2014topcat.md — TOPCAT
- yusuf2003charm.md — CHARM-Preserved
- massie2008ipreserve.md — I-PRESERVE
- mcmurray2014paradigm.md — PARADIGM-HF
- mcmurray2019dapahf.md — DAPA-HF
- packer2020emperor.md — EMPEROR-Reduced
- anker2021emperor.md — EMPEROR-Preserved
- solomon2022deliver.md — DELIVER
- redfield2015neat.md — NEAT-HFpEF
- zamani2015indie.md — INDIE-HFpEF
- armstrong2020vitality.md — VITALITY-HFpEF
- udelson2020capacity.md — CAPACITY-HFpEF
- ahmed2006dig.md — DIG-Preserved
- pocock2013maggic.md — MAGGIC

### Wiki metadata updated
- wiki/index.md — added all new pages; reorganised by category
- wiki/timeline.md — populated Landmark Trials, Diagnostic Criteria, Treatment, Pathophysiology tables
- wiki/log.md — this entry

## 2026-04-30 (session 3 — ingest: Ho 2019 + Sachdev 2023)

### Sources ingested
- raw/2019-CirculationAHA-Ho-exercise-response.pdf → citekey: Ho2019HFpEFDefinitions
- raw/2023-CirculationAHA-Sachdev-hfpef-exercise.pdf → citekey: Sachdev2023Exercise

### New pages created
- wiki/sources/ho2019hfpefdefinitions.md — study: 7 HFpEF definitions vs. invasive CPET; enrollment 12–90%; HFpEF_phys (53%) independently predicts CV events
- wiki/sources/sachdev2023exercise.md — source: AHA Statement; SET meta-analysis 8 RCTs n=503; VO2 +2.8 mL/kg/min; skeletal muscle mechanism
- wiki/concepts/hfpef-diagnostic-definitions.md — new concept: competing definitions, sensitivity/specificity tables, trial incompatibility implication
- wiki/concepts/exercise-intolerance.md — new concept: four-mechanism model (skeletal muscle primary >50%); therapeutic implications
- wiki/entities/supervised-exercise-training.md — new entity: HIIT/MCT; evidence table; 2022 Class I AHA/ACC; hard outcome caveat
- wiki/entities/cardiopulmonary-exercise-testing.md — new entity: diagnostic gold standard; invasive CPET criteria; mechanistic dissection role

### Existing pages updated
- wiki/concepts/hfpef-diagnosis.md — added Diagnostic Definition Heterogeneity section; sensitivity/specificity table; Ho2019 citation; updated Related Pages
- wiki/concepts/hfpef-treatment-gap.md — added SET as positive intervention with meta-analysis table; updated SGLT2i note; updated Related Pages
- wiki/concepts/diastolic-dysfunction.md — added note that cardiac filling pressure is secondary (not primary) exercise limiter per Sachdev 2023
- wiki/entities/hfpef.md — added HFpEF_phys definition; added SET to Emerging Signals; updated sources and Related Pages
- wiki/contradictions.md — added contradictions 6 (definition heterogeneity), 7 (SET functional vs. hard outcomes), 8 (cardiac vs. peripheral exercise mechanism)
- wiki/overview.md — added session 3 entry; added SET hard outcomes to Active Debates and Knowledge Gaps; updated Key Concepts
- wiki/timeline.md — added Ho 2019 (Diagnostic Criteria, Pathophysiology); added Sachdev 2023 + AHA/ACC 2022 Class I (Treatment)
- wiki/index.md — added new sources (Observational Studies, Scientific Statements sections); added new entities (Diagnostic Tools, Interventions); added new concepts
- wiki/log.md — this entry

## 2026-05-04 (session 4 — ingest: AHA 2022 guideline + TOPCAT design + EMPEROR-Preserved secondary + TORCH; connect registries to papers)

### Sources ingested
- raw/2022-CirculationsAHA-Heidenreich-AHA-ACC-HFSA-Guideline-HF.pdf → citekey: Heidenreich2022AHA
- raw/2011-AHA-Desai-TOPCAT_study.pdf → citekey: Desai2011TOPCAT
- raw/2026-JACCHF-Ferreira-Findings-EMPEROR-Preserved.pdf → citekey: Ferreira2026Emperor
- raw/2017-ESC-HF-Seyler-TORCH_DZHK-1_rationale.pdf → citekey: Seyler2017TORCH
- raw/Study - NCT03251183 (DECIPHER-HFpEF registry) — entity page created
- raw/Study - NCT02187263 (TORCH Phase 1 registry) — linked to TORCH entity
- raw/Study - NCT04265040 (TORCH-Plus registry) — linked to TORCH entity

### New pages created
- wiki/sources/heidenreich2022aha.md — 2022 AHA/ACC/HFSA Guideline; HFimpEF; SGLT2i Class 2a; A–D staging; H₂FPEF; full treatment table
- wiki/concepts/guideline-comparison.md — ESC 2021 vs. AHA 2022 systematic comparison across 7 dimensions
- wiki/sources/desai2011topcat.md — TOPCAT design paper; dual enrollment pathway; 266 centers/6 countries; full parameters
- wiki/sources/ferreira2026emperor.md — EMPEROR-Preserved Mg secondary analysis; 622 sites/23 countries; Mg paradox
- wiki/sources/seyler2017torch.md — TORCH registry rationale; 19 DZHK centres; 4-module structure; biobank
- wiki/entities/torch.md — TORCH / TORCH-Plus registry entity; Phase 1 (NCT02187263) + Phase 2 (NCT04265040)
- wiki/entities/decipher-hfpef.md — DECIPHER-HFpEF entity; 7 German centres; CMR vs. PV loops; n=185; full parameters + biopsy

### Existing pages updated (methods/results expanded from stubs to full content)
- wiki/sources/anker2021emperor.md — Methods fully expanded: LVEF >40%, NT-proBNP thresholds (AF/no-AF), echo criteria, 622 sites/23 countries; Results added; Limitations updated; Secondary analyses table + Ferreira2026 added
- wiki/sources/pitt2014topcat.md — Methods fully expanded: dual pathway, LVEF ≥45%, 266 centers/6 countries, full parameters, spironolactone titration; Results added; Limitations expanded; Secondary analyses table + Desai2011 added

### Entity pages updated
- wiki/entities/sglt2-inhibitors.md — AHA 2022 Class 2a for HFpEF added; status table (ESC 2021 vs. AHA 2022); Ferreira2026 Mg finding added; contradictions updated
- wiki/entities/sacubitril-valsartan.md — AHA 2022 Class 2b for HFpEF added; status table created
- wiki/entities/spironolactone.md — AHA 2022 Class 2b for HFpEF added; status table created

### Concept pages updated
- wiki/concepts/hf-phenotype-classification.md — HFimpEF added as 4th EF category; AHA 2022 distinction; History extended to 2022
- wiki/concepts/hfpef-treatment-gap.md — SGLT2i Class 2a partial gap closure documented; AHA 2022 treatment table; mortality gap still open; Ferreira2026 Mg open question added
- wiki/contradictions.md — Added contradictions 9 (SGLT2i ESC 2021 vs. AHA 2022), 10 (Mg direction reversal), 11 (HFpEF definition stringency difference)

### Metadata pages updated
- wiki/index.md — Added: heidenreich2022aha, desai2011topcat, ferreira2026emperor, seyler2017torch, torch, decipher-hfpef, guideline-comparison; reorganised Clinical Trial Papers section
- wiki/timeline.md — Added: AHA 2022 guideline (Diagnostic Criteria + Treatment entries); Ferreira 2026 (Landmark Trials); Registries section (TORCH 2014, DECIPHER-HFpEF 2017, TORCH-Plus 2020)
- wiki/log.md — this entry
