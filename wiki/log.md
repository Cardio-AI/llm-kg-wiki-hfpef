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

## 2026-05-04 (session 7 — ingest: 9 papers; NCT corrections; stub expansions)

### Sources ingested (PDFs read)
- raw/2015-NEJM-Redfield-NEAT-HFpEF_study.pdf → citekey: Redfield2015NEAT
- raw/2019-eurheartj-pieske-HFA-PEFF_diagnostic_algorithm.pdf → citekey: Pieske2019HFAPEFF
- raw/2018-CirculationAHA-Yogesh-guide_daignosis-hfpef.pdf → citekey: Reddy2018H2FPEF
- raw/2023-CirculationsAHA-McMurry-DETERMINE_study.pdf → citekey: McMurray2024DETERMINE
- raw/2025-JCF-Docherty-DETERIMINE_wearables_physical_activity.pdf → citekey: Docherty2025DETERMINE
- raw/2025-HFR-Mirzai-Review_physical_activity_hfpef.pdf → citekey: Mirzai2025Exercise
- (DELIVER, PARAGON-HF, CHARM-Preserved, I-PRESERVE, VITALITY-HFpEF, CAPACITY-HFpEF read in prior session; stubs expanded this session)

### New source pages created
- wiki/sources/pieske2019hfapeff.md — HFA-PEFF 4-step algorithm; full scoring table; AF-adjusted thresholds; invasive criteria
- wiki/sources/reddy2018h2fpef.md — H₂FPEF score derivation; 6-variable score 0–9; AUC 0.841/0.886; single-centre Mayo Clinic
- wiki/sources/mcmurray2024determine.md — DETERMINE RCTs; HFpEF arm missed all primary endpoints; 6MWD neutral throughout
- wiki/sources/docherty2025determine.md — DETERMINE accelerometry substudy; accelerometer/KCCQ/6MWD measure distinct dimensions
- wiki/sources/mirzai2025exercise.md — 2025 exercise review ~30 RCTs; MICT best evidence; HIIT not superior to MICT; ~1/3 non-responders

### Stub source pages expanded to full content
- wiki/sources/solomon2022deliver.md — DELIVER: N=6,263; HR 0.82 (P<0.001); consistent benefit including LVEF ≥60%
- wiki/sources/solomon2019paragon.md — PARAGON-HF: N=4,822; RR 0.87 (P=0.06); subgroup signals women + LVEF <57%
- wiki/sources/yusuf2003charm.md — CHARM-Preserved: N=3,023; HR 0.89 (P=0.118); HF hosp signal P=0.017
- wiki/sources/massie2008ipreserve.md — I-PRESERVE: N=4,128; HR 0.95 (P=0.35); all-cause death HR 1.00; fully neutral
- wiki/sources/armstrong2020vitality.md — VITALITY-HFpEF: N=789; KCCQ-PLS neutral (P=0.47/0.80); 24 weeks; NCT03547583
- wiki/sources/udelson2020capacity.md — CAPACITY-HFpEF: N=196; peak VO₂ neutral (P=0.37); KCCQ worse on active arm (P=0.007); NCT03254485
- wiki/sources/redfield2015neat.md — NEAT-HFpEF: N=110; primary P=0.06 trend; all-dose combined P=0.02 LESS active; NCT02053493

### NCT corrections in wiki/trials.md (confirmed from ingested PDFs)
- CAPACITY-HFpEF: NCT03254381 → NCT03254485 (confirmed from paper abstract)
- VITALITY-HFpEF: NCT02673164 → NCT03547583 (confirmed from paper abstract)
- NEAT-HFpEF: NCT01516346 → NCT02053493 (confirmed from paper abstract)
- CHARM-Preserved: "pre-registration era" → NCT00634712 (confirmed from registry file)
- I-PRESERVE: removed [verify on ingest] tag — NCT00095238 confirmed from registry file

### New trials added to wiki/trials.md
- DETERMINE-Preserved (NCT03877224) and DETERMINE-Reduced (NCT03877237)

### wiki/trials-pending.md updated
- Added: SOCRATES-PRESERVED (vericiguat phase 2b in HFpEF; Pieske 2017 EHJ)
- Added: VICTORIA (vericiguat in HFrEF; Armstrong 2020 NEJM; NCT02861534) — for EF-comparison context

### Citations updated
- wiki/citations.md: Added 7 new ingested entries (Pieske2019HFAPEFF, Reddy2018H2FPEF, McMurray2024DETERMINE, Docherty2025DETERMINE, Mirzai2025Exercise, Redfield2015NEAT moved from stub)
- wiki/citations.md: Added full formatted references for all new ingested sources
- Yusuf2003CHARM DOI confirmed: 10.1016/S0140-6736(03)14285-7

### wiki/index.md updated
- Added new source pages under Observational Studies, Scientific Statements, Consensus/Guideline Papers, Clinical Trial Papers, Secondary Analyses sections
- Expanded clinical trial entries with key numbers

### wiki/log.md — this entry

---

## 2026-05-04 (session 6 — clinical trials overview, trials-pending, CLAUDE.md rule, Ferreira DOI)

### New pages created
- wiki/trials.md — master clinical trials overview table; 14 RCTs, 3 registries, 1 meta-analysis, secondary analyses; [verify on ingest] flags for unconfirmed NCT numbers
- wiki/trials-pending.md — staging list for trials referenced in sources but not yet added; initial entries: RELAX (sildenafil in HFpEF, from Ho 2019), ATTR-ACT (tafamidis, from AHA 2022 guideline)

