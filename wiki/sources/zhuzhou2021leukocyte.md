---
type: study
title: "Zhu and Zhou 2021 \u2014 Leukocyte Count and Adverse Outcomes in HFpEF (TOPCAT)"
citekey: ZhuZhou2021Leukocyte
year: 2021
authors: Zhu Z, Zhou S
journal: BMC Cardiovasc Disord
study_type: observational-secondary-analysis
evidence_level: moderate
tags:
- inflammation
- biomarker
- hfpef
- prognosis
- leukocyte
- topcat
created: 2026-05-18
last_updated: 2026-05-18
sources:
- file: raw/2021-BMC-CardiovascDis-Zhu-Zhou-TOPCAT-subanalysis-leukocyte.pdf
  citekey: ZhuZhou2021Leukocyte
page-type: source-summary-page
---
# Zhu and Zhou 2021 — Leukocyte Count and Adverse Outcomes in HFpEF (TOPCAT Substudy)

> Secondary analysis of the TOPCAT trial (N=2,898; LVEF ≥50%) demonstrating a **U-shaped relationship** between leukocyte count and all-cause mortality: both the lowest (Q1, ≤5.5×10⁹/L) and highest (Q4, >8.0×10⁹/L) quartiles had significantly higher adjusted mortality vs. the reference Q2 range (HR 1.44 and 1.90 respectively); U-shaped pattern was significant in women but not men.

**File:** `raw/2021-BMC-CardiovascDis-Zhu-Zhou-TOPCAT-subanalysis-leukocyte.pdf`  
**Authors:** Zhu Z, Zhou S (Department of Cardiovascular Medicine, The Second Xiangya Hospital, Central South University, Changsha, Hunan, China)  
**Year:** 2021 · **Journal:** BMC Cardiovasc Disord 2021;21:333 · **DOI:** 10.1186/s12872-021-02142-y  
**Data source:** TOPCAT trial (NCT00094302) — secondary analysis  
**N:** 2,898 with LVEF ≥50% (from TOPCAT total N=3,445; excluded N=515 with LVEF <50%; excluded N=32 for outlier/missing leukocyte data)  
**Primary outcome:** All-cause mortality  
**Secondary outcomes:** Composite CV events (aborted cardiac arrest, CV death, HF hospitalisation); HF hospitalisation  
**Mean follow-up:** 3.4 years; 429 deaths, 671 composite CV events, 386 HF hospitalisations

---

## Key Findings

- **U-shaped relationship between leukocyte count and all-cause mortality:**
  - Q1 (≤5.5×10⁹/L): adjusted HR 1.439 (95% CI 1.060–1.953; P=0.020) vs. Q2 reference
  - Q3 (6.7–8.0×10⁹/L): adjusted HR 1.510 (95% CI 1.113–2.050; P=0.008)
  - Q4 (>8.0×10⁹/L): adjusted HR 1.901 (95% CI 1.424–2.539; P<0.001)
  - Q2 (5.5–6.7×10⁹/L): reference (lowest mortality risk)
- **Composite CV events:** Q3 HR 1.606 (95% CI 1.407–1.904); Q4 HR 1.650 (95% CI 1.108–2.459) — U-shaped pattern
- **HF hospitalisation:** Leukocyte count NOT independently predictive of HF hospitalisation after multivariable adjustment — outcome-specific finding
- **Sex subgroup (pre-specified):** U-shaped relationship significant in women (P=0.002) but NOT in men (P=0.088) — sex modifies the leukocyte-outcome relationship
- Restricted cubic spline analysis confirmed continuous U-shaped relationship for all three outcomes

## Methods (brief)

**Leukocyte quartiles (based on measured WBC):**
- Q1: ≤5.5×10⁹/L (N=753)
- Q2: 5.5–6.7×10⁹/L (N=707; reference)
- Q3: 6.7–8.0×10⁹/L (N=720)
- Q4: >8.0×10⁹/L (N=718)

**Multivariable adjustment:** Age, sex, race, BMI, smoking, NYHA class, heart rate, eGFR, BUN, hemoglobin, albumin, log-BNP, LVEF, medications (ACEI/ARB, beta-blockers, statins, loop diuretics, spironolactone).

**Baseline characteristics (selected; N=2,898):**

| Variable | All |
|---|---|
| Mean age | 69±9.6 years |
| Male | 46% |
| White | 89% |
| LVEF | 59±6.5% |
| Hypertension | 91% |
| DM | 30% |
| AF | 35% |
| NYHA III-IV | 70% |
| Loop diuretic | 43% |
| Spironolactone (all groups) | 48–52% |

Higher leukocyte quartile associated with: higher BMI, heart rate; lower diastolic BP and eGFR; more NYHA III-IV; more COPD, DM, AF, dyslipidemia.

## Limitations

- TOPCAT data only — TOPCAT has known site-specific enrollment issues (Russia/Georgia contamination); generaliseability uncertain
- Leukocyte count measured at baseline only — no serial measurements to track trajectory
- Leukocyte (WBC) is a composite marker; specific subtypes (neutrophil, lymphocyte, monocyte) not analysed — mechanism remains inferential
- Residual confounding possible: higher leukocyte quartile associated with more comorbidities
- U-shaped lower bound (Q1 low WBC) may reflect frailty, malignancy, or immunosuppression rather than directly inflammatory HFpEF biology — mechanism differs for the two arms of the U
- Women-only U-shaped finding may reflect statistical type-II error in men rather than true biological sex difference

## Connections

- Updates: [[inflammation-hfpef]] — TOPCAT-based evidence for U-shaped leukocyte-mortality relationship; both excess and deficient inflammation associated with worse prognosis
- Connects to: [[fu2024inflammation]] — Zhu and Zhou 2021 cited in Fu 2024 meta-analysis as the largest N (2,898) study on WBC in stable HFpEF; largest in the systematic review
- Connects to: [[tamaki2023nlrplr]] — NLR/PLR (neutrophil/lymphocyte ratio) prognostic in ADHF-HFpEF (Tamaki); leukocyte count prognostic in stable chronic HFpEF (Zhu/Zhou); different populations, consistent direction for high inflammatory burden
- Connects to: [[pitt2014topcat]] — same TOPCAT dataset; this analysis uses LVEF ≥50% subgroup and WBC as the exposure variable

## Related Pages

- Concepts: [[inflammation-hfpef]]
- Entities: [[hfpef]], [[topcat]]
- Sources: [[pitt2014topcat]], [[tamaki2023nlrplr]], [[boralkar2019nlr]], [[fu2024inflammation]]

## Contradictions

The U-shaped relationship (both low and high leukocyte counts associated with worse outcomes) is mechanistically distinct from the simpler "high inflammation = worse outcome" narrative in HFpEF. Low leukocyte count (Q1) may represent immunosuppression, frailty, or malnutrition (distinct mechanism from high inflammatory burden in Q4). The U-shape means inflammatory markers cannot be simply interpreted as "higher = worse" in this population — both extremes are harmful, possibly through different biological pathways. This complicates the use of WBC as a predictive biomarker in clinical practice compared to more specific markers (NLR, PLR, hs-CRP). Noted in `wiki/contradictions.md`.
