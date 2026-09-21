---
title: Deep-Learning Models for the Echocardiographic Assessment of Diastolic Dysfunction
citekey: Pandey2021DeepNNEcho
year: 2021
authors: Pandey A, Kagiyama N, Yanamala N, Segar MW, Cho JS, Tokodi M, Sengupta PP
journal: JACC Cardiovascular Imaging
study_type: observational
evidence_level: moderate
tags:
- hfpef
- ml-ai
- diastolic-dysfunction
- echocardiography
- phenotype
- biomarker
created: 2026-05-12
last_updated: 2026-09-21
sources:
- citekey: Pandey2021DeepNNEcho
  doi: 10.1016/j.jcmg.2021.04.010
page-type: source-summary-page
---
# Deep-Learning Echocardiographic Assessment of Diastolic Dysfunction (Pandey 2021)

> A topological data analysis–based deep neural network using 9 echocardiographic variables classifies diastolic dysfunction severity better than ASE 2016 guidelines and identifies a high-risk HFpEF phenogroup in TOPCAT that derives differential benefit from spironolactone.

**Full citation:**
Pandey A, Kagiyama N, Yanamala N, Segar MW, Cho JS, Tokodi M, Sengupta PP. Deep-Learning Models for the Echocardiographic Assessment of Diastolic Dysfunction. *JACC Cardiovasc Imaging.* 2021;14(9):1887–1900. doi:[10.1016/j.jcmg.2021.04.010](https://doi.org/10.1016/j.jcmg.2021.04.010)
**Year:** 2021 · **Journal:** JACC Cardiovascular Imaging 2021;14(10):1887–1900 · **DOI:** 10.1016/j.jcmg.2021.04.010  
**Study type:** Multi-cohort observational model development + external validation  
**N:** Development cohort 1,242 (training n=990; internal validation n=252); hemodynamic validation 84; clinical outcome validation 219; TOPCAT echocardiography substudy 518; RELAX-HF/NEAT-HFpEF pooled cohort 346  
**Population:** Patients with echocardiographic diastolic assessment ± available invasive hemodynamic data (derivation/validation); TOPCAT participants (outcomes substudy); RELAX-HF and NEAT-HFpEF participants (biomarker/exercise substudy)  
**Follow-up:** TOPCAT median ~3.3 years; clinical outcome validation cohort median ~35 months  
**Primary outcome (model):** LVDD phenogroup classification (high-risk vs. low-risk); hemodynamic validation: AUROC for elevated LV filling pressure (>15 mmHg); TOPCAT substudy: composite all-cause death + HF hospitalisation

---

## Key Findings

- Internal validation (n=252): AUROC 0.988 (training set); AUROC 0.997 (accuracy 96.0%) in internal validation
- External hemodynamic cohort (N=84, overall including indeterminate): DeepNN AUC 0.88 vs. ASE 2016 AUC 0.67 (P=0.01); in classifiable-only subset (n=69): DeepNN AUC 0.894 vs. ASE 2016 AUC 0.829 (P=0.319, non-significant in classifiable subset but significant in overall)
- Most important variable: **e' velocity** (septal or lateral) — highest feature importance; followed by E/e', LV mass index, EF, LAVi, TRV, E velocity, A velocity, E/A ratio
- Clinical outcome validation cohort (N=219): high-risk phenogroup HR 3.96 (95% CI 1.24–12.67; P=0.021) for composite all-cause death or HF hospitalisation vs. low-risk (log-rank P<0.0001)
- TOPCAT substudy (N=518): high-risk phenogroup HR 1.92 (95% CI 1.16–3.22; P=0.01) for composite endpoint vs. low-risk; 81.1% classified high-risk
- Spironolactone benefit confined to high-risk phenogroup: HR 0.65 (95% CI 0.46–0.90; P=0.01); no benefit in low-risk (HR ~1.13, P=0.80); no statistically significant interaction term
- High-risk phenogroup reclassifies 70–80% of Grade I or indeterminate LVDD patients (2016 ASE) into high-risk
- RELAX-HF/NEAT-HFpEF pooled cohort (N=346): high-risk group had higher troponin I, NT-proBNP, lower VO₂peak, worse MLHFQ
- Model publicly available at https://wvu-model.herokuapp.com

## Methods (brief)

**Step 1 — Similarity network:** Topological data analysis (TDA) applied to 9 echo variables (E velocity, A velocity, E/A ratio, e' septal, e' lateral, E/e' ratio, LAVI, LVEF, peak TR velocity, LVMI) to construct a patient similarity network (n=1,242). Patients assigned to TDA loop regions 1–2 (low-risk) or 3–4 (high-risk). Cloud-based automated ML platform (OptiML/BigML) used to train supervised DeepNN classifier.

**Step 2 — Supervised DeepNN:** TDA-derived phenogroup labels used to train DeepNN. Training cohort n=990; internal validation n=252. Reference standard: TDA-derived phenogroup (not ASE 2016 guideline directly). Model accessed via https://wvu-model.herokuapp.com.

**External hemodynamic validation (Step 1):** N=84 patients; RHC (n=25) or left heart catheterisation (n=59) for LV filling pressure; 63 underwent both. Reference = LV filling pressure >15 mmHg. Model AUC 0.894 vs. ASE 2016 AUC 0.829 (classifiable subset n=69, P=0.319); full cohort DeepNN 0.88 vs. 0.67 (P=0.011).

**Clinical outcome validation (Step 2):** N=219 prospectively recruited subjects; echo + follow-up for primary composite (all-cause death or HF hospitalisation). Cox models with/without GLS/PALS covariates.

**TOPCAT echocardiography substudy (Step 3):** N=518 with complete echo data (136 excluded for missing data). Cox models adjusted for age, sex, race, diabetes, country, enrolment stratum consistent with primary TOPCAT analysis. Additional model adjusted for MAGGIC risk score. Spironolactone×phenogroup interaction assessed.

**RELAX-HF/NEAT-HFpEF biomarker/exercise substudy (Step 4):** Pooled N=346 (NEAT n=110; RELAX n=216). Multivariate linear regression of phenogroup with troponin I, NT-proBNP, VO₂peak, MLHFQ score.

## Results

### Model Performance

| Cohort | N | AUC / AUROC | Accuracy | Comparator |
|--------|---|-------------|----------|-----------|
| Training set (internal) | 990 | 0.988 | 92.1% | — |
| Internal validation | 252 | 0.997 | 96.0% | — |
| External hemodynamic (classifiable, LV fill >15 mmHg) | 69 | 0.894 | — | ASE 2016: 0.829 (P=0.319) |
| External hemodynamic (full cohort, all including indeterminate) | 84 | 0.883 | — | ASE 2016: 0.676 (P=0.011) |

Note: DeepNN was significantly better than ASE 2016 in the full hemodynamic cohort (P=0.011) but not in the classifiable-only subset (P=0.319), because the largest incremental gain was in reclassifying indeterminate patients.

### Clinical Outcome Validation Cohort

| Group | HR (95% CI) | P | Outcome |
|-------|-------------|---|---------|
| High-risk vs. low-risk | 3.96 (1.24–12.67) | 0.021 | All-cause death or HF hospitalisation |
| High-risk vs. low-risk (LVEF >50%) | Significant | P=0.0005 | Same composite |

### TOPCAT Substudy Outcomes (N=518)

| Group | HR (95% CI) | P | vs. |
|-------|-------------|---|-----|
| High-risk phenogroup (vs. low-risk) | 1.92 (1.16–3.22) | 0.01 | Composite all-cause death + HF hosp |
| High-risk (MAGGIC-adjusted) | 2.10 (1.20–3.47) | 0.0003 | Low-risk |
| Spironolactone in high-risk | 0.65 (0.46–0.90) | 0.01 | Placebo, high-risk group |
| Spironolactone in low-risk | 1.13 (0.44–2.93) | 0.80 | Placebo, low-risk group |
| Interaction P-value | — | NS (not significant) | Phenogroup × treatment |

### Variable Importance (Feature Importance from DeepNN)

Rank order by model feature importance: e' velocity > E/e' ratio > LV mass index > EF > LAVi > TRV > E velocity > A velocity > E/A ratio. e' velocity (septal or lateral) is the single most discriminating parameter and the model accuracy drops substantially (~72–75%) when e' is excluded.

## Limitations

- TDA + DeepNN is a black-box architecture; clinical interpretability limited; heatmap/neuron-deactivation not applicable to this echo-based model
- Derivation cohort reference standard = TDA-derived phenogroup labels (unsupervised) — not externally validated hemodynamic reference in derivation
- Hemodynamic validation N=84 — small; single centre; 63/84 had both RHC and LHC on same day
- Clinical outcome validation cohort N=219 is prospective but single-institutional; primary endpoint is hospitalisation not adjudicated
- TOPCAT substudy is post-hoc, not pre-specified; phenogroup assignment retrospective; no statistically significant treatment × phenogroup interaction
- TOPCAT LVEF threshold (≥45%) lower than modern HFpEF definition (≥50%)
- TOPCAT Americas/Russia heterogeneity may confound substudy results
- DeepNN uses only 9 resting echo variables — does not capture exercise-unmasked LVDD, biomarkers, or extracardiac factors
- Web tool endpoint (wvu-model.herokuapp.com) may have availability limitations
- Model not validated in a prospective, independently powered HFpEF outcomes trial

## Connections
- Cited by: [[yi2025ai]] — added automatically from the reciprocal Cites: relationships recorded on those pages

- Supports: [[hfpef-phenotype-profiling]] — DeepNN identifies biologically distinct phenogroups with differential treatment response
- Supports: [[topcat]] — TOPCAT Americas analysis consistent with spironolactone benefit in sicker subgroup; extends Pitt 2014 analysis
- Supports: [[shah2015phenomapping]] — independent method (DeepNN vs. hierarchical clustering) converges on heterogeneous HFpEF phenogroups requiring personalised treatment
- Updates: [[diastolic-dysfunction]] — DeepNN classification outperforms ASE 2016 guideline for hemodynamic correlation
- Connects to: [[gao2025ecgdl]] — parallel approach using ECG instead of echo for HFpEF risk stratification
- Cites: [[redfield2015neat]], [[redfield2013relax]] — NEAT-HFpEF and RELAX named as NO/cGMP-pathway comparator context
- Cites: [[pocock2013maggic]] — MAGGIC risk score used as a comparator prognostic model to the DeepNN phenogroup classification
- Contradicts: one-size-fits-all pharmacological trial designs (spironolactone null in unselected; benefit in high-risk subgroup); see `wiki/contradictions.md`

## Secondary Analyses & Data Reuse

| Citekey | Focus | Wiki page |
|---------|-------|-----------|
| — | — | — |

## Related Pages

- Concepts: [[hfpef-phenotype-profiling]], [[diastolic-dysfunction]], [[exercise-intolerance]]
- Entities: [[topcat]], [[hfpef]]
- Sources: [[shah2015phenomapping]], [[pitt2014topcat]], [[gao2025ecgdl]]

## Contradictions

Spironolactone benefit only in high-risk phenogroup (Pandey 2021 TOPCAT substudy) vs. overall neutral TOPCAT result (Pitt 2014). Post-hoc subgroup; should be confirmed prospectively. Noted in `wiki/contradictions.md`.
