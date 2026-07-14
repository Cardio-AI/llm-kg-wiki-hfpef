---
question: "How does obesity affect natriuretic peptide interpretation in HFpEF?"
answer_summary: Obesity suppresses BNP and NT-proBNP through two independent mechanisms — (1) adipocyte-mediated clearance via NPR-C and neprilysin, and (2) Thr-71 glycosylation of NT-proBNP blocking Elecsys antibody binding (ratio 0.27 HFpEF vs. 0.32 HFrEF; ~3.6× underestimation). Up to 20–30% of invasively confirmed HFpEF fall below the ≥125 pg/mL diagnostic threshold. Low NP in obese HFpEF signals worse — not better — prognosis (inverse of HFrEF). H₂FPEF partially compensates via its BMI ≥30 = 2pt term; HFA-PEFF does not. tNT-proBNP (research-only) corrects for glycosylation but is not commercially available. Weight loss with semaglutide reduced NT-proBNP by 22% vs. 4.9% placebo.
sources_used:
  - McDonagh2021ESC
  - hage2026ntprobnp
  - Ammar2025BNP
  - borlaug2023statement
  - landsteiner2025hemodynamics
  - Reddy2018H2FPEF
  - morfino2022biomarkers
timestamp: 2026-05-21
verification_status: verified
derived_from:
  - wiki/concepts/natriuretic-peptides.md
  - wiki/entities/obesity-hfpef.md
  - wiki/sources/hage2026ntprobnp.md
  - wiki/sources/ammar2025bnp.md
  - wiki/sources/borlaug2023statement.md
  - wiki/sources/landsteiner2025hemodynamics.md
---

## Question

How does obesity affect natriuretic peptide interpretation in HFpEF?

---

## Answer

### Clinical bottom line

Obesity suppresses BNP and NT-proBNP through two independent mechanisms — enhanced peripheral clearance and Thr-71 glycosylation of NT-proBNP — producing measured NP levels that are systematically lower than the true haemodynamic burden. In the obese HFpEF patient, a normal or low NP **does not exclude HFpEF**, the prognostic inversion is opposite to HFrEF (low BNP predicts worse, not better outcomes), and standard diagnostic thresholds lose sensitivity in proportion to BMI [[McDonagh2021ESC]], [[Ammar2025BNP]], [[hage2026ntprobnp]].

---

### Mechanism 1 — Adipocyte-mediated NP clearance and degradation

Adipose tissue is not metabolically inert with respect to natriuretic peptides. Two clearance pathways are upregulated with increasing fat mass [[borlaug2023statement]], [[McDonagh2021ESC]]:

**NPR-C (natriuretic peptide clearance receptor):** Expressed on adipocytes; binds and internalises BNP for degradation. Greater fat mass → greater NPR-C sink → reduced circulating BNP. This affects BNP substantially (short half-life ~20 min; cleared via NPR-C and neprilysin) and NT-proBNP less so (longer half-life ~70–120 min; not a neprilysin substrate), but both are suppressed.

**Neprilysin (neutral endopeptidase 24.11):** Cleaves BNP in plasma and in the kidney and lung. Adipose tissue and the kidney both express neprilysin; obese patients have proportionally higher neprilysin activity → accelerated BNP catabolism.

**Net effect:** Obese HFpEF patients have lower BNP relative to haemodynamic severity than non-obese patients. This is the primary reason BNP is more profoundly suppressed in obesity than NT-proBNP, though both are affected [[McDonagh2021ESC]], [[borlaug2023statement]].

---

### Mechanism 2 — Glycosylation of NT-proBNP at Thr-71 (Hage 2026)

A second, mechanistically distinct pathway has been characterised: **post-translational O-glycosylation of NT-proBNP at threonine-71** [[hage2026ntprobnp]].

The globally dominant standard assay (Elecsys proBNP II STAT; Roche) uses monoclonal antibodies targeting the central NT-proBNP epitope. When Thr-71 is glycosylated, the antibody cannot bind the glycosylated fraction → that fraction is invisible to the assay → measured NT-proBNP is falsely lower than the true total concentration.

