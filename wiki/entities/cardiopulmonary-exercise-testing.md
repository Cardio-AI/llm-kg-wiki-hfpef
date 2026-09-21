---
title: Cardiopulmonary Exercise Testing (CPET)
summary: Integrated assessment of cardiorespiratory, metabolic, and gas exchange responses
  to graded exercise; in invasive form (with PA catheter and arterial line), it is
  the gold standard for diagnosing HFpEF in equivocal cases and for mechanistic dissection
  of exercise intolerance components.
entity_type: diagnostic-tool
tags:
- hfpef
- diagnosis
- cardiopulmonary-exercise-testing
- imaging
- physiology
- exercise
created: 2026-04-30
last_updated: 2026-09-21
sources:
- citekey: Ho2019HFpEFDefinitions
  doi: 10.1161/CIRCULATIONAHA.118.039136
- citekey: Sachdev2023Exercise
  doi: 10.1161/CIR.0000000000001122
- citekey: McDonagh2021ESC
  doi: 10.1093/eurheartj/ehab368
- citekey: borlaug2010exercise
  doi: 10.1161/CIRCHEARTFAILURE.109.930701
- citekey: landsteiner2025hemodynamics
  doi: 10.1161/CIRCRESAHA.125.326504
- citekey: Landsteiner2026Multiorgan
  doi: 10.1161/CIRCULATIONAHA.125.077579
page-type: entity-page
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

This allows decomposition of VO2 = CO × A-VO2 diff (Fick principle), quantifying cardiac vs. peripheral contributions to exercise intolerance. (source: Ho2019HFpEFDefinitions; source: Sachdev2023Exercise)

## Role in HFpEF

### As Diagnostic Gold Standard

In equivocal HFpEF cases, invasive CPET establishes physiologic HFpEF (HFpEF_phys). Thresholds differ by exercise position:

**Supine exercise (Borlaug 2010 protocol):**
- PCWP ≥15 mmHg at rest → elevated LV filling pressure at rest
- PCWP ≥25 mmHg during supine exercise → exertional HFpEF
- LVEDP ≥16 mmHg at rest (direct LV catheterization)
- Exercise PASP ≥45 mmHg (non-invasive Doppler surrogate): sensitivity 96%, specificity 95%, AUC 0.99 in patients with normal resting hemodynamics (source: borlaug2010exercise)
- Hemodynamic gap emerges within 1.5 minutes of exercise at 20W — very low workload threshold (source: borlaug2010exercise)

**Upright exercise (Landsteiner 2025 protocol):**
- PCWP/CO slope >2 mmHg/L/min during upright ergometry (minute-by-minute over ~10 minutes) — preferred metric for upright protocols; captures the slope of filling pressure rise relative to cardiac output augmentation
- HC-HFpEF (hemodynamically confirmed HFpEF): resting PCWP ≥15 mmHg OR exercise PCWP/CO slope >2 mmHg/L/min (source: landsteiner2025hemodynamics)
- **Upright vs. supine distinction:** Upright exercise produces lower absolute PCWP than supine at equivalent workload (gravitational venous pooling reduces preload); reclassification between protocols is known. The Landsteiner cohort used upright ergometry, yielding lower absolute PCWP values than the Borlaug 2010 supine protocol — thresholds are not interchangeable.

**Exercise-unmasked HFpEF:** 23–28% of HC-HFpEF patients have normal resting PCWP but elevated exercise PCWP/CO slope — entirely missed by resting-only assessment. This subgroup has independent adverse prognosis (HR 1.42, 95% CI 1.08–1.86 vs. normal rest + exercise hemodynamics). (source: landsteiner2025hemodynamics)

The ESC 2021 gold-standard criteria (rest PCWP ≥15, exercise PCWP ≥25) are anchored to supine protocols; Borlaug 2023 also endorsed the PCWP/CO slope >2 for upright protocols. (source: McDonagh2021ESC; source: borlaug2023statement)

In the Ho 2019 cohort (n=461), 53% of referred HFpEF-suspect patients met HFpEF_phys criteria by invasive CPET — demonstrating that no non-invasive criterion alone reliably identifies this group:

| Non-invasive marker | Sensitivity for HFpEF_phys | Specificity |
|---|---|---|
| Echo structural markers | 71% | 51% |
| NT-proBNP ≥125 pg/mL | 48% | 74% |
| E/e' >9 | 78% | 59% |
| E/e' >13 | 46% | 86% |

(source: Ho2019HFpEFDefinitions)

### As Mechanistic Tool

Invasive CPET quantifies relative contributions to [[exercise-intolerance]]:
- A-VO2 diff (skeletal muscle) accounts for >50% of VO2 reduction in HFpEF
- CO reserve (cardiac) accounts for the remainder
- Chronotropic incompetence present in ~50%

(source: Sachdev2023Exercise)

