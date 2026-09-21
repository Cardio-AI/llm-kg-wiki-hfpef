---
title: "MAGGIC: Meta-analysis Global Group in Chronic Heart Failure \u2014 Individual\
  \ Patient Data Meta-analysis"
citekey: Pocock2013MAGGIC
year: 2013
authors: Pocock SJ, Ariti CA, McMurray JJV, et al.; Meta-analysis Global Group in
  Chronic Heart Failure (MAGGIC)
journal: Eur Heart J
study_type: meta-analysis
evidence_level: high
tags:
- meta-analysis
- hfpef
- hfref
- prognosis
- risk-score
created: 2026-04-30
last_updated: 2026-05-05
sources:
- citekey: Pocock2013MAGGIC
  doi: 10.1093/eurheartj/ehs337
page-type: source-summary-page
---
# MAGGIC Meta-analysis

> Individual patient data meta-analysis (N=39,372; 30 studies; 15,851 deaths) derived a 13-predictor all-cause mortality risk score; EF risk plateaus above 40% — no survival benefit from higher LVEF in preserved range; ACEi/ARB NOT significantly protective in EF ≥40 (RR 0.938 P=0.233), prospectively predicting neutral RAAS trial results in HFpEF; integer score 0–52 (heartfailurerisk.org): score 20 → 25% 3-year mortality, score 30 → 52%.