### CLAUDE.md updated
- Added Clinical Trials Overview Rule: maintain trials.md + trials-pending.md; on every ingest scan for unreferenced trials; on trial addition move from pending to trials.md; required columns specified

### Citations updated
- wiki/citations.md: Ferreira2026Emperor DOI updated: 10.1016/j.jchf.2025.102889 (provided by user); [doi pending] notes removed

### Metadata updated
- wiki/index.md — added [[trials]] and [[trials-pending]] to Core Pages
- wiki/log.md — this entry

## 2026-05-04 (session 5 — lint, citation registry, redundancy reduction, cross-linking)

### New pages created
- wiki/citations.md — master citekey → full citation registry; 9 ingested + 13 stub sources with full formatted references

### CLAUDE.md updated
- Added Citation Lookup Rule: when user asks for a reference, read citations.md and return full formatted citation by citekey
- Extended Lint definition: redundancy detection, missing citations, stub tracking, citations.md drift

### Redundancies removed (content reduced to summary + pointer to canonical page)
- wiki/entities/hfpef.md: Table 9 marker table → pointer to [[hfpef-diagnosis]]
- wiki/concepts/diastolic-dysfunction.md: Table 9 marker table → bullet summary + pointer to [[hfpef-diagnosis]]
- wiki/concepts/guideline-comparison.md: H₂FPEF scoring table → inline summary + pointer to [[hfpef-diagnosis]]
- wiki/sources/heidenreich2022aha.md: H₂FPEF scoring table → inline summary + pointer to [[hfpef-diagnosis]]

### Content fixes
- wiki/entities/hfpef.md: "Role in HFpEF" → "Epidemiology and Clinical Profile"; ESC Long-Term Registry stat marked [needs source]; Status section → comparison table + AHA 2022; sources updated
- wiki/concepts/exercise-intolerance.md: Evidence table source column fixed to proper `source: filename.pdf` format
- wiki/concepts/natriuretic-peptides.md: Added AHA 2022 NP guidance note, EMPEROR-Preserved trial threshold context, updated sources and Related Pages

### Cross-links added
- diastolic-dysfunction.md → [[guideline-comparison]], [[decipher-hfpef]]
- hfpef-diagnosis.md → [[guideline-comparison]], [[decipher-hfpef]]
- natriuretic-peptides.md → [[guideline-comparison]], [[anker2021emperor]], [[ferreira2026emperor]]

### Metadata
- wiki/index.md — [[citations]] added to Core Pages
- wiki/log.md — this entry

## 2026-05-05 (session 8 — ingest DELIVER)

### Ingested
- raw/2022-NEJM-Solomon-Deliver_study.pdf → [[solomon2022deliver]] (citekey: Solomon2022DELIVER)

### Updated pages
- wiki/sources/solomon2022deliver.md — full rewrite from PDF; added complete Table 1 baseline data, Table 2 outcomes, subgroup forest plot HRs, KCCQ win ratio 1.11 (P=0.009), safety profile, dual-primary statistical design, CV death rate context
- wiki/concepts/hfpef-treatment-gap.md — SGLT2i symptom gap section updated: DELIVER KCCQ positive vs. DETERMINE neutral reconciled
- wiki/contradictions.md — added #16: DELIVER KCCQ positive vs. DETERMINE-Preserved neutral (same drug, different method + follow-up)
- wiki/citations.md — Solomon2022DELIVER promoted from Stub to Ingested; duplicate entries for Pitt2014TOPCAT and Anker2021EMPEROR removed from stubs

### Stubs added to trials-pending.md
- Butler 2022 (Eur Heart J): EMPEROR-Preserved EF spectrum subgroup analysis — motivated DELIVER dual-primary design; DELIVER found no heterogeneity, resolving the concern

## 2026-05-05 (session 8 — ingest PARAGON-HF)

### Ingested
- raw/2019-NEJM-PARAGON-HF_study.pdf → [[solomon2019paragon]] (citekey: Solomon2019PARAGON)

### Updated pages
- wiki/sources/solomon2019paragon.md — full rewrite from PDF; added complete Table 1 baseline, Table 2 outcomes with exact rates, full subgroup forest plot (12 prespecified), safety Table 3, statistical design details (dual run-in, adjusted alpha 0.048), 26-patient GCP exclusion
- wiki/citations.md — Solomon2019PARAGON promoted from Stub to Ingested

### Key new data vs. stub
- Renal protection: HR 0.50 (0.33–0.77) — significant; strongest secondary endpoint, underreported in HFpEF narrative
- NYHA improvement: OR 1.45 (1.13–1.86) — significant
- KCCQ NS (+1.0 pt, 0.0–2.1); both arms declined — important contrast with DELIVER
- Safety: paradoxically lower creatinine elevation and hyperkalemia despite active RAAS comparator
- Exact subgroup RRs: women 0.73 (0.59–0.90); LVEF ≤57%: 0.78 (0.64–0.95)

## 2026-05-05 (session 8 — ingest CHARM-Preserved)

### Ingested
- raw/2003-LANCET-Yusuf-CHARM-preserved_study.pdf → [[yusuf2003charm]] (citekey: Yusuf2003CHARM)

### Updated pages
- wiki/sources/yusuf2003charm.md — full rewrite from PDF; added complete Table 1 baseline (N=3,023, mean age 67.2y, LVEF 54%, 65% HTN, 29% AF, only 20% ACEi), Tables 2+3+4 (unadjusted HR 0.89 P=0.118; adjusted P=0.051; adjudicated HF hosp adjusted P=0.047; investigator-reported P=0.017/P=0.014; new-onset diabetes HR 0.60 P=0.005), safety discontinuations, baseline imbalance note, mid-trial ACEi protocol change
- wiki/citations.md — Yusuf2003CHARM promoted from Stub to Ingested; duplicate Solomon2019PARAGON removed from Stub refs section

