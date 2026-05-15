---
type: study
title: "Phenomapping for Novel Classification of Heart Failure With Preserved Ejection Fraction"
citekey: Shah2015Phenomapping
year: 2015
authors: "Shah SJ, Katz DH, Selvaraj S, Burke MA, Yancy CW, Gheorghiade M, Bonow RO, Huang CC, Deo RC"
journal: "Circulation"
study_type: observational
evidence_level: moderate
tags:
  - ml-ai
  - hfpef
  - phenotyping
  - cluster-analysis
  - machine-learning
  - prognosis
  - heterogeneity
created: 2026-05-12
last_updated: 2026-05-13
sources:
  - file: raw/2014-CirculationAHA-Shah-Phenomapping.pdf
    citekey: Shah2015Phenomapping
---
# Shah et al. 2015 — HFpEF Phenomapping

> Unsupervised ML phenomapping of 397 HFpEF patients identified 3 mutually exclusive phenogroups with distinct clinical profiles and outcomes; phenogroup 3 (oldest, cardiorenal, RV dysfunction) had HR 4.2 (95% CI 2.0–9.1) for the combined outcome of CV hospitalisation or death (P<0.001) and HR 4.8 (95% CI 2.4–9.6) for HF hospitalisation alone vs. phenogroup 1; prognostic information validated prospectively in 107 independent patients.

**File:** `raw/2014-CirculationAHA-Shah-Phenomapping.pdf` · **Authors:** Sanjiv J. Shah, Daniel H. Katz, Senthil Selvaraj, Michael A. Burke, Clyde W. Yancy, Mihai Gheorghiade, Robert O. Bonow, Chiang-Ching Huang, Rahul C. Deo · **Year:** 2015 · **Journal:** *Circulation* 2015;131:269–279 · **DOI:** 10.1161/CIRCULATIONAHA.114.010637  
**Study type:** Prospective observational cohort + unsupervised ML analysis · **N:** 397 derivation; 107 validation · **Population:** HFpEF (LVEF ≥50%, grade ≥2 diastolic dysfunction or elevated BNP >100 pg/mL or invasive elevated PCWP); enrolled post-hospitalisation from Northwestern HFpEF outpatient programme · **Follow-up:** Continuous (death/Social Security Death Index query; HF hospitalisations tracked every 6 months) · **NCT:** NCT01030991 · **Period:** March 2008 – May 2011 (derivation); January 2012 – February 2014 (validation)

---

## Key Findings

- HFpEF is demonstrably heterogeneous: hierarchical clustering of 67 phenotypic variables reveals no single common pathophysiological profile
- ML model-based clustering identifies **3 optimal phenogroups** (Bayesian information criterion minimum at 3 clusters)
- Phenogroups have step-wise increasing risk: phenogroup 1 < 2 < 3
- **Phenogroup 3** (oldest/cardiorenal/advanced remodeling): unadjusted HR for HF hospitalisation 4.8 (95% CI 2.4–9.6; P<0.001) and for CV hospitalisation or death 4.2 (95% CI 2.0–9.1; P<0.001) vs. phenogroup 1; adjusted HR for combined CV outcome 3.3 (1.1–9.5; P=0.026) after adjusting for BNP and MAGGIC score
- Phenogroup assignment provides prognostic information **above and beyond** BNP and MAGGIC score (LRT, NRI, IDI all positive)
- SVM supervised learning: AUC 0.70–0.76 for combined outcome prediction in validation cohort

## Methods (brief)

**Population:** 420 patients enrolled from Northwestern HFpEF Program; 23 excluded (incomplete data); 397 in derivation analysis

**HFpEF diagnosis criteria:**
- LVEF ≥50% + prior hospitalisation for symptomatic HF
- + at least one of: echocardiographic grade ≥2 diastolic dysfunction; invasive evidence of elevated LV filling pressures; BNP >100 pg/mL
- No history of LVEF <40%; no constrictive pericarditis; no significant ischemic/valvular disease

**Phenomapping approach:**
1. Collected 67 continuous phenotypic variables (demographics, physical, labs, ECG, echocardiography, invasive hemodynamics for 216/397 patients)
2. Hierarchical clustering of variables (Pearson correlation; r>0.6 filtered) → 46 variables retained
3. Penalised model-based clustering (mclust R package; Bayesian information criterion) → optimal N=3 clusters
4. Validation: 107 additional patients enrolled prospectively; phenogroup assigned using trained model; outcomes re-analyzed with same Cox models

