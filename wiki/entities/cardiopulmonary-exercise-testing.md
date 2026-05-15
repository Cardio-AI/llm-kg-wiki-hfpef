---
type: entity
title: Cardiopulmonary Exercise Testing (CPET)
summary: Integrated assessment of cardiorespiratory, metabolic, and gas exchange responses to graded exercise; in invasive form (with PA catheter and arterial line), it is the gold standard for diagnosing HFpEF in equivocal cases and for mechanistic dissection of exercise intolerance components.
entity_type: diagnostic-tool
tags:
  - hfpef
  - diagnosis
  - cpet
  - imaging
  - physiology
  - exercise
created: 2026-04-30
last_updated: 2026-05-14
sources:
  - file: raw/2019-CirculationAHA-Ho-exercise-response.pdf
    citekey: Ho2019HFpEFDefinitions
  - file: raw/2023-CirculationAHA-Sachdev-hfpef-exercise.pdf
    citekey: Sachdev2023Exercise
  - file: raw/2021-ESC-Guidelines-Heart-Failure.pdf
    citekey: McDonagh2021ESC
  - file: raw/2010-CircHeartFail-Borlaug-Exercise_Hemodynamics.pdf
    citekey: borlaug2010exercise
  - file: raw/2025-CirculationAHA-Landsteiner-Exercise_hemodynamics.pdf
    citekey: landsteiner2025hemodynamics
---
# Cardiopulmonary Exercise Testing (CPET)

> Measurement of expired gas (VO2, VCO2, VE) and cardiovascular responses during graded exercise; invasive CPET adds direct haemodynamic measurement (PCWP, CO) and is the gold standard for HFpEF diagnosis in equivocal cases and for dissecting exercise intolerance mechanisms.

---

## Aliases
| Alias | Type | Notes |
|---|---|---|
| CPET | abbreviation | cardiopulmonary exercise testing — universal shorthand |
| CPEX | abbreviation | British English variant |
| peak VO₂ test | descriptive | refers to the primary output measure |
| invasive CPET | abbreviation | CPET with simultaneous right heart catheterisation (PA pressure + PCWP) |
| exercise stress test | descriptive | lay term; usually refers to non-metabolic ECG stress testing only |

---

## Description

CPET simultaneously measures:
- **VO2** (oxygen consumption) — overall aerobic capacity; peak VO2 as primary metric
- **VCO2** (CO2 production) and **VE/VCO2 slope** — ventilatory efficiency; elevated in pulmonary hypertension and HF
- **Anaerobic threshold (AT)** — submaximal fitness marker; respiratory exchange ratio (RER) ≥1.1 confirms maximal effort
- **Heart rate response** — chronotropic reserve; chronotropic incompetence if attenuated

**Standard (non-invasive) CPET:** Gas exchange + ECG monitoring + pulse oximetry + blood pressure. Identifies exercise limitation phenotype but cannot distinguish cardiac vs. peripheral causes.

**Invasive CPET:** Standard CPET + intra-arterial blood pressure + pulmonary artery catheter measuring:
- PCWP (pulmonary capillary wedge pressure) — surrogate for LV filling pressure
- Cardiac output (CO) by thermodilution or Fick
- Arteriovenous O2 difference (A-VO2 diff) — peripheral O2 extraction (skeletal muscle capacity)

This allows decomposition of VO2 = CO × A-VO2 diff (Fick principle), quantifying cardiac vs. peripheral contributions to exercise intolerance. (source: 2019-CirculationAHA-Ho-exercise-response.pdf; source: 2023-CirculationAHA-Sachdev-hfpef-exercise.pdf)

## Role in HFpEF

### As Diagnostic Gold Standard

In equivocal HFpEF cases, invasive CPET establishes physiologic HFpEF (HFpEF_phys). Thresholds differ by exercise position:

**Supine exercise (Borlaug 2010 protocol):**
- PCWP ≥15 mmHg at rest → elevated LV filling pressure at rest
- PCWP ≥25 mmHg during supine exercise → exertional HFpEF
- LVEDP ≥16 mmHg at rest (direct LV catheterization)
- Exercise PASP ≥45 mmHg (non-invasive Doppler surrogate): sensitivity 96%, specificity 95%, AUC 0.99 in patients with normal resting hemodynamics (source: 2010-CircHeartFail-Borlaug-Exercise_Hemodynamics.pdf)
- Hemodynamic gap emerges within 1.5 minutes of exercise at 20W — very low workload threshold (source: 2010-CircHeartFail-Borlaug-Exercise_Hemodynamics.pdf)

**Upright exercise (Landsteiner 2025 protocol):**
- PCWP/CO slope >2 mmHg/L/min during upright ergometry (minute-by-minute over ~10 minutes) — preferred metric for upright protocols; captures the slope of filling pressure rise relative to cardiac output augmentation
- HC-HFpEF (hemodynamically confirmed HFpEF): resting PCWP ≥15 mmHg OR exercise PCWP/CO slope >2 mmHg/L/min (source: 2025-CirculationAHA-Landsteiner-Exercise_hemodynamics.pdf)
- **Upright vs. supine distinction:** Upright exercise produces lower absolute PCWP than supine at equivalent workload (gravitational venous pooling reduces preload); reclassification between protocols is known. The Landsteiner cohort used upright ergometry, yielding lower absolute PCWP values than the Borlaug 2010 supine protocol — thresholds are not interchangeable.