### Key new data vs. stub
- New-onset diabetes: HR 0.60 (0.41–0.86), P=0.005 — 40% reduction; stronger result than primary efficacy endpoint
- Investigator-reported total HF admissions: 402 vs. 566, P=0.014 — counts diverge markedly from adjudicated
- Baseline imbalance: candesartan arm had more adverse prognostic factors (more MI, stroke, diabetes) — modest bias against treatment effect
- Mid-trial ACEi protocol change after HOPE publication introduces heterogeneity in background RAAS exposure

## 2026-05-05 (session 8 — ingest I-PRESERVE)

### Ingested
- raw/2008-NEJM-Massie-I-PRESERVE_study.pdf → [[massie2008ipreserve]] (citekey: Massie2008IPreserve)

### Updated pages
- wiki/sources/massie2008ipreserve.md — full rewrite from PDF; added complete Table 1 baseline (N=4,128, mean age 72y, LVEF 59–60%, 76% NYHA III, 88% HTN, 29% AF, median NT-proBNP 320/360, eGFR 72–73), Tables 2+3 outcomes with exact rates, Figure 2 subgroup (8/8 zero heterogeneity), Table 4 safety, concomitant RAAS background change during trial
- wiki/citations.md — Massie2008IPreserve promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub
- All-cause death: HR 1.00 (0.88–1.14), P=0.98 — exact CI and P now recorded
- Zero heterogeneity across all 8 prespecified subgroups — cleanest null in RAAS-HFpEF; contrast with PARAGON sex/LVEF signals
- NT-proBNP change NS (P=0.14): no biomarker effect despite 3.8 mmHg BP reduction
- MLHF QoL NS (P=0.85): neutral on symptoms
- Safety: creatinine doubling 6% vs. 4% P<0.001; K >6.0 3% vs. 2% P=0.01
- ACEi use rose 25% → 39%, spironolactone 15% → 28% during trial — progressive RAAS background dilution
- LVEF 59–60% (highest among early RAAS trials) — most representative of true HFpEF

### Trials-pending
- No new post-2020 HFpEF-important trials identified in I-PRESERVE references

## 2026-05-05 (session 8 — ingest CAPACITY-HFpEF)

### Ingested
- raw/2020-JAMA-Udelson-CAPACITY-HFpEF_study.pdf → [[udelson2020capacity]] (citekey: Udelson2020CAPACITY)

### Updated pages
- wiki/sources/udelson2020capacity.md — full rewrite from PDF; added complete Table 1 baseline (N=196, primary analysis n=143, median NT-proBNP 244 pg/mL, 57% ≤300, LVEF median 61.5%, BMI 34, 19% diuretics), Table 2 primary and secondary outcomes with exact CIs, exploratory KCCQ/6-MWT responder analyses, Figure 2 subgroup forest plot, Table 3 safety
- wiki/citations.md — Udelson2020CAPACITY promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub
- KCCQ worse: −7.2 [−12.3 to −2.0], P=0.007 — exact CI; KCCQ responders OR 0.43, P=0.01
- 6-MWT responders fewer on drug: OR 0.39, P=0.007 — significant harm signal on responder analysis
- Age interaction P=0.004: harm in ≥70y (adjusted diff −1.22 [−2.44 to −0.46]) — enrichment criterion group harmed
- Loop diuretic only 19% (vs. 52-93% in major trials) — very different population
- Median NT-proBNP 244 pg/mL; 57% below modern HFpEF NP entry thresholds — diagnostic uncertainty
- BP lowered −6.3 mmHg; dizziness 9.9% vs. 1.1%, hypotension 8.8% vs. 0% — likely mechanism for harm in elderly

### Trials-pending
- No new post-2020 HFpEF-important trials identified in CAPACITY-HFpEF references

## 2026-05-05 (session 8 — ingest VITALITY-HFpEF)

### Ingested
- raw/2020-JAMA-Armstrong-VITALITY-HFpEF.pdf → [[armstrong2020vitality]] (citekey: Armstrong2020VITALITY)

### Updated pages
- wiki/sources/armstrong2020vitality.md — full rewrite from PDF; added complete Table 1 baseline (N=789, LVEF 56.8%, median NT-proBNP 1364–1644 pg/mL, 86% loop diuretics, 86% beta-blockers, 45% MRA, 36% AF, eGFR 57–62), primary/secondary outcomes with exact CIs, Table 2 safety+clinical outcomes, titration details, placebo response analysis
- wiki/citations.md — Armstrong2020VITALITY promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub
- KCCQ-PLS: LS diff −1.5 [−5.5 to 2.5] P=0.47 (15mg); −0.5 [−4.6 to 3.5] P=0.80 (10mg) — exact CIs
- 6MWD: −5.5 m [−19.7 to 8.8] P=0.45; −1.8 m [−16.2 to 12.6] P=0.81 — exact CIs
- Placebo response +6.9 KCCQ PLS pts (exceeds MCID of 5 pts) — natural post-decompensation recovery; all 3 arms improved meaningfully
- Mortality signal: CV death 3.0%/4.6%/1.5% for 15mg/10mg/placebo — numerically more in 10mg; trial not powered
- SBP reduced −3.1/−3.8/−1.2 mmHg; symptomatic hypotension 6.4% vs. 3.4%
- Median NT-proBNP ~1400 pg/mL — starkly different from CAPACITY-HFpEF (244 pg/mL); very different severity populations