**Variable domains (Table 1):**
- Demographics, physical characteristics (BMI, HR, BP, pulse pressure)
- Laboratory (Na, K, BUN, creatinine, eGFR, glucose, Hgb, Plt, WBC, BNP*)
- ECG (PR, QRS duration, QTc, QRS axis, QRS-T angle*)
- Echocardiography — LV structure, systolic function (LVEF, Vcf, TAPSE), diastolic function (E, A, E/A*, e', E/e'*, IVRT), RV structure+function, right heart
- Hemodynamics (SV, CO, Ees, Ea, VA coupling, PCWP, PASP, RA pressure)
*Variables used in final 46-variable set after filtering

**Supervised learning:** SVM (support vector machine) with radial and sigmoid kernel; 46 phenotypic predictors; evaluated on validation cohort (AUC)

**Baseline characteristics (derivation cohort):**
- Mean age 65±12y; 62% female; 39% Black; mean LVEF 61±7%
- Mean E/e': 17±9; PCWP 23±9 mm Hg (n=216)
- Median BNP: 234 (IQR 86–530) pg/mL
- NYHA III/IV: 48%; 75% with grade ≥2 diastolic dysfunction; 34±14 mL/m² mean LAVi

## Results

### 3 Phenogroup Profiles

| Characteristic | Phenogroup 1 (n=128) | Phenogroup 2 (n=120) | Phenogroup 3 (n=149) | P |
|---|---|---|---|---|
| Age, y | 60.7±13.6 | 65.7±11.3 | 67.3±13.1 | <0.001 |
| Female, % | 67 | 68 | 55 | 0.049 |
| BMI, kg/m² | 31.2±7.3 | 37.0±10.7 | 28.9±7.4 | <0.001 |
| Obesity, % | 65 | 84 | 37 | <0.001 |
| T2DM, % | 9 | 52 | 34 | <0.001 |
| OSA, % | 35 | 60 | 31 | <0.001 |
| CKD, % | 6 | 34 | 53 | <0.001 |
| AF, % | 13 | 22 | 43 | <0.001 |
| Hypertension, % | 66 | 90 | 75 | <0.001 |
| eGFR, mL/min | 79.5±21.2 | 53.8±17.6 | 43.9±27.3 | <0.001 |
| Creatinine, mg/dL | 0.9±0.2 | 1.3±0.4 | 2.3±2.2 | <0.001 |
| BNP, pg/mL (median) | 72 (26–161) | 188 (83–300) | 607 (329–1138) | <0.001 |
| MAGGIC risk score | 15.6±6.7 | 19.8±5.8 | 22.8±7.5 | <0.001 |
| LV mass index, g/m² | 89.1±22.6 | 96.4±26.3 | 122.0±47.3 | <0.001 |
| LA volume index, mL/m² | 29.1±11.1 | 31.5±10.6 | 40.9±16.7 | <0.001 |
| e' velocity, cm/s (tissue Doppler) | 9.3±3.2 | 7.5±2.1 | 7.9±3.4 | <0.001 |
| E/e' | 11.2±3.7 | 15.2±6.4 | 18.6±10.6 | <0.001 |
| Diastolic dysfunction grade III–IV, % | 18 | 26 | 56 | <0.001 |
| PASP, mm Hg | 35.3±9.7 | 43.5±14.6 | 51.2±16.3 | <0.001 |
| RV basal diameter, cm | 3.6±0.6 | 3.8±0.5 | 4.2±0.8 | <0.001 |
| PCWP (n=216), mm Hg | 19.9±9.3 | 24.6±8.3 | 23.7±9.7 | 0.002 |
| QRS duration, ms | 93.8±21.0 | 91.3±13.6 | 112.7±33.3 | <0.001 |
| QRS-T angle, degrees | 42.6±41.7 | 53.4±44.0 | 86.6±54.0 | <0.001 |

### Phenogroup Archetypes

**Phenogroup 1 — "Young/Mild"**  
Youngest (60.7y); predominantly female; normal BMI for HFpEF; low BNP (72 pg/mL); mildest diastolic dysfunction; lowest hemodynamic derangement; normal GFR; low MAGGIC score; lowest risk. Preserved cardiac architecture and e' velocity.

