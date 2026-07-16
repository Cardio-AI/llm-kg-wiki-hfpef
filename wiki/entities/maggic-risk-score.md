---
title: MAGGIC Risk Score
summary: "Integer mortality risk score (0–52 points) derived from an individual patient
  data meta-analysis of 39,372 chronic HF patients across the full LVEF spectrum;
  13 predictors (age, EF, NYHA class, creatinine, diabetes, SBP, BMI, smoking, COPD,
  HF duration, beta-blocker/ACEi-ARB use, male sex) computed via heartfailurerisk.org;
  used both clinically for prognostication and as a covariate to demonstrate incremental
  prognostic value of HFpEF ML phenomapping."
entity_type: score
tags:
  - diagnosis
  - prognosis
  - hfpef
  - hfref
created: 2026-07-15
last_updated: 2026-07-15
sources:
  - citekey: Pocock2013MAGGIC
    doi: 10.1093/eurheartj/ehs337
  - citekey: Shah2015Phenomapping
    doi: 10.1161/CIRCULATIONAHA.114.010637
page-type: entity-page
---
# MAGGIC Risk Score

> Integer risk score (0–52 points) derived by the Meta-Analysis Global Group in Chronic Heart Failure (MAGGIC) from individual patient data across 39,372 patients (30 studies) spanning the full LVEF range; quantifies 1- and 3-year all-cause mortality risk from 13 readily available clinical predictors; validated as adding prognostic information beyond BNP in HFpEF ML phenomapping.

## Aliases

| Alias | Type | Notes |
|---|---|---|
| MAGGIC | acronym | Meta-Analysis Global Group in Chronic Heart Failure |
| MAGGIC score | alternate-name | common clinical shorthand |
| heartfailurerisk.org | research-name | online calculator hosting the score |

---

## Description

The MAGGIC score was derived by Pocock et al. (2013) from an individual patient data meta-analysis (IPD-MA) of 39,372 patients with chronic heart failure across 30 studies (6 RCTs + 24 observational/registry cohorts), spanning both reduced and preserved LVEF. Median follow-up was 2.5 years; 15,851 patients (40.2%) died. Poisson regression with forward stepwise variable selection identified 13 independent, highly significant mortality predictors, in descending order of predictive strength: age, lower EF, NYHA class, serum creatinine, diabetes, not prescribed beta-blocker, lower systolic BP, lower body mass, time since diagnosis, current smoker, COPD, male sex, and not prescribed ACE inhibitor or angiotensin-receptor blocker. (source: [[pocock2013maggic]])

The continuous model coefficients were converted into an easy-to-use integer risk score (0–52 points; median 23 in the derivation cohort), accessible online at heartfailurerisk.org. (source: [[pocock2013maggic]])

**Integer scoring chart** (raw derivation document, Figure 2):

| Risk factor | Points |
|---|---|
| EF <20% / 20–24% / 25–29% / 30–34% / 35–39% / ≥40% | +7 / +6 / +5 / +3 / +2 / 0 |
| Extra for age, if EF <30% (by decade <55 → ≥80y) | 0, +1, +2, +4, +6, +8, +10 |
| Extra for age, if EF 30–39% | 0, +2, +4, +6, +8, +10, +13 |
| Extra for age, if EF ≥40% | 0, +3, +5, +7, +9, +12, +15 |
| Extra for SBP, if EF <30% (<110 → ≥150 mmHg) | +5, +4, +3, +2, +1, 0 |
| Extra for SBP, if EF 30–39% | +3, +2, +1, +1, 0, 0 |
| Extra for SBP, if EF ≥40% | +2, +1, +1, 0, 0, 0 |
| BMI <15 / 15–19 / 20–24 / 25–29 / ≥30 kg/m² | +6, +5, +3, +2, 0 |
| Creatinine <90 / 90–109 / 110–129 / 130–149 / 150–169 / 170–209 / 210–249 / ≥250 µmol/L | 0, +1, +2, +3, +4, +5, +6, +8 |
| NYHA class I / II / III / IV | 0, +2, +6, +8 |
| Male sex | +1 |
| Current smoker | +1 |
| Diabetic | +3 |
| Diagnosis of COPD | +2 |
| First diagnosis of HF within past 18 months | +2 |
| Not on beta-blocker | +3 |
| Not on ACEi/ARB | +1 |