### Trials-pending
- No new post-2020 HFpEF-important trials identified in VITALITY-HFpEF references (VICTORIA already in pending)

## 2026-05-05 (session 8 — ingest PARADIGM-HF)

### Ingested
- raw/2014-NEJM-McMurray-PARADIGM-HF_study.pdf → [[mcmurray2014paradigm]] (citekey: McMurray2014PARADIGM)

### Updated pages
- wiki/sources/mcmurray2014paradigm.md — full rewrite from stub; added complete Table 1 baseline (N=8,442, LVEF 29.6%, 21% female, median NT-proBNP 1631, 93% beta-blocker, 54% MRA), Table 2 outcomes (primary HR 0.80, CV death HR 0.80, all-cause HR 0.84, KCCQ +1.64 P=0.001), Table 3 safety (paradoxically lower creatinine + hyperkalemia, more hypotension), subgroup forest plot, dual run-in design, early stopping context
- wiki/citations.md — McMurray2014PARADIGM promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub (stub was all placeholders)
- Primary HR 0.80 (0.73–0.87) P<0.001; exact P=4.0×10⁻⁷
- All-cause death HR 0.84 (0.76–0.93) P<0.001 — mortality benefit confirmed
- KCCQ clinical summary +1.64 pts [0.63–2.65] P=0.001 — significant symptom benefit; EF-contrast with PARAGON NS
- Safety paradox: creatinine ≥2.5 3.3% vs. 4.5% P=0.007; K>6.0 4.3% vs. 5.6% P=0.007 — same renal paradox pattern as PARAGON
- Run-in details: 18% screened patients excluded; 1,102 enalapril + 977 LCZ696 run-in dropouts
- Early stopping: 3rd interim analysis March 28, 2014; stopping boundary P<0.001 crossed

### Trials-pending
- No new post-2020 HFpEF-important trials identified in PARADIGM-HF references

## 2026-05-05 (session 8 — ingest DAPA-HF)

### Ingested
- raw/2019-NEJM-McMurray-DAPA-HF_study.pdf → [[mcmurray2019dapahf]] (citekey: McMurray2019DAPAHF)

### Updated pages
- wiki/sources/mcmurray2019dapahf.md — full rewrite from stub; added complete Table 1 baseline with medications (MRA 71.5%, sacubitril-valsartan 10.5%, beta-blocker 96%), Table 2 primary+secondary outcomes with exact HRs and CIs, subgroup forest plot (all patients + 15 prespecified subgroups), laboratory changes at 8 months, Table 2 safety, non-DM subgroup analysis
- wiki/citations.md — McMurray2019DAPAHF promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub (stub was all placeholders)
- Primary HR 0.74 (0.65–0.85) P<0.001; 386 (16.3%) vs 502 (21.2%); NNT=21
- Non-DM HR 0.73 (0.60–0.88) consistent with DM HR 0.75 (0.63–0.90) — mechanism beyond glucose lowering established
- NYHA II HR 0.63 (0.52–0.75) vs NYHA III/IV HR 0.90 (0.74–1.09) — post-hoc apparent attenuation; inconsistent with other advanced-disease markers
- Sacubitril-valsartan 10.5% at baseline; HR 0.75 consistent in this subgroup
- Lab changes: creatinine +0.02 mg/dL (minimal); hematocrit +2.41% P<0.001; NT-proBNP −301 [−457 to −150] P<0.001; weight −0.87 kg P<0.001; SBP −1.27 mmHg P=0.002
- Safety: AE discontinuation identical (4.7% vs 4.9%); renal AEs fewer on dapa (6.5% vs 7.2% NS); DKA 3 vs 1 case; no amputation/Fournier's difference
- KCCQ total symptom score win ratio 1.18 (1.11–1.26) P<0.001

### Trials-pending
- EMPEROR-Preserved (Anker 2021) and DELIVER (Solomon 2022) already ingested; no new post-2020 HFpEF-important trials to add from DAPA-HF (2019 paper)

## 2026-05-05 (session 8 — ingest EMPEROR-Reduced)

### Ingested
- raw/2020-NEJM-Packer-EMPEROR-Reduced_study.pdf → [[packer2020emperor]] (citekey: Packer2020EMPEROR)

### Updated pages
- wiki/sources/packer2020emperor.md — full rewrite from stub; added complete Table 1 baseline (N=3,730, LVEF ≤30%: 71.8%, median NT-proBNP 1887, sacubitril-valsartan 18.3%, MRA 70.1%, ICD 31%), Table 2 outcomes with exact HRs and CIs, subgroup forest plot (Figure 2, 16 subgroups), eGFR slope analysis, discontinuation eGFR analysis, safety summary
- wiki/citations.md — Packer2020EMPEROR promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub (stub was all placeholders)
- Primary HR 0.75 (0.65–0.86) P<0.001; NNT=19; first HF hosp HR 0.69 (0.59–0.81)
- eGFR slope +1.73 (1.10–2.37) mL/min/1.73m²/yr P<0.001 — headline renal finding
- Composite renal outcome HR 0.50 (0.32–0.77) — same as PARAGON-HF
- CV death HR 0.92 NS; all-cause HR 0.92 NS — shorter follow-up than DAPA-HF
- LVEF >30% subgroup HR 0.99 (0.76–1.31) — possible EF-gradient even within HFrEF
- Sacubitril-valsartan at baseline HR 0.64 (0.45–0.89) vs no ARNi 0.77
- Discontinuation analysis confirms structural renal protection: eGFR −0.93 vs −4.21 mL/min/yr after drug stop
- Hematocrit +2.36% (2.08–2.63) — consistent with DAPA-HF (+2.41%)