**Total NT-proBNP (tNT-proBNP)** — a research-use-only assay (Roche Diagnostics) using antibodies to glycosylation-free N- and C-terminal epitopes — detects both forms. Key data from KaRen (HFpEF, N=83) and MetAnEnd (HFrEF, N=79) [[hage2026ntprobnp]]:

| Measure | HFpEF | HFrEF | P |
|---|---|---|---|
| tNT-proBNP median (pg/mL) | 3,830 | 10,468 | <0.001 |
| NT-proBNP median (pg/mL) | 1,055 | 3,196 | <0.001 |
| NT-proBNP / tNT-proBNP ratio | **0.27** | **0.32** | 0.019 |

The lower ratio in HFpEF means **HFpEF has proportionally more glycosylation** than HFrEF — the standard assay underestimates NT-proBNP more severely in HFpEF than in HFrEF. In HFpEF patients, tNT-proBNP is approximately **3.6× higher** than standard NT-proBNP.

**Drivers of glycosylation in HFpEF:**

| Driver | Association (Hage 2026) |
|---|---|
| Higher BMI | Primary driver across both EF categories |
| Type 2 diabetes / insulin resistance | Strong independent driver |
| Atrial fibrillation | OR 4.11 in HFpEF |
| Lower eGFR | OR 0.34 |
| Higher systolic BP | OR 0.29 |
| Higher heart rate | OR 11.5 in HFpEF |

These drivers overlap precisely with the HFpEF comorbidity profile — obesity, T2DM, hypertension, AF — meaning glycosylation-driven underestimation is most severe in the patients most likely to have HFpEF [[hage2026ntprobnp]].

**Clinical scale of the problem:** In obese, diabetic HFpEF, the combination of adipocyte clearance (mechanism 1) and glycosylation (mechanism 2) can produce standard NT-proBNP values well below the ≥125 pg/mL diagnostic threshold despite haemodynamically confirmed HFpEF.

---

### Diagnostic consequences

**False-negative rate:** Up to **20% of invasively confirmed HFpEF** fall below the NT-proBNP ≥125 pg/mL diagnostic threshold [[McDonagh2021ESC]]; Borlaug 2023 estimates this as high as **30%** in contemporary cohorts enriched for obesity [[borlaug2023statement]].

**Landsteiner 2025 trial data:** NT-proBNP thresholds as used in pivotal HFpEF trials excluded **67–71%** of patients with hemodynamically confirmed HFpEF (HC-HFpEF) — the primary exclusion mechanism was NT-proBNP below trial entry threshold. STEP-HFpEF, which substituted BMI ≥30 kg/m² for the high NP requirement, excluded only 35% of HC-HFpEF — a substantially more inclusive design [[landsteiner2025hemodynamics]].

**Algorithm-specific implications:**

| Algorithm | BMI component       | NP role                                                 | Obesity behaviour                                                                                                                                                 |
| --------- | ------------------- | ------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| H₂FPEF    | **BMI >30 = 2 pts** | E/e' >9 = 1 pt; PA systolic >35 mmHg = 1 pt             | BMI points partially compensate for suppressed NP; obese patient can reach intermediate/high score without elevated NP                                            |
| HFA-PEFF  | None                | NT-proBNP domain: major ≥220 pg/mL, minor 125–220 pg/mL | No offset for obesity — suppressed NP directly reduces biomarker domain score; obese patient with normal echo may score ≤1 and be misclassified as HFpEF unlikely |

The H₂FPEF algorithm is more robust to NP suppression in obesity precisely because its BMI term is a structural compensation [[Reddy2018H2FPEF]], [[borlaug2023statement]].

---

### Prognostic consequences — the obesity paradox inversion

In HFrEF, low BNP reliably signals good prognosis and treatment response. **In HFpEF, the relationship inverts** [[Ammar2025BNP]]:

