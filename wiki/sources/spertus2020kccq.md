---
title: 'Interpreting the Kansas City Cardiomyopathy Questionnaire in Clinical Trials
  and Clinical Care'
citekey: spertus2020kccq
year: 2020
authors: Spertus JA, Jones PG, Sandhu AT, Arnold SV
journal: J Am Coll Cardiol
tags:
- kccq
- quality-of-life
- outcome-measure
- mcid
- patient-reported-outcomes
- fda-qualification
- clinical-trials-methodology
- heart-failure
created: 2026-07-15
last_updated: 2026-07-15
sources:
- citekey: spertus2020kccq
  doi: 10.1016/j.jacc.2020.09.542
page-type: source-summary-page
---
# Spertus 2020 — Interpreting the KCCQ in Clinical Trials and Clinical Care

> [zotero-unverified] JACC State-of-the-Art Review by the KCCQ's developer group defining the instrument's item/domain/summary-score architecture, the anchor-based origin of the 5/10/20-point clinical-change thresholds, and the FDA's qualification of the KCCQ as a Clinical Outcome Assessment for drug/device approval.

**Full citation:**
Spertus JA, Jones PG, Sandhu AT, Arnold SV. Interpreting the Kansas City Cardiomyopathy Questionnaire in Clinical Trials and Clinical Care. *J Am Coll Cardiol.* 2020;76(20):2379–2390. doi:[10.1016/j.jacc.2020.09.542](https://doi.org/10.1016/j.jacc.2020.09.542)

---

## Core Arguments

**Instrument architecture (item/domain/summary-score structure):**
- The KCCQ was developed in 1996 (input from patients and clinicians) and published in 2000 (source: spertus2020kccq, citing Green et al. 2000); it uses a 2-week recall period and comprises **23 items mapping to 7 domains**: symptom frequency, symptom burden, symptom stability, physical limitations, social limitations, quality of life, and self-efficacy (source: spertus2020kccq).
- **Calculation/aggregation logic** (Central Illustration + Figure 2A):
  - Symptom frequency + symptom burden domains → merged into the **Total Symptom Score (TSS)**.
  - TSS + physical limitation domain → **Clinical Summary Score (CSS)**, which "mirrors the key concepts of NYHA functional class."
  - Symptom (frequency+burden) + physical limitation + social limitation + quality-of-life domains → **Overall Summary Score (OSS)**.
  - Symptom stability and self-efficacy domains feed a separate **KCCQ Self-Efficacy Scale**, not incorporated into either summary score.
  - All scores are rescaled 0–100 (higher = better); commonly binned in 25-point ranges (0–24 very poor–poor, 25–49 poor–fair, 50–74 fair–good, 75–100 good–excellent).
- **KCCQ-12 short form** (Spertus & Jones 2015, cited as ref. 10, not independently reviewed here): a 12-item reduction retaining symptom frequency, physical limitations, social limitations, and quality-of-life domains — **but dropping the symptom stability and self-efficacy domains/scales**, which are only available in the 23-item version. The 12-item version still generates CSS and OSS with "excellent concordance" to the full 23-item instrument's scores (source: spertus2020kccq). Figure 2B gives the analogous item→domain→summary-score mapping for the 12-item version (items 1a–1c physical limitation; items 2&5, 3&4 symptom frequency; items 6–7 quality of life; items 8a–8c social limitation).
- Item-level sensitivity: for KCCQ-23, a single one-category "shift" in patient response changes the physical limitation domain score by ~4.2 points, and moves the overall/clinical summary scores by smaller increments depending on which item shifted (range ~0.53–2.1 points per item response-shift on the 23-item version); reaching a 5-point summary-score change typically requires 3–5 category shifts across items (source: spertus2020kccq, Figure 2).

**Origin and derivation of the 5-point MCID/clinical-change thresholds:**
- The thresholds of **5, 10, and 20 points** (small-but-important, moderate-to-large, and large-to-very-large clinical change, respectively) were **not derived by distribution-based statistics** but by an explicit **anchor-based, multi-center study**: a "14-center study was explicitly designed to estimate these thresholds of clinically important change" (cited as Spertus et al., *Am Heart J* 2005;150:707–15) (source: spertus2020kccq).
- Method: clinicians rated patients' magnitude of clinical change using a **Physician Global Assessment** (categories: large/moderate/small-but-clinically-important deterioration, no change, small/moderate/large improvement), and these categories were correlated against mean KCCQ score changes (Figure 1). The mapping showed "great symmetry and proportionality" for both improvement and deterioration directions, and was "exceedingly similar" between the KCCQ-23 and KCCQ-12 overall summary scores.
- Secondary support for the same thresholds comes from prognostic-association studies (Kosiborod et al. 2007, cited as ref. 2): each 5-point KCCQ improvement was associated with ~10% relative reduction in cardiovascular mortality/all-cause hospitalization risk (linearly, with no threshold effect), and each 5-point KCCQ decrement with a comparable ~10% increase in risk — replicated in both HFpEF and HFrEF cohorts (cited as ref. 12) (source: spertus2020kccq). Table 1 in this paper also links 5/10/20-point KCCQ changes to correlated changes in 6-minute walk distance (112/225/450 m) and peak VO2 (2.5/5/10 mL/kg/min).

**FDA regulatory qualification (not a clinical-practice guideline):**
- The paper states that "both the cardiovascular drug and device divisions [of the FDA] have qualified the Kansas City Cardiomyopathy Questionnaire (KCCQ) as a Clinical Outcome Assessment (COA)," meaning drug/device approval and labeling claims can be obtained by demonstrating clinically important KCCQ improvement, independent of hard clinical events (source: spertus2020kccq, citing FDA COA Qualification Submission, DCTA form #0000084, April 16, 2020, and the FDA Medical Device Development Tool [MDDT] program statement).
- This is explicitly an **FDA regulatory/methodological qualification for trial endpoints**, not a professional-society (e.g., ACC/AHA/ESC) clinical-practice-guideline recommendation to administer KCCQ in routine care — the paper separately states, in its concluding section, that routine clinical/population-health use of KCCQ remains "more aspiration than reality" and that "more research and experience are needed" before it becomes standard clinical practice (source: spertus2020kccq).
- The paper notes CHIEF-HF (NCT04252287) as an example trial being launched to use KCCQ as its primary trial outcome, illustrating the practical consequence of the FDA COA qualification.

**Interpretive framework for trial reporting:**
- Argues that between-group **mean KCCQ differences** are frequently misapplied when interpreted against the MCID (the MCID is a within-patient concept, and applying it to between-group means risks a "misuse" when there is heterogeneity of treatment effect across patients, which the authors argue is the norm for patient-centered health status measures).
- Recommends reporting the **distribution of patients experiencing 5-, 10-, or 20-point changes** (responder analysis) alongside or instead of mean differences, and gives worked examples (DEFINE-HF, dapagliflozin) contrasting a "clinically unchanged" mean-difference conclusion with distributional differences in the proportions of patients worsening vs. improving.

## Relevance to HFpEF Wiki

This paper is the direct evidentiary source for filling two of the three explicit `[needs source]` gaps previously flagged on `wiki/entities/kansas-city-cardiomyopathy-questionnaire.md`: (1) the subscale item/domain/calculation structure of CSS/TSS/PLS/OSS, and (2) the origin of the 5-point MCID threshold. It also provides the first documented evidence of a **regulatory** (FDA COA) qualification of KCCQ, though this is explicitly not the same as a clinical-practice-guideline endorsement, so gap (3) is only partially addressed. It also directly substantiates the wiki's existing methodological-heterogeneity contradiction note (win ratio vs. ANCOVA/LS-mean-difference approaches to KCCQ across trials; see `wiki/contradictions.md`), since this paper is the primary argument, from the KCCQ's own developer, for why mean-difference reporting alone is an interpretive "misuse" of the MCID.

## Connections

- Supplies the mechanistic/structural backbone for every KCCQ subscale figure already tabulated on [[kansas-city-cardiomyopathy-questionnaire]] (CSS in EMPEROR-Preserved/STEP-HFpEF/STEP-HFpEF DM/SUMMIT; TSS in DAPA-HF/EMPULSE/FINEARTS-HF; PLS in SOCRATES-PRESERVED/VITALITY-HFpEF; OSS in STEP-HFpEF DM/CAPACITY-HFpEF).
- Provides the anchor-based derivation underlying every "≥5-point responder" or MCID claim made across trial source pages in this wiki (e.g., Udelson2020CAPACITY, Voors2022EMPULSE, Armstrong2020VITALITY).

## Connections
- Cites: [[anker2021emperor]] — EMPEROR-Preserved named as a KCCQ-CSS-reporting trial
- Cites: [[kosiborod2024stephfpefdm]] — STEP-HFpEF DM named as a KCCQ-CSS and OSS reporting trial
- Cites: [[mcmurray2019dapahf]] — DAPA-HF named as a KCCQ-TSS reporting trial
- Cites: [[solomon2024finearts]] — FINEARTS-HF named as a KCCQ-TSS reporting trial
- Cites: [[pieske2017socrates]] — SOCRATES-PRESERVED named as a KCCQ-PLS reporting trial

## Related Pages

- Entities: [[kansas-city-cardiomyopathy-questionnaire]], [[step-hfpef]], [[summit]], [[finearts-hf]], [[sglt2-inhibitors]]
- Sources: [[udelson2020capacity]], [[voors2022empulse]], [[armstrong2020vitality]]

## Contradictions

- Reinforces, rather than creates, the existing wiki contradiction on methodological heterogeneity in KCCQ analysis (win ratio vs. mean-difference approaches; see `wiki/contradictions.md` #16 and the Contradictions section of [[kansas-city-cardiomyopathy-questionnaire]]) — this paper is the primary methodological argument (from the KCCQ's own developer) that mean-difference-only reporting of KCCQ can misrepresent clinical benefit absent responder-distribution data.