### Trials-pending
- EMPEROR-Preserved (Anker 2021) already ingested; no new post-2020 HFpEF-important trials to add

## 2026-05-05 (session 8 — ingest INDIE-HFpEF)

### Ingested
- raw/2014-CirculationAHA-Zamani-Indie_Beetroot_HFpEF.pdf → [[zamani2015indie]] (citekey: Zamani2015INDIE)

### Updated pages
- wiki/sources/zamani2015indie.md — full rewrite from stub (multiple stub errors corrected); added complete Table 1 baseline (N=17 crossover, age 65.5y, 88% male, 82% Black, 100% HTN, 71% DM, 94% obese, LVEF 63.5%, E/e' 11.6, median NT-proBNP 144 pg/mL, 53% met ESC criteria), Table 2 gas exchange data, Table 3 haemodynamic reserve, NIRS and aortic tonometry results
- wiki/citations.md — Zamani2015INDIE added to Ingested table and formatted refs; removed from Stub formatted refs; also removed orphaned Solomon2022DELIVER duplicate from Stub formatted refs

### Stub errors corrected on ingest
- Journal: stub said "JACC: Heart Failure" → corrected to Circulation 2015;131(4):371–380
- Intervention: stub said "KNO₃" → corrected to beetroot juice NO₃⁻ 12.9 mmol (crossover, single dose)
- N: stub said ~65 → corrected to 17 (modified ITT)
- Design: stub said parallel RCT ~6 weeks → corrected to double-blind crossover, single dose, ≥5-day washout
- Key finding: stub said "did not improve peak VO₂" → corrected to POSITIVE peak VO₂ (P=0.005); primary (efficiency) was neutral (P=0.64)

### Key new data vs. stub
- Primary (efficiency): neutral P=0.64
- Peak VO₂: +1.0 mL/min/kg, P=0.005 — SIGNIFICANT (stub was wrong)
- Mechanism: peripheral hemodynamic (↑CO +32.5% P=0.006; ↓SVR −10.6% P=0.03), not O₂ extraction
- Aortic augmentation index: −9.1%, P=0.03 — reduced wave reflections
- Crossover confirms bioavailability: plasma NOₓ 326 vs 10 µmol/L P=0.0003

### Trials-pending
- No new post-2020 HFpEF-important trials identified in INDIE-HFpEF references

## 2026-05-05 (session 8 — ingest DIG-Preserved)

### Ingested
- raw/2006-CirculationAHA-Ahmed-DIG_HF.pdf → [[ahmed2006dig]] (citekey: Ahmed2006DIG)

### Updated pages
- wiki/sources/ahmed2006dig.md — full rewrite from stub; added complete Table 1 baseline (N=988, LVEF 55.4%, 86% ACEi, 77% diuretics, 57% HTN, 56% ischaemic, NYHA I/II/III/IV 20/58/21/1%), Table 2 mortality and composite outcomes at 2y and study end, Table 3 hospitalisations by cause, digoxin toxicity data, offsetting mechanism analysis
- wiki/citations.md — Ahmed2006DIG promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub (stub had all placeholders)
- Primary HR 0.82 (0.63–1.07) P=0.136 at study end (NS); but at 2y HR 0.71 (0.52–0.98) P=0.034 (significant — pre-specified)
- Mortality completely null: all-cause HR 0.99, CV HR 1.00
- Worsening HF hosp reduced: 2y HR 0.66 P=0.012; overall trend HR 0.79 P=0.094
- Unstable angina hosp increased: 2y HR 1.76 P=0.004; overall trend HR 1.37 P=0.061
- Digoxin toxicity: 48 (10%) vs 18 (4%) P<0.001 — important safety signal
- Net null explained by competing effects: HF reduction offset by angina increase

### Trials-pending
- No post-2020 HFpEF-important trials to add from a 2006 publication

## 2026-05-05 (session 8 — ingest MAGGIC)

### Ingested
- raw/2013-ESC-Pocock-MAGGIC_meta-analysis.pdf → [[pocock2013maggic]] (citekey: Pocock2013MAGGIC)

### Updated pages
- wiki/sources/pocock2013maggic.md — full rewrite from stub; added complete Table 2 (13 predictors with exact RRs and CIs), Table 5 (EF <40 subgroup, N=21,442), Table 6 (EF ≥40 subgroup, N=17,930 — ACEi/ARB RR 0.938 P=0.233 NS), Table 4 risk score calibration; design details (30 studies: 6 RCTs + 24 observational, IPD-MA, Poisson regression with study random effect), EF spline analysis (knot at 40%), heartfailurerisk.org integer score
- wiki/citations.md — Pocock2013MAGGIC promoted from Stub to Ingested; Stub table and Stub formatted refs section now empty (all stubs ingested)

### Key new data vs. stub (stub was all placeholders)
- Exact N: 39,372 patients; 15,851 deaths (40.2%); median follow-up 2.5y (IQR 1.0–3.9y)
- EF threshold confirmed at 40%: EF per 5% RR 0.581 up to 40%, then flat — HFpEF as distinct prognostic entity
- ACEi/ARB EF ≥40: RR 0.938 (0.864–1.019) P=0.233 — NOT significant; EF <40: RR 0.834 P<0.001 — significant
- Age RR 1.589/decade in EF ≥40 (> EF <40 RR 1.407) — age dominant predictor in HFpEF
- Diabetes RR 1.513 in EF ≥40 (> EF <40 RR 1.354) — cardiometabolic burden more harmful in HFpEF
- Integer score calibration: score 20 → 25% 3y mortality; score 30 → 52%; score 33+ → 70%

### Trials-pending
- 2013 meta-analysis; no post-2020 HFpEF-important trials to add

## 2026-05-05 (session 8 — ingest Yi 2025 AI review)

### Ingested
- raw/2025-jjcc-Yi-AI_in_HFpEF.pdf → [[yi2025ai]] (citekey: Yi2025AI)

### New pages created
- wiki/sources/yi2025ai.md — new source page; review article using source template
- wiki/concepts/ml-ai-hfpef.md — new concept page; ML/AI in HFpEF; 4 domains (diagnosis, phenotyping, risk prediction, management); history from 2015 to 2025; open questions

### Key content from review (38 studies, Yi & Cho 2025, J Cardiol 87:113–120)
- ECG deep learning: AUC 0.87 (Unterhuber/Kwon); NPV 0.98 — scalable rule-out
- Echo 3D-CNN (Akerman): AUC 0.79; single A4C clip; outperforms HFA-PEFF/H₂FPEF
- NLP/EHR: 75.4% of ESC-criteria HFpEF patients undiagnosed in routine EHR (Garan 2023)
- Phenotyping: 11 studies; 3–4 phenogroups consistent across datasets; cardiometabolic/inflammatory/ischaemic/age-AF axes
- Spironolactone responders (Kresoja 2023; Desai 2024): ML predicts responders; BMI top predictor (33.7%); non-responders show no benefit (P=0.52 vs P=0.008) — TOPCAT reframed as enrichment failure
- In silico empagliflozin mechanism: NHE1 inhibition → cardiomyocyte oxidative stress (Bayes-Genis 2021)

### Citations updated
- wiki/citations.md — Yi2025AI added to Ingested table and formatted refs (new entry; no prior stub)

### Trials-pending
- No post-2020 HFpEF RCTs identified as missing from wiki; Aldo-DHF referenced but 2013 (pre-cutoff)

## 2026-05-06 (session 8 — ingest Kittleson 2023 ACC ECDP)

### Ingested
- raw/2023-JACC-Kittleson-ACC_expert_consensu_HFpEF.pdf → [[kittleson2023acc]] (citekey: Kittleson2023ACC)

### New pages created
- wiki/sources/kittleson2023acc.md — new source page; guideline/consensus document using source template; 44-page ACC ECDP; full treatment algorithm, dose tables, contraindication tables, mimics table, comorbidity management, referral acronyms

### Updated pages
- wiki/concepts/guideline-comparison.md — added ACC 2023 ECDP section; updated History section; added sex-stratified algorithm table; H₂FPEF vs. HFA-PEFF priority clarification; updated sources frontmatter
- wiki/trials-pending.md — added SUMMIT (NCT04847557, semaglutide in HFpEF) and STEP-HFpEF (NCT04788511, tirzepatide in HFpEF)
- wiki/citations.md — Kittleson2023ACC added to Ingested table and formatted refs
- wiki/index.md — added [[kittleson2023acc]] under new "Guidelines and Consensus Documents" section

### Key content vs. existing wiki
- Treatment algorithm (Figure 9): SGLT2i first (near-Class I) → MRA for women (all EF) + men EF <55–60% → ARNI same criteria → ARB for ARNI-ineligible
- Sex-stratified recommendation: PARAGON HR 0.73 women vs. 1.03 men; LVEF 50–55% may be abnormal in women (smaller LV)
- Table 3: dose targets — dapa/empa 10mg; spiro 25→50mg; sac/val 24/26→97/103mg BID; cand 4–8→32mg
- Table 1: HFpEF mimics — 8 mimics with clinical clues + diagnostic tests (amyloidosis CTS/lumbar → Tc-PYP; Fabry → α-galactosidase; sarcoidosis → FDG-PET+CMR)
- CHECK-IN (PCP→cardiology) + INHALE (cardiology→HF specialist) acronyms
- GLP-1RA: semaglutide and tirzepatide referenced; SUMMIT + STEP-HFpEF ongoing
- STRONG-HF: 8% absolute reduction HF readmission/death with in-hospital GDMT titration
- CardioMEMS Class 2b; GUIDE-HF COVID-confounded; useful subset defined
- Comorbidity management: TZDs contraindicated; saxagliptin/alogliptin avoided; finerenone for diabetic CKD; thiazide + loop for CKD diuretic resistance

### Trials-pending added
- SUMMIT (NCT04847557): semaglutide in HFpEF with obesity
- STEP-HFpEF (NCT04788511): tirzepatide in HFpEF with obesity

## 2026-05-06 (session 9 — ingest Anker 2023 HFA/ESC/ESH HFpEF Phenotyping Statement)

### Ingested
- raw/2023-ESC-Anker_HFpEF_phenotyping.pdf → [[anker2023hfpefphenotype]] (citekey: Anker2023HFpEFPhenotype)

### New pages created
- wiki/sources/anker2023hfpefphenotype.md — new source page; 20-page HFA/ESC/ESH scientific statement; phenotype prevalence wheel (Figure 1, 18 phenotypes), treatment wheel (Figure 2), phenotype-specific evidence sections, ongoing trials
- wiki/concepts/hfpef-phenotype-profiling.md — new concept page; two-layer treatment model; phenotype-guided add-on table; LVEF 50–55% and >65% subgroup data; CMD prevalence; cancer HFpEF; ongoing trials table

### Updated pages
- wiki/entities/hfpef.md — added Comorbidity Phenotype Prevalences section (Figure 1 table, 18 phenotypes with prevalences); added [[hfpef-phenotype-profiling]] to Related Pages; added Anker2023HFpEFPhenotype to sources
- wiki/entities/atrial-fibrillation.md — added AF prevalence up to 50% (paroxysmal); EAST-AFNET4 data; CABA-HFpEF (NCT05508256, Phase III, DZHK); atrial FMR combined phenotype; updated Related Pages + sources
- wiki/entities/spironolactone.md — added ESC/HFA 2023 "may be considered" framing; SPIRIT-HF (NCT04727073) and SPIRRIT (NCT02901184) ongoing; FINEARTS-HF (NCT04435626, finerenone) first non-steroidal MRA trial; updated Related Pages + sources
- wiki/concepts/hfpef-treatment-gap.md — added "Phenotype-Based Approach" section with two-layer model and ongoing trials table (FINEARTS-HF, SUMMIT, STEP-HFpEF, SPIRIT-HF, CABA-HFpEF, FAIR-HFpEF); updated Related Pages + sources

### Key content vs. existing wiki
- Figure 1: First structured prevalence data for 18 HFpEF comorbidity phenotypes; iron deficiency 50–75% most underrecognised
- Figure 2: Treatment wheel — phenotype-specific add-on agents for 7 comorbidity categories
- Iron deficiency 50–75%; VO2 reduction, 6MWD reduction, HRQOL impairment; FAIR-HFpEF/PREFER-HF ongoing
- CMD: PROMIS-HFpEF 66% endothelium-independent + 24% endothelium-dependent = 91% total
- LVEF 50–55%: distinct subgroup; spironolactone benefit (TOPCAT), sacubitril/valsartan benefit (PARAGON ≤57%), empagliflozin benefit (EMPEROR ≥50% to <64%)
- LVEF >65%: U-shaped mortality; secondary HFpEF workup mandatory (ATTR 13% with LVH)
- Cancer HFpEF: doxorubicin → diastolic dysfunction 60% at 1y, 80% at 3y; excluded from all major trials
- Chronotropic incompetence: beta-blocker withdrawal improves function — contra-intuitive but documented
- CABA-HFpEF (NCT05508256): Phase III AF ablation vs. rate control in HFpEF; DZHK network

### Citations updated
- wiki/citations.md — Anker2023HFpEFPhenotype added to Ingested table and formatted refs

### Trials-pending added
- FINEARTS-HF (NCT04435626): finerenone (non-steroidal MRA) in HFpEF, LVEF ≥40%
- CABA-HFpEF (NCT05508256): catheter ablation vs. rate control in HFpEF with AF; DZHK Phase III
- FAIR-HFpEF (NCT03074591): ferric carboxymaltose vs. placebo in HFpEF with iron deficiency
- SPIRIT-HF (NCT04727073): spironolactone in HFpEF; resolves TOPCAT MRA question

## 2026-05-06 (session 9 — ingest Savarese 2022 global HF burden)

### Ingested
- raw/2022-ESC-Savarese-Global_burden_HF.pdf → [[savarese2022globalburden]] (citekey: Savarese2022GlobalBurden)

### New pages created
- wiki/sources/savarese2022globalburden.md — new source page; global HF epidemiology invited review (Cardiovasc Res 2022); prevalence, incidence, aetiology, outcomes, hospitalisations, costs by EF phenotype; 7-registry distribution table; Figure 1/2/3/4 data

### Updated pages
- wiki/entities/hfpef.md — Epidemiology section updated: HFpEF fraction 16–47% by registry; 5-year mortality comparable to HFrEF (75.7%); non-CV mortality 30.7% vs 20.1% in HFrEF; 63% non-CV hospitalisations; sources + Related Pages updated
- wiki/entities/hfmref.md — added Epidemiology section: HFmrEF 14–24% across 5 registries; 1-year mortality 7.6%; sources + Related Pages updated
- wiki/concepts/hf-phenotype-classification.md — added 7-registry EF phenotype distribution table; sources + Related Pages updated

### Key content vs. existing wiki
- First structured epidemiological data for the wiki; existing pages had [needs source] placeholders
- HFpEF 16–47% range explained by registry setting, region, diagnostic criteria
- 5-year mortality paradox: lower 1-year CV mortality in HFpEF offset by higher non-CV mortality → comparable 5-year outcomes
- IHD 32% in HFpEF vs. 56–60% in HFrEF (Swedish HF registry) — mechanistically distinct aetiology profile
- Valvular disease 20% of HFpEF vs. 4% HFrEF (ESC-HF-LT)
- Costs: Germany €25,532/year highest; HFpEF driving disproportionate future cost increases

### Citations updated
- wiki/citations.md — Savarese2022GlobalBurden added to Ingested table and formatted refs

### Trials-pending
- No post-2020 HFpEF clinical trials to add (epidemiology review)

## 2026-05-06 (session 10 — ingest Pfeffer 2019 HFpEF perspective)

### Ingested
- raw/2019-CIRCRESAHA-Pfeffer-HFpEF_perspective.pdf → [[pfeffer2019hfpef]] (citekey: Pfeffer2019HFpEF)

### New pages created
- wiki/sources/pfeffer2019hfpef.md — new source page; invited Circ Res perspective; pathophysiologic cascade (Figure 2); cGMP/PKG paradigm; titin; ATTR 13–19% prevalence; therapeutic landscape 2019; CHAMPION trial; SECRET trial; prevention evidence; PEP-CHF

### Updated pages
- wiki/entities/hfpef.md — added cGMP/PKG cellular mechanism paragraph; titin; ATTR 13–19% prevalence + tafamidis/SPECT screening; Pfeffer2019HFpEF to sources
- wiki/concepts/hfpef-treatment-gap.md — added PEP-CHF to failed trials table (HR 0.92, P=0.55); added CHAMPION trial section (haemodynamic monitoring reduces HF hosp in HFpEF); Pfeffer2019HFpEF to sources
- wiki/concepts/exercise-intolerance.md — added Kitzman 2010 first RCT note; SECRET trial (exercise + caloric restriction, additive benefit); systemic microvascular dysfunction mechanism; Pfeffer2019HFpEF to sources
- wiki/concepts/hfpef-diagnosis.md — added 1990s–2000s history entry: 9 epidemiological definitions 1997–2015; CHARM-Preserved LVEF >40% threshold rationale; Pfeffer2019HFpEF to sources
- wiki/index.md — added [[pfeffer2019hfpef]] under Review Articles
- wiki/citations.md — Pfeffer2019HFpEF added to Ingested table and formatted refs

### Trials-pending added
- PEP-CHF (Cleland 2006): perindopril in HF LVEF >40%, elderly ≥70y; HR 0.92 neutral; historical RAAS trial
- REDUCE LAP-HF II (NCT03088033): interatrial shunt device in HFpEF; haemodynamic decompression via L→R shunt
- Minimally invasive pericardial modification (NCT03923673): device approach targeting extrinsic pericardial constraint in HFpEF

## 2026-05-06 (session 10 — ingest D'Amario 2019 CMD review)

### Ingested
- raw/2019-FPhys-D'Amario-Microvascular_Dysfunction.pdf → [[damario2019cmd]] (citekey: D'Amario2019CMD)

