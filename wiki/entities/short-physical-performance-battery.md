---
title: Short Physical Performance Battery
summary: "Standardised, validated three-component physical-function measure (standing\
  \ balance, gait speed, chair-stand strength; 0–12 total, lower = worse function)\
  \ used as the primary endpoint in REHAB-HF, the only large RCT of post-hospitalisation\
  \ multidomain rehabilitation across the HF ejection-fraction spectrum in this wiki."
entity_type: score
tags:
  - outcome-measure
created: 2026-07-15
last_updated: 2026-07-15
sources:
  - citekey: Kitzman2021REHABHF
    doi: 10.1056/NEJMoa2026141
  - citekey: mentz2021rehabhfhfpef
    doi: 10.1016/j.jchf.2021.05.007
page-type: entity-page
---
# Short Physical Performance Battery

> Standardised, validated global physical-function measure with three components — standing balance, gait speed (4-metre walk), and chair-stand strength — each scored 0–4, summed to a 0–12 total with lower scores indicating more severe physical dysfunction; used as the primary endpoint of REHAB-HF, and its HFpEF/HFrEF subgroup analysis, in frail older patients hospitalised for acute decompensated heart failure.

## Aliases
| Alias | Type | Notes |
|---|---|---|
| SPPB | abbreviation | Short Physical Performance Battery — used throughout REHAB-HF and its subgroup analysis |

---

## Description

The SPPB is described in the REHAB-HF primary results paper as "a standardized, reproducible measure of global physical function that has been validated in frail, older persons and predicts a wide range of clinical outcomes." It has three components: "a standing balance test, a gait-speed (4-m walk) test, and a strength test (as assessed by the time needed to rise from a chair five times). Each component is scored on a scale of 0 to 4; the sum of the scores ranges from 0 to 12, with lower scores indicating more physical dysfunction" (source: Kitzman2021REHABHF, raw PDF). The REHAB-HF HFpEF/HFrEF subgroup analysis independently confirms this structure: "It has 3 components (standing balance, gait speed, and strength), which each scored 0-4 for a total score ranging from 0 to 12, with lower scores indicating more severe physical dysfunction" (source: mentz2021rehabhfhfpef, raw PDF).

The minimal clinically important difference (MCID) for SPPB is stated as **0.5 points** in the wiki source summary for REHAB-HF's main results, against which the trial's observed +1.5-point between-group difference is described as "approximately 3× the MCID" (source: [[kitzman2021rehabhf]]).

## Role in HFpEF

- **Primary endpoint:** REHAB-HF used SPPB change at 3 months as its sole primary endpoint in 349 patients ≥60 years hospitalised for acute decompensated heart failure across the full ejection-fraction spectrum (53% HFpEF, defined as LVEF ≥45%) (source: Kitzman2021REHABHF).
- **Subgroup primary re-analysis:** the pre-specified Mentz 2021 EF-subgroup analysis re-examined SPPB change separately in HFpEF (n=185) vs. HFrEF (n=164), finding a nominally larger improvement in HFpEF (+1.9 pts, 95% CI 1.1–2.6) than HFrEF (+1.1 pts, 0.3–1.9), though the interaction P was not significant (P=0.25) (source: mentz2021rehabhfhfpef).
- **Component of a global rank composite endpoint:** both papers also use SPPB as the lowest tier of a hierarchical "global rank" endpoint (death > all-cause rehospitalisation > 3-month SPPB score), analysed via probability index; this composite was significant in the HFpEF subgroup (probability index 0.59, P=0.04) but not in HFrEF (0.50, P=0.69), with a non-significant EF interaction (P=0.098) (source: mentz2021rehabhfhfpef).

SPPB is, in this wiki, specific to the post-hospitalisation/frailty rehabilitation context — distinct from the outpatient, stable-HFpEF exercise trials that use peak VO₂ (OptimEx-Clin) or 6MWD (SECRET, FAIR-HFpEF) as primary endpoints. REHAB-HF's population was markedly more frail (97% frail or pre-frail, mean 5 comorbidities) than typical outpatient exercise-training cohorts (source: [[kitzman2021rehabhf]]; source: [[supervised-exercise-training]]).

## Evidence

| Analysis | Result | P | Source |
|---|---|---|---|
| REHAB-HF overall (primary) | Rehab 8.3 vs. usual care 6.9; diff +1.5 (0.9–2.0), ~3× the 0.5-point MCID | <0.001 | Kitzman2021REHABHF |
| REHAB-HF HFpEF subgroup | +1.9 (1.1–2.6) | — | mentz2021rehabhfhfpef |
| REHAB-HF HFrEF subgroup | +1.1 (0.3–1.9) | — | mentz2021rehabhfhfpef |
| HFpEF vs. HFrEF interaction (SPPB) | Not significant | 0.25 | mentz2021rehabhfhfpef |
| Global rank endpoint, HFpEF (death + rehosp. + SPPB) | Probability index 0.59 | 0.04 | mentz2021rehabhfhfpef |
| Global rank endpoint, HFrEF | Probability index 0.50 | 0.69 | mentz2021rehabhfhfpef |
| Global rank endpoint, EF interaction | Not significant | 0.098 | mentz2021rehabhfhfpef |

## Status

SPPB is, in this wiki, used exclusively within the REHAB-HF trial programme (main results plus its pre-specified EF-subgroup analysis) — no other cited HFpEF trial uses it as an endpoint. Its use here reflects a frailty/geriatric-functional-assessment orientation distinct from the cardiopulmonary/metabolic orientation of peak VO₂-based exercise trials. The 2022 AHA/ACC/HFSA guideline context is noted as consistent with a Class I, Level A recommendation for exercise training across the EF spectrum, which REHAB-HF is cited as supporting specifically for the post-hospitalisation window (source: [[rehab-hf]]).

## Related Pages

- Concepts: [[exercise-intolerance]]
- Entities: [[six-minute-walk-test]], [[kansas-city-cardiomyopathy-questionnaire]], [[rehab-hf]], [[supervised-exercise-training]], [[cardiopulmonary-exercise-testing]], [[hfpef]], [[hfref]]
- Sources: [[kitzman2021rehabhf]], [[mentz2021rehabhfhfpef]]

## Contradictions

- **EF-interaction non-significance despite a suggestive pattern:** the global rank endpoint interaction P=0.098 and the SPPB-specific interaction P=0.25 mean the apparently larger HFpEF benefit is not formally established as EF-specific — REHAB-HF was not powered to test this interaction, and the finding is explicitly flagged in the wiki as "suggestive but not formally significant" (source: [[rehab-hf]]). See [[contradictions]].
- **Functional improvement without hard-outcome benefit:** SPPB (and 6MWD) improved significantly while 60-day all-cause rehospitalisation did not differ (RR 0.93, 95% CI 0.66–1.19) — consistent with a broader pattern in this wiki of surrogate/functional improvement dissociating from hospitalisation/mortality endpoints in HFpEF trials (source: Kitzman2021REHABHF).

## References
- Kitzman DW, Whellan DJ, Duncan P, et al.; REHAB-HF Trial Investigators. Physical Rehabilitation for Older Patients Hospitalized for Heart Failure. *N Engl J Med.* 2021;385(3):203–216. doi:[10.1056/NEJMoa2026141](https://doi.org/10.1056/NEJMoa2026141)
- Mentz RJ, Whellan DJ, Duncan PW, et al. Heart Failure With Preserved vs Reduced Ejection Fraction in the REHAB-HF Trial. *JACC Heart Fail.* 2021;9(10):747–757. doi:[10.1016/j.jchf.2021.05.007](https://doi.org/10.1016/j.jchf.2021.05.007)