- Obese HFpEF patients have lower BNP/NT-proBNP despite **equivalent or worse haemodynamic burden**
- One cohort (Sakane et al. in [[Ammar2025BNP]]): HFpEF with low BNP had **worse outcomes** than HFpEF with elevated BNP — the opposite of the HFrEF pattern
- Meta-analysis dose-response [[Ammar2025BNP]]: BNP ≥300 pg/mL → HR 7.80 for adverse events, but BNP 30–99 pg/mL → HR 2.50 — even the "low-BNP" obese HFpEF group carries substantial risk, with NP artificially depressed below the level that would be expected for their haemodynamic severity

**Prognostic value of tNT-proBNP:** In multivariable Cox analysis in HFpEF [[hage2026ntprobnp]]:

| Model | tNT-proBNP HR | P | Standard NT-proBNP |
|---|---|---|---|
| Univariable | 1.69 (1.07–2.66) | 0.024 | Significant |
| Model 1 (age, sex, eGFR) | 1.51 (0.92–2.49) | 0.101 — NS | NS |
| Model 2 (age, sex, diabetes) | **1.77 (1.08–2.88)** | **0.022** | NS — loses significance |

When adjusting for eGFR rather than diabetes, standard NT-proBNP loses independent prognostic significance in HFpEF while tNT-proBNP retains it — suggesting tNT-proBNP captures prognostic signal that standard NT-proBNP misses in the obese/diabetic population.

---

### Clinical workarounds

| Strategy                                                           | Rationale                                                                                                                 | Evidence                                      |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| Do not use low NP to exclude HFpEF in obese patients               | 20–30% false-negative rate                                                                                                | [[McDonagh2021ESC]], [[borlaug2023statement]] |
| Apply H₂FPEF preferentially in obese patients                      | BMI term compensates for NP suppression                                                                                   | [[Reddy2018H2FPEF]], [[borlaug2023statement]] |
| Exercise echocardiography if NP normal but clinical suspicion high | Exercise PASP ≥45 mmHg has AUC 0.99 regardless of NP level                                                                | [[borlaug2010exercise]]                       |
| Weight loss normalises NP                                          | Semaglutide reduced NT-proBNP by 22% vs. 4.9% placebo (Petrie 2024; N=1,145); effect independent of weight loss magnitude | [[obesity-hfpef]]                             |
| BNP ≥100 pg/mL retains prognostic signal                           | Even in obese HFpEF, BNP >100 pg/mL → HR 4.00 for hospitalisation                                                         | [[Ammar2025BNP]]                              |
| Serial NT-proBNP change >1,000 ng/L over 6 months                  | Predicts CV death/HF hospitalisation (HR ~2) even when absolute level appears low                                         | [[morfino2022biomarkers]]                     |

**tNT-proBNP (total NT-proBNP):** The research assay that corrects for glycosylation is not commercially available. Its clinical availability would most benefit the obese/diabetic HFpEF phenotype where the glycosylation gap is largest, but it requires prospective validation in larger cohorts before clinical deployment [[hage2026ntprobnp]].

---

## Evidence

| Finding | Source | Key datum |
|---|---|---|
| Up to 20–30% HFpEF below NP threshold | [[McDonagh2021ESC]], [[borlaug2023statement]] | False-negative rate in obese/invasively confirmed HFpEF |
| NP suppression mechanisms | [[borlaug2023statement]] | Adipocyte NPR-C + neprilysin clearance |
| Thr-71 glycosylation | [[hage2026ntprobnp]] | NT-proBNP/tNT-proBNP ratio 0.27 HFpEF vs. 0.32 HFrEF; ~3.6× underestimation in HFpEF |
| Obesity paradox inversion | [[Ammar2025BNP]] | Low BNP = worse prognosis in HFpEF (opposite of HFrEF) |
| Trial exclusion by NP threshold | [[landsteiner2025hemodynamics]] | 67–71% HC-HFpEF excluded by trial NP entry criteria |
| H₂FPEF BMI offset | [[Reddy2018H2FPEF]] | BMI >30 = 2 pts; partially compensates for NP suppression |
| Weight loss normalises NP | [[obesity-hfpef]] (Petrie 2024) | Semaglutide −22% NT-proBNP vs. −4.9% placebo |

---

## Contradictions