### New pages created
- wiki/sources/damario2019cmd.md — new source page; CMD as "common soil" paradigm; Figure 1 cascade (comorbidities→inflammation→EndoMT→HFpEF); titin N2BA→N2B isoform shift; EndoMT mechanism; calcium overload (late Na⁺/RALI-DHF); CMD measurement tools + 4-type classification; OSA RR 2.2; iron deficiency severity correlation; statins (JASPER); anti-IL-1/anakinra (D-HART); PDE-9; anti-fibrotic (nintedanib/pirfenidone); SGLT2i microvascular mechanism

### Updated pages
- wiki/concepts/diastolic-dysfunction.md — added Cellular Mechanisms section: cGMP/PKG detailed molecular pathway; titin N2BA→N2B isoform shift + hypophosphorylation; EndoMT (endothelial-mesenchymal transition as fibrosis driver); calcium overload via late Na⁺ current; History section extended (Paulus/Tschöpe 2013; Graziani/Crea 2018 CMD "common soil"); sources + Related Pages updated
- wiki/citations.md — D'Amario2019CMD added to Ingested table and formatted refs
- wiki/index.md — added [[damario2019cmd]] under Review Articles

### Key content vs. existing wiki
- EndoMT: first time captured in wiki; primary fibrosis driver; α-SMA/collagen I upregulation; TGF-β/SMAD; cardiomyocyte apoptosis via paracrine signalling
- Titin isoform shift (N2BA→N2B): distinction from mere "titin stiffness" — now mechanistically detailed
- CMD 4-type Camici/Crea classification: not previously in wiki
- OSA: RR 2.2 for HF admission (16.8% prevalence); treatment improves diastolic function
- Iron deficiency: diastolic dysfunction severity proportional to ID severity; absolute vs. functional ID distinction
- Statins: observational evidence for HFpEF benefit; endomyocardial biopsy data (↑PKG, ↓nitrotyrosine, ↓hypertrophy); JASPER study
- Ranolazine/RALI-DHF: calcium overload target; acute haemodynamic proof-of-concept (↓LVEDP/PCWP)
- Anti-fibrotic approaches: HFpEF-IPF shared mechanism; nintedanib/pirfenidone

