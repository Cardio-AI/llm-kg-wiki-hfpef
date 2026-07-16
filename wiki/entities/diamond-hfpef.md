---
title: DIAMOND-HFpEF
summary: "Single-centre prospective CMR study (n=101 HFpEF, 43 controls; Leicester, UK) showing 70% prevalence of microvascular dysfunction (MPR <2.0) in HFpEF, that impaired myocardial perfusion reserve independently predicts death/HF hospitalisation, and that microvascular dysfunction and diffuse myocardial fibrosis (ECV) are statistically uncorrelated, independent prognostic mechanisms."
entity_type: trial
tags:
  - trial
  - hfpef
  - coronary-microvascular-dysfunction
  - cardiac-mri
  - fibrosis
created: 2026-07-15
last_updated: 2026-07-15
sources:
  - citekey: Arnold2022DIAMOND
    doi: 10.1016/j.jcmg.2021.10.002
page-type: entity-page
---
# DIAMOND-HFpEF

> CMR-based multiparametric study demonstrating that microvascular dysfunction (measured as myocardial perfusion reserve, MPR) is present in 70% of HFpEF patients, independently predicts adverse outcomes, and — critically — is not correlated with diffuse myocardial fibrosis (ECV), identifying microvascular dysfunction and fibrosis as two distinct, additive prognostic pathways rather than a single causal cascade.

---

## Aliases
| Alias | Type | Notes |
|---|---|---|
| DIAMOND-HFpEF | research-name | study group name used in [[arnold2022diamond]] |
| NCT03050593 | Trial-ID | registered on clinicaltrials.gov |

---

## Description

- **Study type:** Single-centre prospective observational cohort with matched controls
- **Site:** University Hospitals of Leicester NHS Trust, UK
- **N:** 101 HFpEF patients + 43 healthy age/sex-matched controls
- **Population:** HFpEF (ESC criteria; LVEF ≥50%); no obstructive coronary artery disease (excluded by CT or angiography); stable outpatients
- **Baseline HFpEF cohort:** age 73±9 years, 48% male, BMI 34±7 kg/m², LVEF 56%, AF 44%, hypertension 90%, diabetes 49%, BNP median 135 (IQR 66–239) pg/mL, E/e′ 13±5
- **CMD measurement:** Adenosine stress cardiac MRI myocardial perfusion reserve (MPR = hyperaemic:rest myocardial blood flow ratio); microvascular dysfunction (MVD) defined as MPR <2.0
- **Follow-up:** Median 3.1 years; 45 composite events (31 HF hospitalisations, 25 deaths)
- **Full paper stub:** [[arnold2022diamond]]

(source: arnold2022diamond)

## Role in HFpEF

DIAMOND-HFpEF is a primary evidentiary source for [[microvascular-dysfunction]] and directly informs the [[hfpef-fibrosis-paradigm]] concept page. Its central contribution is demonstrating that coronary microvascular dysfunction (CMD) is highly prevalent in HFpEF even in the absence of obstructive CAD — an intrinsic feature of the syndrome rather than a downstream consequence of epicardial disease — and that CMD is independently prognostic. Its most mechanistically important finding is that MPR and diffuse fibrosis (ECV) are statistically uncorrelated (r=−0.06, P=0.638), which challenges a simple sequential model (CMD → fibrosis → adverse outcomes) in favour of two parallel, additive pathological processes. (source: arnold2022diamond)

This complements [[shah2018promis]] (PROMIS-HFpEF; 75% CMD prevalence by Doppler coronary flow reserve) as a second, methodologically distinct (CMR-based) confirmation of high CMD prevalence in HFpEF, and is cited as the highest-priority reference in the CMD meta-analysis [[lin2023cmd]].

## Evidence

- **MPR:** 1.74 ± 0.76 (HFpEF) vs. 2.22 ± 0.76 (controls); P=**0.001**
- **MVD prevalence (MPR <2.0):** **70%** HFpEF vs. 48% controls; P=**0.014**
- **MPR independently predicts composite (death or HF hospitalisation) across 3 fully adjusted models:**
  - Clinical model (age, sex, HTN, DM, AF, BMI, NYHA): HR **0.673** per SD increase in MPR (P=0.038)
  - Blood biomarker model (+ troponin, BNP): HR **0.694** (P=0.039)
  - Full imaging model (+ LVEF, ECV, LGE, LV mass): HR **0.690** (P=0.034)
- **Optimal MPR cut-off:** 1.82 (by ROC); Kaplan-Meier log-rank P=**0.020** — significant survival separation
- **MPR vs. ECV (diffuse fibrosis) correlation:** r=**−0.06**, P=**0.638** — no correlation
- **MPR vs. iECV correlation:** r=−0.10, P=0.473 — no correlation
- **MPR in LGE-positive vs. LGE-negative patients:** not significantly different — focal fibrosis does not predict MPR severity
- Both ECV (diffuse fibrosis) and MPR are independently prognostic, contributing separately rather than in series

(source: arnold2022diamond)

## Status

**Published (2022, JACC Cardiovascular Imaging).** Limitations noted in the source: single centre with modest N, limiting power for event-driven subgroup analyses; MPR reflects combined vasomotor reactivity and structural change rather than direct microvascular resistance; controls (N=43) were not fully matched for all cardiometabolic comorbidities (48% MVD prevalence even in controls suggests possible subclinical disease or measurement overlap); no functional testing (KCCQ, 6MWT) was reported alongside CMR, so symptom-CMD correlation was not assessed; and the observational design precludes causal inference between MVD and outcomes. (source: arnold2022diamond)

## Related Pages
- Concepts: [[microvascular-dysfunction]], [[coronary-microvascular-dysfunction]], [[myocardial-fibrosis]], [[hfpef-fibrosis-paradigm]], [[cardiac-mri]]
- Entities: [[hfpef]]
- Sources: [[arnold2022diamond]], [[shah2018promis]], [[lin2023cmd]], [[damario2019cmd]], [[ipek2024cmr]], [[lange2024cmr]]

## Contradictions
MPR (microvascular dysfunction severity) and ECV (diffuse myocardial fibrosis) are not correlated (r=−0.06, P=0.638), yet both independently predict adverse outcomes. This challenges a simple causal chain (CMD → fibrosis → adverse outcomes) and instead suggests two parallel and additive pathological processes — a mechanistically important tension already flagged in `wiki/contradictions.md` and in [[hfpef-fibrosis-paradigm]]. See [[contradictions]].

## References
- Arnold JR, Kanagala P, Budgeon CA, Jerosch-Herold M, Gulsin GS, Singh A, Khan JN, Chan DCS, Squire IB, Ng LL, McCann GP. Prevalence and Prognostic Significance of Microvascular Dysfunction in Heart Failure With Preserved Ejection Fraction. *JACC Cardiovasc Imaging.* 2022;15(6):1001–1011. doi:[10.1016/j.jcmg.2021.11.022](https://doi.org/10.1016/j.jcmg.2021.11.022)