- **Mechanism 1 vs. mechanism 2 relative contribution:** The relative contribution of adipocyte-mediated BNP clearance vs. Thr-71 glycosylation to NT-proBNP suppression in obese HFpEF is unquantified. Both are plausible and likely additive, but no study has formally decomposed the two pathways [[hage2026ntprobnp]], [[borlaug2023statement]]. See [[contradictions]].
- **tNT-proBNP statistical power:** All tNT-proBNP prognostic comparisons in Hage 2026 (N=83 HFpEF) are exploratory and non-significant at conventional thresholds — the mechanistic plausibility is established but clinical utility unproven at scale [[hage2026ntprobnp]].
- **Obesity paradox directionality:** Low BNP in obese HFpEF signals worse prognosis (adipocyte suppression of BNP despite haemodynamic burden) — but some observational cohorts report lower overall mortality in obese vs. lean HFpEF, creating an apparent paradox. RCT evidence (STEP-HFpEF, SUMMIT) supports that weight reduction improves outcomes, resolving the paradox in favour of adiposity as harmful. See [[contradictions]].

---

## References

**McDonagh2021ESC**
> McDonagh TA, Metra M, Adamo M, et al. 2021 ESC Guidelines for the diagnosis and treatment of acute and chronic heart failure. *Eur Heart J.* 2021;42(36):3599–3726. doi:10.1093/eurheartj/ehab368

**hage2026ntprobnp**
> Hage C, Mang A, Daubert JC, et al. Total NT-proBNP in heart failure with preserved vs reduced ejection fraction. *Int J Cardiol.* 2026;458:134554. doi:10.1016/j.ijcard.2026.134554

**Ammar2025BNP**
> Ammar LA, Massoud GP, Chidiac C, et al. BNP and NT-proBNP as Prognostic Biomarkers in HFpEF: Systematic Review and Meta-Analysis. *Heart Fail Rev.* 2025;30(1):45–54.

**borlaug2023statement**
> Borlaug BA, Sharma K, Shah SJ, Ho JE. Heart Failure With Preserved Ejection Fraction: JACC Scientific Statement. *J Am Coll Cardiol.* 2023;81(18):1810–1834. doi:10.1016/j.jacc.2023.01.049

**landsteiner2025hemodynamics**
> Landsteiner I, Ikoma T, Ramesh A, et al. Implications of HFpEF Definitions Unveiled by Rest and Exercise Hemodynamics. *Circ Res.* 2025;137:357–359. doi:10.1161/CIRCULATIONAHA.124.072346

**Reddy2018H2FPEF**
> Reddy YNV, Carter RE, Obokata M, Redfield MM, Borlaug BA. A Simple, Evidence-Based Approach to Help Guide Diagnosis of Heart Failure with Preserved Ejection Fraction. *Circulation.* 2018;138(9):861–870. doi:10.1161/CIRCULATIONAHA.118.034646

**morfino2022biomarkers**
> Morfino P, Aimo A, Castiglione V, Vergaro G, Emdin M, Clerico A. Biomarkers of HFpEF: Natriuretic Peptides, High-Sensitivity Troponins and Beyond. *J Cardiovasc Dev Dis.* 2022;9(8):256. doi:10.3390/jcdd9080256

---

## Evidence Quality

**Rating: 4 / 5**
- Sources: 7 (2 major guidelines, 1 JACC scientific statement, 1 systematic review/meta-analysis, 1 mechanistic cohort study, 1 contemporary haemodynamic cohort, 1 diagnostic algorithm derivation)
- Evidence type: guideline (ESC 2021); scientific statement (Borlaug 2023); meta-analysis (Ammar 2025; 22 studies, 10,158 patients); mechanistic cohort (Hage 2026; N=162); retrospective haemodynamic cohort (Landsteiner 2025; N=872); algorithm derivation (Reddy 2018)
- Publication years: 2018–2026
- Limitations: tNT-proBNP data from small cohorts (N=83 HFpEF); research-use-only assay not commercially available; quantitative contribution of glycosylation vs. adipocyte clearance not decomposed; BMI-adjusted NP thresholds not yet formally validated in prospective studies; obesity paradox inversion mechanistically plausible but confounded by selection bias in observational data