Age and EF, and SBP and EF, enter as interaction terms — the mortality impact of age and of low SBP is more pronounced at higher EF, so the score's "extra for age/SBP" component is itself EF-band-dependent, as shown in the table above. (raw PDF: Pocock SJ et al., *Eur Heart J.* 2013;34(19):1404–1413, Figure 2)

## Role in HFpEF

**EF plateau above 40%:** No additional survival benefit is conferred by higher LVEF once EF exceeds 40% — EF per 5% increase carries RR 0.581 (95% CI 0.554–0.609) up to 40%, then flattens completely. This supports a conceptual model of HFpEF as an age-comorbidity syndrome rather than a cardiac-dysfunction syndrome on a continuum with HFrEF. (source: [[pocock2013maggic]])

**ACEi/ARB null in EF ≥40%, prospectively predicting RAAS trial failures:** In the EF ≥40 subgroup (N=17,930), ACEi/ARB carried RR 0.938 (95% CI 0.864–1.019, P=0.233) — not significant — versus RR 0.834 (P<0.001) in EF <40. Published in 2013, this non-significant observational association (despite N=17,930) anticipated the narrowly missed significance of CHARM-Preserved (HR 0.89, P=0.118), I-PRESERVE (HR 0.95, P=0.35), and PARAGON-HF (RR 0.87, P=0.06). (source: [[pocock2013maggic]])

**Age and diabetes dominate HFpEF prognosis more than HFrEF:** Age RR 1.589/decade in EF ≥40 vs. 1.407 in EF <40; diabetes RR 1.513 in EF ≥40 vs. 1.354 in EF <40. (source: [[pocock2013maggic]])

**Adjustment covariate in HFpEF ML phenomapping (Shah 2015):** MAGGIC score was used, alongside BNP, as an adjustment covariate to test whether unsupervised ML-derived phenogroups add prognostic information beyond conventional risk markers. Mean MAGGIC score rose stepwise across the three phenogroups: phenogroup 1 ("young/mild") 15.6±6.7, phenogroup 2 ("obese/metabolic/atrial") 19.8±5.8, phenogroup 3 ("cardiorenal/advanced remodeling") 22.8±7.5 (P<0.001) — phenogroup 3 has the highest MAGGIC-predicted background risk of the three groups. Even after adjusting for BNP and MAGGIC score, phenogroup 3 retained an adjusted HR of 3.3 (95% CI 1.1–9.5, P=0.026) for the combined outcome in the validation cohort, and phenogroup assignment provided prognostic information above and beyond BNP and MAGGIC score (positive likelihood ratio test, NRI, and IDI). (source: [[shah2015phenomapping]])

## Evidence

**13 independent predictors — full model (N=39,372):**

| Predictor | RR (95% CI) |
|---|---|
| Age per 10y | 1.154 (1.143–1.165) |
| Male sex | 1.115 (1.068–1.163) |
| BMI per 1 kg/m² (up to 30) | 0.965 (0.960–0.970) |
| Current smoker | 1.159 (1.097–1.224) |
| SBP per 10 mmHg | 0.882 (0.877–0.887) |
| Diabetes | 1.422 (1.356–1.491) |
| NYHA I (vs. II) | 0.788 (0.736–0.844) |
| NYHA III (vs. II) | 1.410 (1.358–1.465) |
| NYHA IV (vs. II) | 1.684 (1.561–1.816) |
| EF per 5% (up to 40%) | 0.581 (0.554–0.609); flat above 40% |
| COPD | 1.228 (1.169–1.289) |
| HF duration >18mo | 1.188 (1.130–1.249) |
| Creatinine per 10 µmol/L (up to 350) | 1.039 (1.037–1.041) |
| Beta-blocker | 0.760 (0.726–0.796) |
| ACEi/ARB | 0.908 (0.863–0.955) |