### Trials-pending
- No post-2020 major HFpEF outcome trials to add (experimental agents are Phase 2 pre-outcome)

## 2026-05-06 (session 10 — comprehensive update of overview.md and timeline.md)

### Updated pages
- wiki/overview.md — full rewrite reflecting all 10 sessions; updated High-Level Summary (microvascular/EndoMT paradigm; two-layer treatment model); Key Concepts expanded (hfpef-phenotype-profiling, ml-ai-hfpef, diastolic-dysfunction cellular mechanisms added); Active Debates extended (CMD debate, statins, diagnostic algorithm choice); Recent Additions through session 10; Knowledge Gaps updated and extended (FINEARTS-HF, SUMMIT/STEP-HFpEF, CABA-HFpEF, CMD targeting, EndoMT, statins RCT, iron deficiency, cancer HFpEF)
- wiki/timeline.md — added Epidemiology section (Savarese 2022; Anker 2023 comorbidity prevalences); Pathophysiology timeline: filled [needs source] entries; added 2013 (Paulus/Tschöpe cGMP/PKG), 2018 (Graziani/Crea CMD "common soil"), 2019 (EndoMT + titin isoform shift + calcium overload); Treatment timeline: added 2010 (Kitzman first exercise RCT), 2017 (AHA/ACC Class IIb ARB/MRA), 2023 (Anker HFA/ESC two-layer model + ACC 2023 ECDP); Landmark Trials: added PEP-CHF (2006); AI/ML section: populated with Yi 2025 data (ECG-AI, NLP, phenotyping, TOPCAT responder prediction)