**Largest iCPET HFpEF cohort to date (Landsteiner 2026, N=820):** Defined 7 distinct organ-specific exercise physiological deficits (cardiac filling pressure, stroke volume, heart-rate augmentation, pulmonary vascular resistance, breathing reserve, metabolic cost of exercise initiation, peripheral O₂ extraction) using invasive CPET, most of which co-occur across ≥2 organ systems per patient. Prevalence: elevated exercise filling pressure 43%, blunted HR augmentation 48%, increased PVR 38%, decreased peripheral O₂ extraction 44%, increased metabolic cost of exercise 45%, decreased breathing reserve 25%, decreased stroke volume 16%. Total deficit count strongly predicts adverse outcomes (≥5 deficits: HR 3.90, 95% CI 1.74–8.75, for composite CV hospitalisation/mortality). Deficit-specific plasma metabolite signatures (via LASSO regression) validated in an independent community cohort (MESA, N=6,345, ~18.6y follow-up) predicted incident HF, adding up to ~20% continuous net reclassification improvement over traditional risk factors. (source: [[landsteiner2026multiorgan]])

### As Prognostic Tool

HFpEF_phys (elevated PCWP by invasive CPET) independently predicts CV events HR 1.62 (p=0.01) regardless of guideline classification. Peak VO2 is a continuous prognostic predictor. (source: Ho2019HFpEFDefinitions)

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

**Clinical use:** Limited to specialist centres; procedural risk (arterial/venous access, PA catheter) restricts routine use. ESC 2021 recommends invasive exercise testing for diagnostic uncertainty; use limited to research and specialist evaluation. (source: McDonagh2021ESC)

**Research role:** Standard in HFpEF mechanistic studies and therapeutic trials requiring objective exercise capacity measurement.

**Limitation:** PA catheter placement carries procedural risk; inter-centre variability in technique; PCWP measurement during exercise requires expertise and standardised methodology.

## Related Pages

- Concepts: [[exercise-intolerance]], [[hfpef-diagnostic-definitions]], [[hfpef-diagnosis]], [[diastolic-dysfunction]]
- Entities: [[hfpef]], [[echocardiography]], [[supervised-exercise-training]], [[six-minute-walk-test]]
- Sources: [[ho2019hfpefdefinitions]], [[sachdev2023exercise]], [[mcdonagh2021esc]], [[borlaug2010exercise]], [[landsteiner2025hemodynamics]], [[borlaug2023statement]], [[landsteiner2026multiorgan]]

## Contradictions

- Non-invasive markers have only moderate accuracy for HFpEF_phys (E/e' >9: sensitivity 78%, specificity 59%; NT-proBNP ≥125: sensitivity 48%) — invasive confirmation cannot be replaced by any single non-invasive criterion. See [[contradictions]].

## References
- Landsteiner I, Stolze LK, Peterson TE, et al. Multiorgan Physiological Deficits During Exercise Identify Clinical and Molecular Predisposition to Heart Failure With Preserved Ejection Fraction. *Circulation.* 2026;153(13):1362–1384. doi:[10.1161/CIRCULATIONAHA.125.077579](https://doi.org/10.1161/CIRCULATIONAHA.125.077579)
- Borlaug BA, Nishimura RA, Sorajja P, Lam CSP, Redfield MM. Exercise Hemodynamics Enhance Diagnosis of Early Heart Failure With Preserved Ejection Fraction. *Circ Heart Fail.* 2010;3(5):588–595. doi:[10.1161/CIRCHEARTFAILURE.109.930701](https://doi.org/10.1161/CIRCHEARTFAILURE.109.930701) [DOI unverified]
- Ho JE, Zern EK, Wooster L, et al. Differential Clinical Profiles, Exercise Responses, and Outcomes Associated With Existing HFpEF Definitions. *Circulation.* 2019;140(5):353–365. doi:[10.1161/CIRCULATIONAHA.118.039136](https://doi.org/10.1161/CIRCULATIONAHA.118.039136)
- Landsteiner I, Ikoma T, Ramesh A, Campain J, Cohen LP, Hardin CC, Malhotra R, Lewis GD. Implications of HFpEF Definitions Unveiled by Rest and Exercise Hemodynamics. *Circ Res.* 2025;137(4):357–359. doi:[10.1161/CIRCRESAHA.125.326504](https://doi.org/10.1161/CIRCRESAHA.125.326504) [DOI unverified]
- McDonagh TA, Metra M, Adamo M, et al.; ESC Scientific Document Group. 2021 ESC Guidelines for the diagnosis and treatment of acute and chronic heart failure. *Eur Heart J.* 2021;42(36):3599–3726. doi:[10.1093/eurheartj/ehab368](https://doi.org/10.1093/eurheartj/ehab368)
- Sachdev V, Sharma K, Keteyian SJ, et al. Supervised Exercise Training for Chronic Heart Failure With Preserved Ejection Fraction: A Scientific Statement from the American Heart Association. *Circulation.* 2023;147(10):e699–e715. doi:[10.1161/CIR.0000000000001122](https://doi.org/10.1161/CIR.0000000000001122)