**Risk score calibration** (score → predicted mortality): score 10 → 10% 1-year / — 3-year probability; score 20 → 25% 3-year mortality; score 30 → 52% 3-year mortality; score ≥33 → ~70%+ 3-year mortality. Score range 0–52; median 23 in derivation cohort. (source: [[pocock2013maggic]])

**EF-stratified models:** in EF <40 (N=21,442; 8,900 deaths), ACEi/ARB RR 0.834 (0.787–0.884, significant); in EF ≥40 (N=17,930; 6,951 deaths), ACEi/ARB RR 0.938 (0.864–1.019, P=0.233, non-significant), while age (RR 1.589) and diabetes (RR 1.513) are more dominant than in the EF <40 subgroup. (source: [[pocock2013maggic]])

## Status

Validated internally via split-half analysis; discrimination assessed by C-statistic. Referenced in both ESC 2021 and AHA 2022 guidelines for HF risk stratification. (source: [[pocock2013maggic]]) Implemented as a public online calculator at heartfailurerisk.org. (raw PDF: Pocock SJ et al., *Eur Heart J.* 2013;34(19):1404–1413)

**Limitations:** 24/30 contributing studies were observational/registry-based; ACEi/ARB and beta-blocker protective associations are likely confounded by indication (healthier patients preferentially prescribed). Enrollment spans the 1980s–2000s, predating SGLT2 inhibitors and largely predating sacubitril-valsartan and modern device therapy, so background-therapy context does not reflect current standard of care. EF was measured heterogeneously (echo, nuclear, ventriculography) across studies, and the EF ≥40% definition of "preserved" EF in this 2013 dataset includes what would now be classified as HFmrEF (40–49%) under current taxonomy. Near-universal ACEi/ARB use in EF ≥40 (74% at baseline) severely limited statistical power to detect a treatment association in that subgroup. (source: [[pocock2013maggic]])

## Related Pages

- Concepts: [[hfpef-treatment-gap]], [[hfpef-diagnosis]], [[hf-phenotype-classification]], [[ml-ai-hfpef]]
- Entities: [[hfpef]], [[hfref]], [[hfmref]]
- Sources: [[pocock2013maggic]], [[shah2015phenomapping]], [[mcdonagh2021esc]], [[heidenreich2022aha]]

## Contradictions

- **ACEi/ARB observational RR 0.938 (P=0.233) in EF ≥40** is directionally concordant with, but non-significant like, the RCT effects of CHARM-Preserved (HR 0.89, P=0.118), I-PRESERVE (HR 0.95, P=0.35), and PARAGON-HF (RR 0.87, P=0.06) — MAGGIC did not achieve significance even at N=17,930, largely because near-universal background use (74%) limited observational power. See [[contradictions]].
- **No EF-mortality gradient above 40%** (MAGGIC) vs. **treatment benefit persisting above 60% LVEF** in DELIVER (HR ~0.74 in LVEF ≥60%) — absence of a prognostic EF gradient does not imply absence of a treatment-benefit gradient; SGLT2i mechanism (haemodynamic, natriuretic, anti-inflammatory) is argued to be independent of EF-associated background prognosis. See [[contradictions]].

## References
- Pocock SJ, Ariti CA, McMurray JJV, Køber L, Squire IB, Swedberg K, Dobson J, Poppe KK, Whalley GA, Doughty RN; Meta-Analysis Global Group in Chronic Heart Failure (MAGGIC). Predicting survival in heart failure: a risk score based on 39,372 patients from 30 studies. *Eur Heart J.* 2013;34(19):1404–1413. doi:[10.1093/eurheartj/ehs337](https://doi.org/10.1093/eurheartj/ehs337)
- Shah SJ, Katz DH, Selvaraj S, Burke MA, Yancy CW, Gheorghiade M, Bonow RO, Huang CC, Deo RC. Phenomapping for Novel Classification of Heart Failure With Preserved Ejection Fraction. *Circulation.* 2015;131(3):269–279. doi:[10.1161/CIRCULATIONAHA.114.010637](https://doi.org/10.1161/CIRCULATIONAHA.114.010637)