**Full citation:**
Pocock SJ, Ariti CA, McMurray JJV, et al.; Meta-analysis Global Group in Chronic Heart Failure (MAGGIC). Predicting survival in heart failure: a risk score based on 39 372 patients from 30 studies. *Eur Heart J.* 2013;34(19):1404–1413. doi:[10.1093/eurheartj/ehs337](https://doi.org/10.1093/eurheartj/ehs337)
**Study type:** Individual patient data meta-analysis (IPD-MA) · **N:** 39,372 patients from 30 studies (6 RCTs + 24 observational/registry) · **Population:** Chronic HF across full EF spectrum; LVEF measured in all · **Follow-up:** Median 2.5y (IQR 1.0–3.9y); 15,851 deaths (40.2% all-cause mortality)  
**Primary outcome:** All-cause mortality; derivation of integer risk score for clinical prognostication  
**NCT:** None (meta-analysis) · **Website:** heartfailurerisk.org

---

## Key Findings

- **All-cause mortality:** 15,851 deaths in 39,372 patients (40.2%) at median 2.5y
- **EF threshold:** Risk constant above EF 40% — no additional survival benefit from higher LVEF in preserved range; EF per 5% RR **0.581** (0.554–0.609) up to 40%, then flattens completely
- **ACEi/ARB in EF ≥40:** RR **0.938** (0.864–1.019), **P=0.233** — NOT significant; contrast with EF <40: RR 0.834 (0.787–0.884), P<0.001
- **Beta-blocker protective** across all EF: RR 0.760 (0.726–0.796); EF ≥40 RR 0.820, EF <40 RR 0.734
- **Diabetes more harmful in HFpEF:** EF ≥40 RR 1.513 (1.415–1.619) vs EF <40 RR 1.354
- **Age more dominant in HFpEF:** EF ≥40 age RR 1.589 (1.567–1.611) vs EF <40 RR 1.407
- **Integer risk score:** 0–52 points; score 10 → 10% 3y mortality; score 20 → 25%; score 30 → 52%; score 33+ → 70%

## Methods

**Design:** Pooled individual patient data from 30 studies. 6 RCTs (control/placebo arms used to avoid treatment heterogeneity) + 24 observational cohorts and registries. Data collected from contributing study coordinators; missing covariate values multiply imputed.

**Studies included:**
- 30 total: 6 RCTs + 24 observational
- EF subgroups: EF <40 (N=21,442; 8,900 deaths); EF ≥40 (N=17,930; 6,951 deaths)
- Geographic range: international; enrollment spanning 1980s–2000s

**Statistical model:**
- Poisson regression with survival time grouped into annual intervals; random effect for study accounts for between-study heterogeneity
- 13 independent predictors selected by backward elimination; EF modelled as continuous with linear spline (knot at 40%)
- Integer score derived by rounding log RR coefficients to nearest integer unit (scaled)
- Validation: split-half internal validation; discrimination assessed by C-statistic

**EF-stratified analyses:**
- Table 5: All predictors for EF <40 subgroup (N=21,442)
- Table 6: All predictors for EF ≥40 subgroup (N=17,930)

## Results

### 13 Independent Predictors — Full MAGGIC Model (Table 2)

| Predictor | RR (95% CI) |
|---|---|
| Age per 10y | 1.154 (1.143–1.165) |
| Male sex | 1.115 (1.068–1.163) |
| BMI per 1 kg/m² | 0.965 (0.960–0.970) |
| Current smoker | 1.159 (1.097–1.224) |
| SBP per 10 mmHg | 0.882 (0.877–0.887) |
| Diabetes | 1.422 (1.356–1.491) |
| NYHA I (vs II) | 0.788 (0.736–0.844) |
| NYHA III (vs II) | 1.410 (1.358–1.465) |
| NYHA IV (vs II) | 1.684 (1.561–1.816) |
| EF per 5% (up to 40%) | 0.581 (0.554–0.609); flat above 40% |
| COPD | 1.228 (1.169–1.289) |
| HF duration >18mo | 1.188 (1.130–1.249) |
| Creatinine per 10 µmol/L | 1.039 (1.037–1.041) |
| Beta-blocker | 0.760 (0.726–0.796) |
| ACEi/ARB | 0.908 (0.863–0.955) |

### EF-Stratified Models

**Table 5 — EF <40 (N=21,442; 8,900 deaths)**

| Predictor | RR (95% CI) |
|---|---|
| Age per 10y | 1.407 (1.386–1.428) |
| ACEi/ARB | **0.834 (0.787–0.884)** — significant |
| Beta-blocker | 0.734 (0.694–0.777) |
| SBP per 10 mmHg | 0.842 (0.832–0.852) |
| Diabetes | 1.354 (1.271–1.441) |

**Table 6 — EF ≥40 (N=17,930; 6,951 deaths)**

| Predictor | RR (95% CI) | P |
|---|---|---|
| Age per 10y | **1.589 (1.567–1.611)** | <0.001 |
| ACEi/ARB | **0.938 (0.864–1.019)** | **0.233** |
| Beta-blocker | 0.820 (0.768–0.876) | <0.001 |
| SBP per 10 mmHg | 0.982 (0.973–0.991) | <0.001 |
| Diabetes | 1.513 (1.415–1.619) | <0.001 |

### Risk Score Calibration (Table 4)

| Score | 3-Year Predicted Mortality |
|---|---|
| 0–10 | ~10% |
| ~15 | ~15% |
| ~20 | ~25% |
| ~25 | ~35% |
| ~30 | ~52% |
| ≥33 | 70%+ |

Score range: 0–52; median 23 in derivation cohort.

## Limitations

- **Observational/registry-dominant:** 24/30 studies non-randomised; ACEi/ARB and beta-blocker protective associations likely confounded by indication — healthier patients more likely prescribed, inflating apparent protection
- **Historical enrollment:** Studies span 1980s–2000s; background therapy does not reflect current standard of care (no SGLT2i, minimal sacubitril-valsartan, low ICD/CRT)
- **EF measurement heterogeneity:** LVEF measured by multiple modalities (echo, nuclear, ventriculography) across studies; EF 40% cutoff chosen post-hoc to maximise statistical contrast
- **HFpEF definition pre-modern criteria:** EF ≥40% includes HFmrEF (40–49%) per current taxonomy; no structural/functional diastolic criteria; NT-proBNP not universally available
- **Near-universal ACEi/ARB use in EF ≥40:** 74% already prescribed at baseline; statistical power to detect treatment association severely limited at such high background prevalence
- **No EF-mortality gradient above 40%** may reflect survivor bias or insufficient follow-up in higher-EF registries rather than true biological equivalence
- **Integer score rounding** introduces approximation; exact model coefficients (available at heartfailurerisk.org) needed for maximum accuracy

## HFpEF Wiki Relevance

MAGGIC is the largest prognostic meta-analysis in chronic HF and provides key mechanistic insights:

1. **ACEi/ARB null in EF ≥40 prospectively predicted RAAS trial failures:** Published in 2013, MAGGIC's EF ≥40 ACEi/ARB RR 0.938 P=0.233 — non-significant even with N=17,930 — prospectively explained why CHARM-Preserved (HR 0.89 P=0.118), I-PRESERVE (HR 0.95 P=0.35), and PARAGON-HF (RR 0.87 P=0.06) all narrowly missed significance. The observational signal was weak and non-significant in far larger N than any RCT; the RCTs were highly unlikely to confirm it. This is one of the clearest pre-trial mechanistic predictions in HFpEF evidence history.

2. **EF plateau above 40% — HFpEF as distinct prognostic entity:** No survival benefit from higher LVEF once EF exceeds 40%. HFpEF mortality is driven by non-EF factors (age, comorbidities, NYHA, creatinine), not cardiac pump reserve. This supports the conceptual model of HFpEF as an age-comorbidity syndrome rather than a cardiac dysfunction syndrome on a continuum with HFrEF.

3. **Age dominates HFpEF prognosis more than HFrEF:** Age RR 1.589/decade in EF ≥40 vs 1.407 in EF <40. Combined with diabetes RR 1.513 (> HFrEF 1.354), this frames HFpEF mortality as fundamentally driven by senescence and cardiometabolic burden — consistent with the fat/obese vs. age/AF phenotyping literature.

4. **Validated prognostic tool:** MAGGIC integer score (heartfailurerisk.org) covers the full EF spectrum. Score 20 → 25% 3-year mortality; score 30 → 52%. Referenced in both ESC 2021 and AHA 2022 guidelines for risk stratification.

## Connections
- Cited by: [[pandey2021deepnnecho]] — added automatically from the reciprocal Cites: relationships recorded on those pages
- Cited by: [[shah2015phenomapping]] — added automatically from the reciprocal Cites: relationships recorded on those pages

- Predicts neutral RAAS trials: [[yusuf2003charm]], [[massie2008ipreserve]], [[solomon2019paragon]] — all show HR 0.87–0.95 NS, consistent with observational RR 0.938
- Concept: [[hfpef-treatment-gap]] — ACEi/ARB null in EF ≥40 observational data explains RAAS trial failures; EF plateau supports HFpEF as distinct therapeutic target
- Concept: [[hfpef-diagnosis]] — EF threshold 40% for mortality gradient; HFmrEF (40–49%) lies in transitional zone
- Entity: [[hfpef]] — Age/diabetes/NYHA dominant predictors; 3-year mortality 10–70% across score range
- Guidelines: [[mcdonagh2021esc]], [[heidenreich2022aha]] — both cite MAGGIC for HF risk stratification
- Cites: [[solomon2022deliver]] — DELIVER's LVEF ≥60% treatment-benefit persistence contrasted with MAGGIC's flat EF-mortality gradient above 40%

## Secondary Analyses & Data Reuse

| Citekey | Focus | Wiki page |
|---------|-------|-----------|
| (Multiple secondary publications from MAGGIC consortium — phenotyping subanalyses) | — | — |

## Related Pages
- Concepts: [[hfpef-treatment-gap]], [[hfpef-diagnosis]], [[hf-phenotype-classification]]
- Entities: [[hfpef]], [[hfref]], [[hfmref]], [[maggic-risk-score]]
- Sources: [[yusuf2003charm]], [[massie2008ipreserve]], [[solomon2019paragon]], [[mcdonagh2021esc]], [[heidenreich2022aha]]

## Contradictions
- **ACEi/ARB observational RR 0.938 (P=0.233) in EF ≥40** vs. directionally concordant but also NS RCT effects: CHARM-Preserved HR 0.89 P=0.118, I-PRESERVE HR 0.95 P=0.35, PARAGON RR 0.87 P=0.06. MAGGIC is consistent in direction with all three RCTs but non-significant even at N=17,930 — near-universal use (74%) severely limits observational power. The RCT evidence confirms: no significant population-level benefit. The directionality remains intriguing for subgroups (PARAGON women, lower EF). See [[contradictions]].
- **No EF-mortality gradient above 40%** (MAGGIC) vs. **treatment benefit persists above 60% LVEF** (DELIVER HR ~0.74 in LVEF ≥60%). MAGGIC shows EF does not predict survival once normalised; this does not mean treatment is ineffective in very-high-EF patients — SGLT2i's mechanism (haemodynamic, natriuretic, anti-inflammatory) is independent of EF-associated prognosis. Absence of prognostic gradient ≠ absence of treatment benefit gradient. See [[contradictions]].