**Phenogroup 2 — "Obese/Metabolic/Atrial"**  
Intermediate age; highest obesity (84%); highest T2DM (52%); highest OSA (60%); worst LV relaxation (lowest e' 7.5 cm/s); highest PVR; moderate-high BNP (188 pg/mL); moderate CKD. Pulmonary vascular involvement prominent. Corresponds to the obesity/metabolic phenotype targeted by GLP-1RA (STEP-HFpEF, SUMMIT).

**Phenogroup 3 — "Cardiorenal/Advanced Remodeling"**  
Oldest (67.3y); highest CKD (53%); highest AF (43%); highest BNP (607 pg/mL); worst ECG remodeling (longest QRS, highest QRS-T angle); highest LV mass index; worst RV function (RVFAC, TAPSE, RV wall thickness all worst); highest MAGGIC score; highest risk. Cardiorenal axis + advanced structural remodeling.

### Outcomes (Derivation Cohort)

| Outcome | PG1 events n(%) | PG2 events n(%) | PG3 events n(%) | HR PG3 vs. PG1 (unadjusted) | HR PG3 vs. PG1 (adj for BNP+MAGGIC) |
|---|---|---|---|---|---|
| CV hospitalisation | 22 (17) | 41 (34) | 71 (48) | 3.9 (2.4–6.3)† | 4.0 (2.3–6.8)† |
| HF hospitalisation | 10 (8) | 36 (30) | 52 (35) | 4.8 (2.4–9.6)† | 4.2 (2.0–9.1)† |
| Death | 5 (4) | 18 (15) | 36 (24) | 6.5 (2.5–16.6)† | 4.0 (1.5–10.6)† |
| Combined end point | 23 (18) | 54 (45) | 84 (56) | 4.4 (2.8–7.0)† | 4.1 (2.5–6.8)† |

†P<0.001 vs. phenogroup 1. Model 1: adjusted for BNP. Model 2: adjusted for BNP + MAGGIC score.

### Validation Cohort (N=107)
Phenogroup assignment: PG1 37 (34.6%), PG2 29 (27.1%), PG3 41 (38.3%)
- Step-wise outcome difference confirmed in validation cohort
- Combined endpoint (CV hospitalisation, HF hospitalisation, or death): PG3 vs. PG1 unadjusted HR 3.6 (95% CI 1.6–8.4; P=0.003); adjusted HR (BNP+MAGGIC) 3.3 (95% CI 1.1–9.5; P=0.026)
- Phenogroup assignment provides prognostic information beyond BNP + MAGGIC (NRI, IDI, LRT all positive)

### SVM Supervised Learning
- AUC 0.70–0.76 for combined outcome prediction in validation cohort

## Limitations

- Single-centre study (Northwestern HFpEF Program); population enriched for hospitalised, post-discharge patients — not community-based
- 39% Black patients — unusually high Black representation for HFpEF trial; limits generalisability to other populations
- BNP >100 pg/mL as one of three diagnostic options — may include compensated HFpEF or non-HF dyspnea
- Invasive hemodynamics only in 54% (216/397) — PCWP available only in subset
- Short follow-up (median not specified); limited event count for validation outcome analyses
- 3 phenogroups a parsimonious but arbitrary boundary — BIC also showed lower values at 8 clusters; clinical utility drove choice of 3
- Features available in clinical practice? Many variables from invasive hemodynamics or specialised echo — not routinely obtainable
- No treatment interaction analysis (does phenogroup moderate treatment response?) — not powered for this

## Connections

- Foundational source for: [[hfpef-phenotype-profiling]] — first ML-derived phenomapping; 3 phenogroup framework
- Foundational source for: [[ml-ai-hfpef]] — first application of unsupervised ML to HFpEF classification
- Supports: [[hfpef]] — confirms HFpEF is heterogeneous; 3 distinct pathophysiological profiles
- Precursor to: [[step-hfpef]] — phenogroup 2 (obese/metabolic) = GLP-1RA target subphenotype
- Precursor to: [[anker2023hfpefphenotype]] — 18-comorbidity phenotyping framework builds on this 3-phenogroup concept
- Related: [[hfpef-diagnostic-definitions]] — phenogroup membership provides prognostic info beyond definitional criteria

## Secondary Analyses & Data Reuse

| Citekey | Focus | Wiki page |
|---------|-------|-----------|
| — | Multiple Northwestern HFpEF Program analyses published subsequently | — |

## Related Pages

- Concepts: [[hfpef-phenotype-profiling]], [[ml-ai-hfpef]], [[hfpef-diagnostic-definitions]]
- Entities: [[hfpef]], [[step-hfpef]], [[summit]]
- Sources: [[anker2023hfpefphenotype]], [[yi2025ai]], [[kosiborod2023stephfpef]]

## Contradictions

No direct contradictions. Note: the 3-phenogroup classification has been replicated in other cohorts but the specific phenogroup assignments and boundaries vary by cohort. Whether phenogroup membership should guide treatment selection remains unproven in RCTs.
