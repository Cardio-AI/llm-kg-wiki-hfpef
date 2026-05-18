---
type: study
title: "Boralkar 2019 — NLR and NLR Trajectory in Acute HFpEF (Stanford STRIDE)"
citekey: Boralkar2019NLR
year: 2019
authors: Boralkar KA, Kobayashi Y, Amsallem M, Arthur Ataam J, Moneghetti KJ, Cauwenberghs N, Horne BD, Knowlton KU, Maecker H, Kuznetsova T, Heidenreich PA, Haddad F
journal: Am J Cardiol
study_type: observational-retrospective
evidence_level: low-moderate
tags:
  - inflammation
  - biomarker
  - hfpef
  - acute-hf
  - prognosis
  - nlr
created: 2026-05-18
last_updated: 2026-05-18
sources:
  - file: raw/2019-AJCariol-Boralkar-lymphocyte_NLR_hospitalization_hfpef.pdf
    citekey: Boralkar2019NLR
---
# Boralkar 2019 — NLR and NLR Trajectory in Acute HFpEF (Stanford)

> In 443 patients hospitalized for acute HFpEF (Stanford STRIDE database), NLR on admission (HR 1.18; P=0.04) and absolute NLR trajectory from admission to discharge (HR 1.26; P=0.001) were independently predictive of all-cause mortality beyond the GWTG-HF risk score; NLR trajectory significantly improved AUC and reclassification at 1-, 2-, and 3-year follow-up.

**File:** `raw/2019-AJCariol-Boralkar-lymphocyte_NLR_hospitalization_hfpef.pdf`  
**Authors:** Boralkar KA, Kobayashi Y, Amsallem M, et al. (Haddad lab, Stanford)  
**Year:** 2019 (published online 2019; print Am J Cardiol 2020;125:229–235)  
**Journal:** Am J Cardiol 2020;125:229–235 · **DOI:** 10.1016/j.amjcard.2019.10.020  
**Data source:** Stanford Translational Research Integrated Database Environment (STRIDE); single centre retrospective cohort  
**Study period:** January 2002 – December 2013  
**N:** 443 (from 580 acute HFpEF hospitalisations; 137 excluded for missing CBC on discharge day)  
**HFpEF definition:** ICD-9 code 428.3; NT-proBNP >300 pg/mL or HF evidence (pulmonary oedema/edema + elevated right atrial pressure); LVEF >50%  
**Primary outcome:** All-cause mortality  
**Median follow-up:** 2.2 years; 121 (27.3%) died

---

## Key Findings

- **Median NLR on admission:** 6.5 (IQR 3.6–11.1); majority (60.7%) decreased during hospitalisation
- **NLR on admission: HR 1.18 (95% CI 1.00–1.38; P=0.04)** — independently associated with all-cause mortality per SD, multivariable
- **Absolute NLR trajectory (discharge − admission): HR 1.26 (95% CI 1.10–1.45; P=0.001)** — independent predictor per SD
- Both NLR on admission and absolute NLR trajectory were incremental to GWTG-HF risk score (P<0.05 for both)
- **AUC improvement by adding NLR + trajectory to GWTG-HF:**
  - At 1 year: ΔAUC +0.047 (P=0.0068); sensitivity 78.8%, specificity 60.5% (optimal 12.9% cutoff)
  - At 2 years: ΔAUC +0.022 (P=0.044)
  - At 3 years: ΔAUC +0.023 (P=0.047)
- **Net reclassification improvement (NRI):** 0.51 at 1 year (P=0.0001); 0.31 at 2 years (P=0.011); 0.27 at 3 years (P=0.019)
- Kaplan-Meier: high NLR tertile on admission (log-rank P=0.04) and high NLR trajectory tertile (log-rank P=0.04) both showed worse survival
- **Other CBC markers independently associated with all-cause mortality:** higher RDW (HR 1.20; 95% CI 1.07–1.37; P=0.002) and lower MCHC (HR 0.82; 95% CI 0.68–0.99; P=0.04)
- Median NT-proBNP (where available, N=271): 2,262 pg/mL (1,071–5,243) — high acuity population

## Methods (brief)

**NLR definition:** Neutrophil count/lymphocyte count from CBC with differential; measured on admission and on discharge day. Absolute NLR trajectory = NLR_discharge − NLR_admission.

**GWTG-HF risk score:** Calculated per Peterson et al.; includes age, race/ethnicity, COPD, heart rate, SBP, BUN, serum sodium.

**Multivariable model:** Hierarchical Cox regression; GWTG-HF score + NT-proBNP (log) + NLR on admission + NLR trajectory. Variables selected with P<0.20 on univariate analysis.

**Population characteristics:**

| Variable | Value (N=443) |
|---|---|
| Mean age | 77±16 years |
| Female | 58.5% |
| BMI | 28.4±7.2 |
| LVEF | 58.4±4.8% |
| Hypertension | 96.6% |
| Coronary artery disease | 58.2% |
| DM | 35.4% |
| AF | 57.5% |
| COPD | 31.2% |
| ACEI/ARB use | 42.4% |
| Beta-blocker | 57.3% |
| Diuretics | 59.6% |
| Median duration of hospitalisation | 5 days |

## Limitations

- Single-centre retrospective design (Stanford STRIDE); subject to selection bias and missing data (N dropped from 580 to 443 due to missing CBC on discharge day)
- NLR is non-specific — elevated in infection, malignancy, hematologic conditions; no exclusion for active infection documented
- Long study period (2002–2013): HFpEF management evolved substantially; older cohort lacks modern SGLT2i, ARNi therapy
- LVEF >50% threshold; NT-proBNP criterion applied only to available subset — ICD-9 code alone insufficient for guideline-level HFpEF diagnosis
- No rehospitalisation endpoint — only mortality followed across different institutions; potential for outcome misclassification
- MCHC and RDW were independently associated but less clinically interpretable than NLR

## Connections

- Updates: [[inflammation-hfpef]] — NLR on admission and trajectory both independently predict all-cause mortality in ADHF-HFpEF beyond GWTG-HF clinical risk score; trajectory (serial measurement) adds unique prognostic information
- Connects to: [[tamaki2023nlrplr]] — Tamaki 2023 (N=1,026, Japanese) and Boralkar 2019 (N=443, US/Stanford) independently validate NLR as a prognostic marker in ADHF-HFpEF; populations differ markedly (age 77 vs. 83; US vs. Japan; single vs. multicentre)
- Connects to: [[fu2024inflammation]] — Fu 2024 meta-analysis includes NLR studies; Boralkar 2019 is one of the individual studies providing US real-world data
- Connects to: [[ammar2025bnp]] — NT-proBNP available in 271/443 patients; NLR adds incremental predictive value beyond NT-proBNP

## Related Pages

- Concepts: [[inflammation-hfpef]], [[natriuretic-peptides]]
- Entities: [[hfpef]], [[acute-hf]]
- Sources: [[tamaki2023nlrplr]], [[fu2024inflammation]], [[ammar2025bnp]], [[verma2024inflammation]]

## Contradictions

NLR trajectory in this study is defined as the absolute change (discharge − admission); a decrease in NLR during hospitalisation (as occurred in 60.7% of patients) is associated with better outcomes — suggesting that inflammatory resolution during hospital treatment is a favourable prognostic sign. This differs from Tamaki 2023 which used the combined admission NLR+PLR cross-sectionally rather than tracking trajectory. The trajectory concept adds a dynamic layer not captured in single-timepoint NLR measurement and represents a more actionable clinical tool. See [[contradictions]].
