---
type: entity
title: Atrial Fibrillation (AF)
summary: The most common sustained cardiac arrhythmia; both a cause and consequence of HFpEF; associated with elevated LA pressure, atrial fibrosis, and worse outcomes; requires adjusted diagnostic thresholds for natriuretic peptides and LA volume index in HFpEF workup; exercise RHC is the only reliable HFpEF diagnostic in AF.
entity_type: comorbidity
tags:
  - atrial-fibrillation
  - arrhythmia
  - hfpef
  - comorbidity
created: 2026-04-30
last_updated: 2026-05-15
sources:
  - file: raw/2021-ESC-Guidelines-Heart-Failure.pdf
    citekey: McDonagh2021ESC
  - file: raw/2023-ESC-Anker_HFpEF_phenotyping.pdf
    citekey: Anker2023HFpEFPhenotype
  - file: raw/2024-NEJM_Reddy-AF_HFpEF_study.pdf
    citekey: reddy2024afhfpef
---
# Atrial Fibrillation

> The most common sustained cardiac arrhythmia; both a driver and consequence of HFpEF via elevated LA pressure and atrial fibrosis; requires adjusted diagnostic thresholds in HFpEF workup.

---

## Aliases
| Alias | Type | Notes |
|---|---|---|
| AF | abbreviation | universal clinical shorthand |
| AFib | abbreviation | American English informal |
| atrial flutter | alternate-name | distinct arrhythmia; often grouped with AF clinically; higher NP thresholds apply to both |
| paroxysmal AF | alternate-name | intermittent subtype; may be missed at time of HFpEF workup |
| persistent AF | alternate-name | sustained subtype; associated with worse LA remodelling |

---

## Description

Atrial fibrillation (AF) is an irregular, chaotic atrial rhythm resulting from disorganised electrical activity. It is characterised by the absence of coordinated atrial contractions, leading to variable ventricular filling and reduced cardiac output under stress. AF is the most common sustained arrhythmia and strongly associated with heart failure of all phenotypes. (source: 2021-ESC-Guidelines-Heart-Failure.pdf)

**Atrial fibrosis** is a key substrate for AF maintenance: chronic atrial pressure elevation (from [[diastolic-dysfunction]]) promotes LA remodelling and fibrosis, creating re-entrant circuits. AF and HFpEF are thus mutually reinforcing.

## Role in HFpEF

AF is substantially more prevalent in [[hfpef]] than in [[hfref]] or [[hfmref]], reflecting the older, more comorbid HFpEF population and the haemodynamic substrate of chronically elevated LA pressure. (source: 2021-ESC-Guidelines-Heart-Failure.pdf)

**Bidirectional relationship:**
- [[diastolic-dysfunction]] → elevated LA pressure → LA dilation and fibrosis → AF
- AF → loss of atrial kick → worsened LV filling in stiff ventricle → precipitates or worsens HFpEF symptoms
- AF → tachycardia-mediated cardiomyopathy → may lower LVEF, reclassifying phenotype

**Diagnostic impact:** AF requires adjusted thresholds for all HFpEF diagnostic markers:
- LA volume index threshold: >40 mL/m² (vs. >34 mL/m² in sinus rhythm)
- NT-proBNP threshold: >365 pg/mL (vs. >125 pg/mL in sinus rhythm)
- BNP threshold: >105 pg/mL (vs. >35 pg/mL in sinus rhythm)

(source: 2021-ESC-Guidelines-Heart-Failure.pdf)

## Evidence

AF is listed as a key predisposing condition for [[diastolic-dysfunction]] alongside hypertension, ageing, obesity, and diabetes. It is included in both the H₂FPEF score (as one of six weighted variables) and the HFA-PEFF algorithm as a factor elevating pre-test probability. (source: 2021-ESC-Guidelines-Heart-Failure.pdf)

AF prevalence: 15–30% in large HFpEF trials; up to 50% when paroxysmal AF is included. AF is associated with increased HF hospitalization risk and may itself precipitate HHF episodes in HFpEF. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

Strong bidirectional pathophysiology: HFpEF with AF and atrial functional mitral regurgitation (FMR) represents a particularly high-risk combined phenotype. Atrial FMR prevalence in HFpEF is up to 50%; coexistence with AF creates a distinct adverse phenotype with very high mortality. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

**AF-HFpEF epidemiology (Reddy 2024):**
- **83% occult HFpEF in symptomatic AF:** Patients with symptomatic AF and normal resting echo/NP who underwent exercise right heart catheterisation (RHC) were found to have HFpEF in 83% of cases — the majority of symptomatic AF patients harbour occult HFpEF
- **~82% occult AF in HFpEF:** HFpEF patients with sinus rhythm at index evaluation developed AF in ~82% over 1 year of monitoring — bidirectional relationship is nearly universal at the disease level
- **Exercise RHC as only reliable HFpEF diagnostic in AF:** Resting biomarkers (NP) and echocardiographic HFpEF scores perform poorly in AF because AF itself confounds NP levels and diastolic parameters. Exercise RHC (PCWP ≥25 mmHg or PCWP/CO slope >2) is the only reliable confirmation method in AF patients
- **Anticoagulation:** Anticoagulation for AF episodes >6 minutes: approximately 32% stroke risk reduction; clinical threshold for anticoagulation initiation — supports monitoring for sub-clinical AF in HFpEF patients
- **Bidirectional LA remodelling:** HFpEF → elevated LA pressure → atrial myopathy → AF substrate; AF → loss of atrial kick → worse LV filling in stiff LV → worsened HFpEF; LA myopathy is the mechanistic convergence
(source: reddy2024afhfpef)

## Status

Management of AF in HFpEF is recommended as part of comorbidity-centred treatment (Class I, C). (source: 2021-ESC-Guidelines-Heart-Failure.pdf)

**Rhythm control:** EAST-AFNET4 trial: early rhythm control (antiarrhythmic drugs or catheter ablation) reduced CV death/stroke/HF hospitalisation composite versus rate control in patients with AF (including subgroup with heart failure). Results support early rhythm control in AF-HFpEF, but EAST-AFNET4 was not dedicated to HFpEF — extrapolation requires caution. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

**CABA-HFpEF** (NCT05508256): Phase III RCT of catheter ablation vs. conventional rate control specifically in HFpEF patients with AF. Led by DZHK (German Centre for Cardiovascular Research — same network as [[torch]] registry). This is the first dedicated HFpEF-AF ablation trial; results will provide direct evidence for rhythm vs. rate control strategy in HFpEF. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

## Related Pages
- Concepts: [[diastolic-dysfunction]], [[hfpef-diagnosis]], [[natriuretic-peptides]], [[hfpef-treatment-gap]]
- Entities: [[hfpef]], [[hfmref]], [[hfref]], [[caba-hfpef]]
- Sources: [[mcdonagh2021esc]], [[anker2023hfpefphenotype]], [[reddy2024afhfpef]]

## Contradictions
- Higher NP and LA volume thresholds in AF reflect the independent NP-elevating effect of AF itself, not just worse HFpEF — this may lead to under-diagnosis of HFpEF in AF patients who are close to but below the higher threshold. (source: [[pieske2019hfapeff]]; [[mcdonagh2021esc]]) Exercise RHC is the only reliable HFpEF diagnostic in AF: resting NP and echocardiographic scores are systematically confounded, and 83% of symptomatic AF patients have occult HFpEF by invasive exercise testing. (source: [[reddy2024afhfpef]])

See [[contradictions]].