**Exercise-unmasked HFpEF:** 23–28% of HC-HFpEF patients have normal resting PCWP but elevated exercise PCWP/CO slope — entirely missed by resting-only assessment. This subgroup has independent adverse prognosis (HR 1.42, 95% CI 1.08–1.86 vs. normal rest + exercise hemodynamics). (source: 2025-CirculationAHA-Landsteiner-Exercise_hemodynamics.pdf)

The ESC 2021 gold-standard criteria (rest PCWP ≥15, exercise PCWP ≥25) are anchored to supine protocols; Borlaug 2023 also endorsed the PCWP/CO slope >2 for upright protocols. (source: 2021-ESC-Guidelines-Heart-Failure.pdf; source: 2023-JACC-Borlaug-HFpEF_scientific_statement.pdf)

In the Ho 2019 cohort (n=461), 53% of referred HFpEF-suspect patients met HFpEF_phys criteria by invasive CPET — demonstrating that no non-invasive criterion alone reliably identifies this group:

| Non-invasive marker | Sensitivity for HFpEF_phys | Specificity |
|---|---|---|
| Echo structural markers | 71% | 51% |
| NT-proBNP ≥125 pg/mL | 48% | 74% |
| E/e' >9 | 78% | 59% |
| E/e' >13 | 46% | 86% |

(source: 2019-CirculationAHA-Ho-exercise-response.pdf)

### As Mechanistic Tool

Invasive CPET quantifies relative contributions to [[exercise-intolerance]]:
- A-VO2 diff (skeletal muscle) accounts for >50% of VO2 reduction in HFpEF
- CO reserve (cardiac) accounts for the remainder
- Chronotropic incompetence present in ~50%

(source: 2023-CirculationAHA-Sachdev-hfpef-exercise.pdf)

### As Prognostic Tool

HFpEF_phys (elevated PCWP by invasive CPET) independently predicts CV events HR 1.62 (p=0.01) regardless of guideline classification. Peak VO2 is a continuous prognostic predictor. (source: 2019-CirculationAHA-Ho-exercise-response.pdf)

## Evidence

| Application | Key Finding | Source |
|---|---|---|
| HFpEF_phys prevalence (resting or exertional) | 53% of referred HFpEF-suspect patients (n=461) | Ho2019HFpEFDefinitions |
| Exercise-unmasked HFpEF | 23–28% of HC-HFpEF missed by resting hemodynamics | landsteiner2025hemodynamics |
| Diagnostic threshold (supine) | PCWP ≥15 (rest) or ≥25 (exercise) mmHg | McDonagh2021ESC |
| Diagnostic threshold (upright) | PCWP/CO slope >2 mmHg/L/min | borlaug2023statement; landsteiner2025hemodynamics |
| Exercise PASP screen (non-invasive) | PASP ≥45 mmHg: sensitivity 96%, specificity 95%, AUC 0.99 | borlaug2010exercise |
| Hemodynamic gap onset | Within 1.5 min at 20W (supine) | borlaug2010exercise |
| Skeletal muscle contribution | A-VO2 diff >50% of VO2 deficit | Sachdev2023Exercise |
| Chronotropic incompetence | ~50% of HFpEF patients | Sachdev2023Exercise |
| Prognostic HR (resting PCWP) | HR 1.62 for CV events (p=0.01) | Ho2019HFpEFDefinitions |
| Prognostic HR (exercise PCWP/CO slope alone) | HR 1.42 (95% CI 1.08–1.86, P=0.012) vs. normal rest + exercise | landsteiner2025hemodynamics |
| Prognostic HR (high rest + high exercise) | HR 2.07 (95% CI 1.58–2.71, P<0.0001) | landsteiner2025hemodynamics |

## Status

**Clinical use:** Limited to specialist centres; procedural risk (arterial/venous access, PA catheter) restricts routine use. ESC 2021 recommends invasive exercise testing for diagnostic uncertainty; use limited to research and specialist evaluation. (source: 2021-ESC-Guidelines-Heart-Failure.pdf)

**Research role:** Standard in HFpEF mechanistic studies and therapeutic trials requiring objective exercise capacity measurement.

**Limitation:** PA catheter placement carries procedural risk; inter-centre variability in technique; PCWP measurement during exercise requires expertise and standardised methodology.

## Related Pages

- Concepts: [[exercise-intolerance]], [[hfpef-diagnostic-definitions]], [[hfpef-diagnosis]], [[diastolic-dysfunction]]
- Entities: [[hfpef]], [[echocardiography]], [[supervised-exercise-training]]
- Sources: [[ho2019hfpefdefinitions]], [[sachdev2023exercise]], [[mcdonagh2021esc]], [[borlaug2010exercise]], [[landsteiner2025hemodynamics]], [[borlaug2023statement]]

## Contradictions

- Non-invasive markers have only moderate accuracy for HFpEF_phys (E/e' >9: sensitivity 78%, specificity 59%; NT-proBNP ≥125: sensitivity 48%) — invasive confirmation cannot be replaced by any single non-invasive criterion. See [[contradictions]].
