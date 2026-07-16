---
title: Kansas City Cardiomyopathy Questionnaire
summary: "Patient-reported, heart-failure-specific quality-of-life instrument scored\
  \ 0–100 (higher = better), used as a primary, co-primary, or secondary/exploratory\
  \ endpoint across nearly all major HFpEF pharmacological and lifestyle RCTs cited\
  \ in this wiki, reported via multiple named subscales (CSS, TSS, PLS, OSS)."
entity_type: score
tags:
  - outcome-measure
created: 2026-07-15
last_updated: 2026-07-15
sources:
  - citekey: McMurray2019DAPAHF
    doi: 10.1056/NEJMoa1911303
  - citekey: Anker2021EMPEROR
    doi: 10.1056/NEJMoa2107038
  - citekey: Kosiborod2024STEPHFPEFDM
    doi: 10.1056/NEJMoa2313307
  - citekey: Armstrong2020VITALITY
    doi: 10.1001/jama.2020.15922
  - citekey: Voors2022EMPULSE
    doi: 10.1038/s41591-021-01659-1
  - citekey: Udelson2020CAPACITY
    doi: 10.1001/jama.2020.16641
  - citekey: spertus2020kccq
    doi: 10.1016/j.jacc.2020.09.542
page-type: entity-page
---
# Kansas City Cardiomyopathy Questionnaire

> Patient-reported heart-failure-specific quality-of-life instrument, scored 0–100 with higher scores indicating better health status; reported across DAPA-HF, EMPEROR-Preserved, STEP-HFpEF/STEP-HFpEF DM, SUMMIT, FINEARTS-HF, SOCRATES-PRESERVED/VITALITY-HFpEF, EMPULSE, CAPACITY-HFpEF, and SECRET via several named subscales (CSS, TSS, PLS, OSS).

## Aliases
| Alias | Type | Notes |
|---|---|---|
| KCCQ | abbreviation | Kansas City Cardiomyopathy Questionnaire — universal shorthand used across all cited trials |
| KCCQ-CSS | abbreviation | Clinical Summary Score subscale — used in EMPEROR-Preserved, STEP-HFpEF, STEP-HFpEF DM, SUMMIT |
| KCCQ-TSS | abbreviation | Total Symptom Score subscale — used in DAPA-HF, EMPULSE, FINEARTS-HF |
| KCCQ-PLS | abbreviation | Physical Limitation Scale subscale — used in SOCRATES-PRESERVED / VITALITY-HFpEF |
| KCCQ-OSS | abbreviation | Overall Summary Score subscale — used in STEP-HFpEF DM, CAPACITY-HFpEF |

---

## Description

The KCCQ is a self-administered questionnaire producing a quality-of-life/health-status score on a 0–100 scale, with higher scores indicating better status: "KCCQ (quality of life; range 0–100, higher=better)" is the explicit description given in the SECRET trial protocol summary (source: Kitzman2016SECRET). The instrument was developed in 1996 (published 2000) with a 2-week recall period and comprises **23 items mapping to 7 domains**: symptom frequency, symptom burden, symptom stability, physical limitations, social limitations, quality of life, and self-efficacy (source: spertus2020kccq). Domains combine into the named subscales as follows: the symptom frequency and symptom burden domains merge into the **Total Symptom Score (TSS)**; TSS plus the physical limitation domain forms the **Clinical Summary Score (CSS)**, which "mirrors the key concepts of NYHA functional class"; and symptom (frequency+burden) + physical limitation + social limitation + quality-of-life domains together form the **Overall Summary Score (OSS)**. Symptom stability and self-efficacy feed a separate self-efficacy scale not incorporated into either summary score (source: spertus2020kccq). A reduced **12-item short form (KCCQ-12)** retains the symptom frequency, physical limitations, social limitations, and quality-of-life domains — dropping symptom stability and self-efficacy, which are only available in the 23-item version — and generates CSS/OSS with "excellent concordance" to the full-length instrument's scores (source: spertus2020kccq). This resolves the domain-structure/calculation gap for CSS, TSS, and OSS. The **Physical Limitation Scale (PLS)** used as a standalone endpoint (e.g., VITALITY-HFpEF) corresponds to the physical limitation domain score itself; spertus2020kccq does not separately name or discuss a "PLS" as distinct from the physical limitation domain, so this specific terminological equivalence is inferred rather than explicitly stated in the source. [needs source: explicit confirmation that trial-reported "PLS" is identical to the physical-limitation-domain score as defined in spertus2020kccq]

