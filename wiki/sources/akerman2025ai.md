---
type: source
title: External validation of artificial intelligence for detection of heart failure
  with preserved ejection fraction
citekey: akerman2025ai
year: 2025
authors: Akerman AP, Al-Roub N, Angell-James C, Cassidy MA, Thompson R, Bosque L,
  Rainer K, Hawkes W, Piotrowska H, Leeson P, Woodward G, Pellikka PA, Upton R, Strom
  JB
journal: Nature Communications
tags:
- ml-ai
- diagnosis
created: 2026-05-15
last_updated: 2026-05-15
sources:
- file: raw/2025-NatCom-Akerman-AI_in_HFpEF_external_validation.pdf
  citekey: akerman2025ai
page-type: source-summary-page
---
# External Validation of AI HFpEF Detection (EchoGo Heart Failure v2)

> Prospective external validation (n=240 HFpEF cases, 256 controls): AI echo model (EchoGo HF v2, Ultromics) achieves AUROC 0.797 vs H₂FPEF 0.788 with dramatically fewer intermediate classifications (9.1% vs 61.7% for H₂FPEF vs 54.2% for HFA-PEFF); AI-positive patients had HR 2.56 (1.46–4.51) for composite outcome — combined AI + clinical score approach outperforms any single tool.

**File:** `raw/2025-NatCom-Akerman-AI_in_HFpEF_external_validation.pdf` · **Authors:** Akerman AP et al. · **Year:** 2025 · **Journal:** Nature Communications 16:2915, DOI: 10.1038/s41467-025-58283-7

---

## Core Arguments

**Study type:** Prospective external validation; case-control design. Cases: HFpEF (n=240) from Beth Israel Deaconess Medical Center echocardiogram database 2018–2022. Controls: age/sex-matched (n=256). HFpEF defined: grade II–III diastolic dysfunction + HF symptoms + LVEF >50%. Baseline: age 74.2±12.4 years, 54.2% female, 68.3% White.

**AI model:** EchoGo Heart Failure v2 (Ultromics Ltd, UK) — 3D convolutional neural network trained on 2,971 HFpEF cases and 3,785 controls from echocardiographic video data. Outputs: continuous probability + categorical (negative/intermediate/positive). External validation tests generalisability beyond the development dataset.

**Discrimination (primary):**
- AI HFpEF AUROC: **0.797 (95% CI 0.756–0.799)**
- H₂FPEF score AUROC: **0.788 (95% CI 0.743–0.789)** — AI statistically superior (P=0.001)
- HFA-PEFF not directly AUROC-compared; lower sensitivity

**Sensitivity/Specificity:**
- AI: sensitivity **77.4%**, specificity **50.2%** — high sensitivity, lower specificity
- H₂FPEF: sensitivity **53.9%**, specificity **90.3%** — less sensitive, highly specific
- HFA-PEFF: sensitivity **63.2%**, specificity **98.5%** — most specific, least sensitive

**Key clinical advantage — intermediate classifications:**
- AI: **9.1%** intermediate (45/496 patients) — decisive classification in 91% of cases
- H₂FPEF: **61.7%** intermediate (306/496) — majority of patients fall in diagnostic grey zone
- HFA-PEFF: **54.2%** intermediate (269/496)
- The reduction from 61.7% to 9.1% intermediate classifications is the AI's primary clinical utility gain

**Prognostic value (median 25–35 months follow-up):**
- 45 HF hospitalisations (10.3%), 61 deaths (14.2%)
- AI-positive: **HR 2.56 (95% CI 1.46–4.51, P=0.001)** for composite outcome (HF hospitalisation + death)
- AI-intermediate: HR 1.49 (0.82–2.71)
- H₂FPEF score continuous: HR 3.15 (1.53–7.47, P=0.009)

**Clinical utility (decision curve analysis):**
- Combined approach (AI + H₂FPEF + HFA-PEFF scores) superior to any single tool across thresholds
- At 30% probability threshold: AI reduces unnecessary interventions vs H₂FPEF alone
- AI continuous probability integrates with clinical scores better than categorical replacement

**Calibration limitation:** AI model shows overestimation (intercept −0.56, slope 0.41) — tends to assign higher probabilities than observed event rates; requires recalibration for clinical deployment.

## Relevance to HFpEF Wiki

First external validation of a commercial AI echocardiography system for HFpEF. The 9.1% vs 61.7% intermediate rate is transformative for the diagnostic pipeline: the majority of patients currently requiring invasive exercise RHC to resolve H₂FPEF ambiguity could potentially be classified non-invasively. This addresses the fundamental scalability challenge of the HFA-PEFF/H₂FPEF algorithms.

The AI does not replace clinical scores but provides a complementary tool — high sensitivity makes it useful as a screening tool; H₂FPEF/HFA-PEFF provide high specificity for confirmation. Integrated pipeline: AI triage → clinical score → exercise RHC only for genuinely ambiguous residual cases.

This positions echocardiographic AI alongside ECG-AI ([[attia2019ecgaf]]) and deep learning echo ([[pandey2021deepnnecho]]) as part of a non-invasive ML diagnostic ecosystem for HFpEF.

## Connections
- Updates: [[ml-ai-hfpef]] — EchoGo HF v2 external validation: AUROC 0.797; 9.1% intermediate vs 61.7% H₂FPEF; HR 2.56 prognostic; calibration overestimation noted
- Updates: [[hfpef-diagnosis]] — AI echo reduces diagnostic grey zone from 62% to 9%; complement to H₂FPEF/HFA-PEFF rather than replacement
- Updates: [[echocardiography]] — AI-enhanced echo for HFpEF classification; EchoGo v2 sensitivity/specificity profile
- Complements: [[attia2019ecgaf]] — ECG-AI for AF vs echo-AI for HFpEF; parallel ML diagnostics
- Connects: [[reddy2024afhfpef]] — AI may triage when exercise RHC is truly needed (especially in AF where clinical scores fail)

## Related Pages
- Concepts: [[ml-ai-hfpef]], [[hfpef-diagnosis]], [[hfpef-diagnostic-definitions]]
- Entities: [[echocardiography]]
- Sources: [[attia2019ecgaf]], [[reddy2024afhfpef]], [[pandey2021deepnnecho]]

## Contradictions
AI achieves far higher sensitivity than HFA-PEFF (77.4% vs 63.2%) but much lower specificity (50.2% vs 98.5%) — different tools serve different positions in the diagnostic cascade (screening vs confirmation). Integration, not replacement, is the validated approach. Note in [[contradictions]].