A change of **≥5 points** is treated as a clinically meaningful threshold ("responder" definition) in multiple independently reported trials: CAPACITY-HFpEF defines "KCCQ responders (≥5-point improvement)" (source: Udelson2020CAPACITY); EMPULSE defines its win-ratio component as "KCCQ-TSS change ≥5 points" and separately reports "≥10-point improvement" (source: Voors2022EMPULSE); VITALITY-HFpEF explicitly states the placebo-arm KCCQ-PLS improvement of +6.9 points "exceeds MCID of 5 points" (source: Armstrong2020VITALITY). The 5/10/20-point thresholds (small, moderate-to-large, and large-to-very-large clinical change, respectively) originate from an **anchor-based, 14-center study** (Spertus et al., *Am Heart J* 2005) that correlated physicians' global assessment of patients' clinical change (7-point scale from large deterioration to large improvement) against mean KCCQ score differences; the mapping showed "great symmetry and proportionality" for both improvement and deterioration and was "exceedingly similar" between the KCCQ-23 and KCCQ-12 overall summary scores (source: spertus2020kccq). Independent prognostic-association evidence supports the same 5-point increment: each 5-point KCCQ improvement is associated with a ~10% relative reduction in cardiovascular mortality/all-cause hospitalization risk (and each 5-point decrement with a comparable ~10% increased risk), linearly and without a threshold effect, replicated in both HFpEF and HFrEF cohorts (source: spertus2020kccq, citing Kosiborod et al. 2007). This resolves the origin-of-MCID gap.

## Role in HFpEF

KCCQ is used across markedly different endpoint roles depending on the trial:

- **Co-primary endpoint:** STEP-HFpEF and STEP-HFpEF DM used KCCQ-CSS change at 52 weeks as one of two dual primary endpoints (source: Kosiborod2024STEPHFPEFDM); SUMMIT used KCCQ-CSS change at 52 weeks as one of two co-primary endpoints alongside the CV death/worsening-HF event endpoint (source: [[summit]]).
- **Primary endpoint:** SOCRATES-PRESERVED used exploratory KCCQ-CSS as a non-co-primary but headline exploratory endpoint (source: Pieske2017SOCRATES); its phase 3 successor VITALITY-HFpEF used KCCQ-PLS change as the sole primary endpoint (source: Armstrong2020VITALITY).
- **Component of a hierarchical win-ratio composite:** DAPA-HF (KCCQ total symptom score win ratio 1.18, HFrEF) and EMPULSE (KCCQ-TSS as the fourth and dominant tier of a four-level hierarchical win ratio: death > HF event frequency > time to first HF event > KCCQ-TSS ≥5-point change) both incorporate KCCQ within a hierarchical composite rather than analysing it as an independent endpoint (source: McMurray2019DAPAHF; source: Voors2022EMPULSE).
- **Secondary/exploratory endpoint:** EMPEROR-Preserved (KCCQ-CSS change at 52 weeks, secondary, hierarchically tested), FINEARTS-HF (KCCQ-TSS change, secondary), and CAPACITY-HFpEF (KCCQ-OSS change, exploratory, not corrected for multiplicity) all report KCCQ as a lower-tier endpoint (source: Anker2021EMPEROR; source: [[finearts-hf]]; source: Udelson2020CAPACITY).
- **Non-pharmacological trials:** SECRET used KCCQ as an exploratory/secondary QoL measure (co-primary was the Minnesota Living with Heart Failure Questionnaire, not KCCQ) and found a diet-specific benefit (+7 points, P=0.004) not replicated by exercise alone (source: Kitzman2016SECRET). REHAB-HF reported KCCQ as a secondary functional/QoL outcome (+7.1 points more with rehabilitation) (source: [[kitzman2021rehabhf]]).

In the EMPULSE win-ratio breakdown, KCCQ-TSS was numerically the dominant tier determining wins/losses (35.9% of empagliflozin comparisons vs. 27.5% for placebo, out of the total hierarchical comparisons), a methodological point the trial's own limitations section flags: the trial "was not powered for individual components" of the hierarchy (source: Voors2022EMPULSE).

## Evidence

| Trial | Subscale | Result | P | Source |
|---|---|---|---|---|
| DAPA-HF (HFrEF) | TSS (win ratio component) | LS change +6.1±18.6 (dapa) vs. +3.3±19.2 (placebo); win ratio 1.18 (1.11–1.26) | <0.001 | McMurray2019DAPAHF |
| EMPEROR-Preserved | CSS | +4.51 pts (empagliflozin) vs. +3.18 pts (placebo); diff +1.32 (0.45–2.19) | — | Anker2021EMPEROR |
| STEP-HFpEF (non-DM) | CSS | +16.6 (sema) vs. +8.7 (placebo); diff +7.8 (4.8–10.9) | <0.001 | [[step-hfpef]] |
| STEP-HFpEF DM | CSS | +13.7 (sema) vs. +6.4 (placebo); diff +7.3 (4.1–10.4) | <0.001 | Kosiborod2024STEPHFPEFDM |
| SUMMIT | CSS | +19.5±1.2 (tirzepatide) vs. +12.7±1.3 (placebo); diff +6.9 (3.3–10.6) | <0.001 | [[summit]] |
| FINEARTS-HF | TSS | +8.0 pts (finerenone) vs. +6.4 pts (placebo); diff +1.6 (0.8–2.3) | <0.001 | [[finearts-hf]] |
| SOCRATES-PRESERVED (phase 2b, exploratory) | CSS | +9.2 pts (vericiguat 10 mg) vs. placebo | 0.016 | Pieske2017SOCRATES |
| VITALITY-HFpEF (phase 3, primary) | PLS | LS diff −1.5 (15 mg, P=0.47); −0.5 (10 mg, P=0.80) — both neutral; placebo arm alone +6.9 pts | 0.47 / 0.80 | Armstrong2020VITALITY |
| EMPULSE | TSS (win ratio tier + adjusted mean) | Adj. mean change 36.19 (empagliflozin) vs. 31.73 (placebo); diff +4.45 (0.32–8.59) | — | Voors2022EMPULSE |
| CAPACITY-HFpEF (exploratory) | OSS | −7.2 pts (praliciguat) vs. placebo — worse on active drug; responders (≥5pt) 41% vs. 63% | 0.007 | Udelson2020CAPACITY |
| SECRET | Total score | Diet +7 pts (P=0.004); exercise +3 pts (P=0.43, not significant) | 0.004 (diet) | Kitzman2016SECRET |
| FAIR-HFpEF (small, underpowered) | OSS | +6.5±5.1 pts, not significant | 0.21 | [[fair-hfpef]] |

## Status

KCCQ is the most widely used patient-reported outcome instrument across the HFpEF pharmacological trial literature cited in this wiki, spanning SGLT2 inhibitors, GLP-1/GIP receptor agonists, non-steroidal MRA, sGC stimulators, and diet/exercise interventions. Both the cardiovascular **drug and device divisions of the U.S. FDA have qualified the KCCQ as a Clinical Outcome Assessment (COA)**, meaning drug/device approval and labeling claims can be obtained by demonstrating clinically important KCCQ improvement independent of hard clinical events (source: spertus2020kccq, citing FDA COA Qualification Submission, DCTA #0000084, April 2020, and the FDA MDDT program). This is a **regulatory/trial-endpoint qualification, not a professional-society clinical-practice guideline recommendation** — spertus2020kccq itself states that routine clinical/population-health use of KCCQ remains "more aspiration than reality" pending further research (source: spertus2020kccq). No source cited in this wiki documents an ACC/AHA/ESC or other clinical-practice-guideline endorsement of KCCQ for routine care decision-making; this narrower gap remains open. [needs source: clinical-practice-guideline (not regulatory) endorsement of KCCQ]

The instrument's subscale item composition, domain structure, and MCID derivation are now documented via spertus2020kccq (see Description, above). The KCCQ's original psychometric **validation study** (development, reliability, and responsiveness testing) is still not independently reviewed in this wiki — spertus2020kccq only cites it (Green et al. 2000, *J Am Coll Cardiol* 35:1245–55) as prior work rather than reporting its methods/results in detail. [needs source: original KCCQ validation study (Green 2000) not yet ingested]

## Related Pages

- Concepts: [[exercise-intolerance]], [[hfpef-treatment-gap]], [[hfpef-phenotype-profiling]]
- Entities: [[six-minute-walk-test]], [[minnesota-living-with-heart-failure-questionnaire]], [[short-physical-performance-battery]], [[step-hfpef]], [[summit]], [[finearts-hf]], [[vitality-hfpef]], [[socrates-preserved]], [[empulse]], [[sglt2-inhibitors]], [[hfpef]]
- Sources: [[mcmurray2019dapahf]], [[anker2021emperor]], [[kosiborod2024stephfpefdm]], [[pieske2017socrates]], [[armstrong2020vitality]], [[voors2022empulse]], [[udelson2020capacity]], [[kitzman2016secret]], [[spertus2020kccq]]

## Contradictions

- **CAPACITY-HFpEF KCCQ worsening (P=0.007) despite mechanistic enrichment:** praliciguat targeted a hypothesised NO-deficiency phenotype yet significantly worsened KCCQ-OSS relative to placebo, with fewer 6-MWT responders on active drug — a paradoxical harm signal in the very subgroup the drug was designed for (source: Udelson2020CAPACITY). See [[contradictions]].
- **SOCRATES-PRESERVED exploratory KCCQ signal not replicated in VITALITY-HFpEF:** phase 2b KCCQ-CSS improvement at 10 mg vericiguat (P=0.016) did not translate into a phase 3 primary-endpoint benefit on KCCQ-PLS (P=0.47 at 15 mg; P=0.80 at 10 mg) — a clear surrogate-to-outcome translation failure (source: Pieske2017SOCRATES; source: Armstrong2020VITALITY). See [[contradictions]].
- **Large placebo response inflating apparent "meaningful improvement":** in VITALITY-HFpEF, the placebo arm alone improved KCCQ-PLS by +6.9 points — exceeding the 5-point MCID — driven by natural post-decompensation recovery, illustrating that a within-arm "clinically meaningful" change does not imply a between-arm treatment effect (source: Armstrong2020VITALITY).
- **Methodological heterogeneity in how KCCQ change is analysed:** win ratio (DAPA-HF, EMPULSE) vs. ANCOVA/LS-mean difference (EMPEROR-Preserved, STEP-HFpEF, SUMMIT, FINEARTS-HF) are not directly comparable, and the wiki separately documents a case (DELIVER vs. DETERMINE-Preserved, same drug) where win-ratio and absolute-change analyses of KCCQ produced discordant conclusions — see `wiki/contradictions.md` #16.

## References
- McMurray JJV, Solomon SD, Inzucchi SE, et al.; DAPA-HF Trial Committees and Investigators. Dapagliflozin in Patients with Heart Failure and Reduced Ejection Fraction. *N Engl J Med.* 2019;381(21):1995–2008. doi:[10.1056/NEJMoa1911303](https://doi.org/10.1056/NEJMoa1911303)
- Anker SD, Butler J, Filippatos G, et al.; EMPEROR-Preserved Trial Investigators. Empagliflozin in Heart Failure with a Preserved Ejection Fraction. *N Engl J Med.* 2021;385(16):1451–1461. doi:[10.1056/NEJMoa2107038](https://doi.org/10.1056/NEJMoa2107038)
- Kosiborod MN, Petrie MC, Borlaug BA, et al.; STEP-HFpEF DM Trial Committees and Investigators. Semaglutide in Patients with Obesity-Related Heart Failure and Type 2 Diabetes. *N Engl J Med.* 2024;390(15):1394–1407. doi:[10.1056/NEJMoa2313307](https://doi.org/10.1056/NEJMoa2313307)
- Pieske B, Maggioni AP, Lam CSP, et al. Vericiguat in patients with worsening chronic heart failure and preserved ejection fraction: results of the SOCRATES-PRESERVED study. *Eur Heart J.* 2017;38(15):1119–1127. doi:[10.1093/eurheartj/ehw593](https://doi.org/10.1093/eurheartj/ehw593)
- Armstrong PW, Lam CSP, Anstrom KJ, et al.; VITALITY-HFpEF Study Group. Effect of Vericiguat vs Placebo on Quality of Life in Patients with Heart Failure and Preserved Ejection Fraction: The VITALITY-HFpEF Randomized Clinical Trial. *JAMA.* 2020;324(15):1512–1521. doi:[10.1001/jama.2020.15922](https://doi.org/10.1001/jama.2020.15922)
- Voors AA, Angermann CE, Teerlink JR, et al. The SGLT2 inhibitor empagliflozin in patients hospitalized for acute heart failure: a multinational randomized trial. *Nat Med.* 2022;28:568–574. doi:[10.1038/s41591-021-01659-1](https://doi.org/10.1038/s41591-021-01659-1)
- Udelson JE, Lewis GD, Shah SJ, et al. Effect of Praliciguat on Peak Rate of Oxygen Consumption in Patients With Heart Failure With Preserved Ejection Fraction: The CAPACITY HFpEF Randomized Clinical Trial. *JAMA.* 2020;324(15):1522–1531. doi:[10.1001/jama.2020.16641](https://doi.org/10.1001/jama.2020.16641)
- Kitzman DW, Brubaker P, Morgan T, et al. Effect of Caloric Restriction or Aerobic Exercise Training on Peak Oxygen Consumption and Quality of Life in Obese Older Patients With Heart Failure With Preserved Ejection Fraction: A Randomized Clinical Trial. *JAMA.* 2016;315(1):36–46. doi:[10.1001/jama.2015.17346](https://doi.org/10.1001/jama.2015.17346)
- Spertus JA, Jones PG, Sandhu AT, Arnold SV. Interpreting the Kansas City Cardiomyopathy Questionnaire in Clinical Trials and Clinical Care. *J Am Coll Cardiol.* 2020;76(20):2379–2390. doi:[10.1016/j.jacc.2020.09.542](https://doi.org/10.1016/j.jacc.2020.09.542)
