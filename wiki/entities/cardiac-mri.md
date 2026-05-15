---
type: entity
title: Cardiac MRI (CMR)
summary: Cardiovascular magnetic resonance imaging; the gold standard for LVEF measurement and myocardial tissue characterisation; higher accuracy than echocardiography for LVEF but limited availability and contraindications in pacemaker/ICD patients; LA reservoir strain, LV GLS, native T1, ECV, LACI, and exercise CMR are emerging HFpEF-specific markers.
entity_type: imaging-tool
tags:
  - cardiac-mri
  - cmr
  - imaging
  - diagnosis
  - hfpef
created: 2026-04-30
last_updated: 2026-05-15
sources:
  - file: raw/2021-ESC-Guidelines-Heart-Failure.pdf
    citekey: McDonagh2021ESC
  - file: raw/2024-ESC-Ipek-CMR_characterization_HFpEF.pdf
    citekey: ipek2024cmr
  - file: raw/2024-IJCI-Lange-CMR_phenotyping_HF.pdf
    citekey: lange2024cmr
---
# Cardiac MRI

> Cardiovascular magnetic resonance imaging (CMR); the reference standard for LVEF measurement and myocardial tissue characterisation; recommended when echocardiography is suboptimal or when specific tissue diagnosis (amyloid, fibrosis) is needed.

---

## Aliases
| Alias | Type | Notes |
|---|---|---|
| CMR | abbreviation | cardiovascular magnetic resonance — preferred scientific abbreviation |
| cardiac MRI | alternate-name | clinical synonym; same modality |
| MRI heart | descriptive | lay/radiological term |
| LGE | abbreviation | late gadolinium enhancement — CMR tissue characterisation technique |
| T1 mapping | abbreviation | CMR quantification of extracellular volume / fibrosis |

---

## Description

Cardiac MRI (CMR) uses magnetic fields and radiofrequency pulses to generate high-resolution cardiac images without ionising radiation. Key capabilities relevant to HF:
- **LVEF and volumes:** Gold standard reference; lower inter-observer variability than [[echocardiography]]
- **Myocardial tissue characterisation:** Late gadolinium enhancement (LGE) for fibrosis/scar; T1 mapping for diffuse fibrosis (extracellular volume, ECV); T2 mapping for oedema
- **Infiltrative disease:** Native T1 elevation + LGE pattern diagnostic for cardiac amyloidosis
- **Pericardial assessment:** Constrictive pericarditis characterisation
- **Valvular quantification:** Flow quantification for regurgitation volumes

## Role in HFpEF

CMR is primarily used in HFpEF as a **second-line or problem-solving modality**:

1. **When [[echocardiography]] windows are inadequate** (obesity, COPD): CMR provides accurate LVEF and structural assessment
2. **Phenotype clarification:** Tissue characterisation to distinguish HFpEF from cardiac amyloidosis (T1 mapping, ECV, LGE pattern) or HCM
3. **LVEF reclassification:** When echocardiography gives a borderline LVEF (e.g., 48–52%), CMR provides a more accurate measurement, potentially reclassifying phenotype
4. **Research applications:** Diffuse myocardial fibrosis quantification (ECV) as a biomarker of diastolic dysfunction severity

**Benefits in HFpEF:**
- Highest accuracy for LVEF measurement — reduces phenotype misclassification
- Tissue characterisation enables specific aetiological diagnosis
- No acoustic window limitations

**Drawbacks in HFpEF:**
- Limited availability and higher cost than echocardiography
- Contraindicated in patients with non-MR-conditional implantable devices (pacemakers, ICDs) — relevant in elderly HFpEF population
- Cannot assess diastolic function in real-time or during exercise (no stress CMR equivalent for filling pressures)
- Gadolinium contraindicated in severe CKD (eGFR <30)

(source: 2021-ESC-Guidelines-Heart-Failure.pdf)

## Evidence

CMR is recommended by ESC 2021 when [[echocardiography]] is suboptimal and for aetiological characterisation, particularly for suspected cardiac amyloidosis or HCM in the differential diagnosis of [[hfpef]] with very high LVEF (>65–70%). (source: 2021-ESC-Guidelines-Heart-Failure.pdf)

**HFpEF-specific CMR markers (Ipek 2024 comprehensive review):**
- **Feature-tracking CMR (FT-CMR) strain:** LA reservoir strain and LV GLS detect functional impairment before LVEF decline; more sensitive than LVEF for HFpEF
- **ECV and native T1 mapping:** Extracellular volume fraction (ECV) correlates with histological fibrosis density (from [[fayyaz2025pathophys]]); native T1 elevation (1012 vs. 988 ms in HFpEF vs. controls; P=0.003) — quantitative fibrosis biomarker
- **LACI (LA-LV Coupling Index):** Ratio of LA volume to LV volume at minimum size; elevated in HFpEF; independently predicts HFpEF severity and correlates with exercise intolerance
- **Spectroscopy:** 31P-MRS measures myocardial PCr/ATP ratio (reduced in HFpEF, consistent with metabolic derangements in [[fayyaz2025pathophys]]); 1H-MRS measures myocardial triglycerides (elevated in obesity-associated HFpEF)
- **Perfusion CMR:** Coronary flow reserve (CFR) assessment by CMR identifies CMD (coronary microvascular dysfunction) subtype — connects to [[coronary-microvascular-dysfunction]] concept
- **Exercise CMR:** Real-time LVEF and SV augmentation during supine cycling — identifies exercise-induced LV dysfunction and blunted SV reserve; technically demanding but mechanistically informative
(source: ipek2024cmr)

**Cross-sectional CMR findings in HFpEF (Lange 2024, n=54 HF + 19 controls):**

| CMR Parameter | HFpEF (n=22) | Controls (n=19) | P-value |
|---|---|---|---|
| LA reservoir strain (%) | 28.9 ± 10.4 | 35.9 ± 6.0 | 0.008 |
| LV GLS (%) | −15.0 ± 3.0 | −19.2 ± 2.0 | 0.001 |
| Native T1 (ms) | 1012 ± 38 | 988 ± 21 | 0.003 |
| LA EDV (mL) | 48.1 ± 9.4 | 38.1 ± 4.8 | <0.01 |
| LACI | Elevated | — | 0.004 |
| NT-proBNP × LA Ee ratio | r = −0.41 | — | 0.008 |

(source: lange2024cmr)

## Status

**ESC 2021:** Recommended when echocardiography is suboptimal or when specific tissue diagnosis is required. Not recommended as routine first-line imaging in HFpEF. (source: 2021-ESC-Guidelines-Heart-Failure.pdf)

**Research role (Ipek 2024):** CMR has the greatest HFpEF phenotyping potential of any imaging modality — multiparametric assessment of function (FT-CMR), tissue composition (T1/T2/LGE/ECV), metabolism (spectroscopy), and hemodynamics (perfusion, exercise). Adoption limited by scanner access, cost, and pacemaker/ICD contraindications in the elderly HFpEF population.

## Related Pages
- Concepts: [[diastolic-dysfunction]], [[hfpef-diagnosis]], [[hf-phenotype-classification]], [[coronary-microvascular-dysfunction]]
- Entities: [[hfpef]], [[hfref]], [[hfmref]], [[echocardiography]]
- Sources: [[mcdonagh2021esc]], [[ipek2024cmr]], [[lange2024cmr]], [[fayyaz2025pathophys]]

## Contradictions
- CMR is the reference standard for LVEF, but echocardiography remains the clinical standard due to availability — this creates systematic LVEF measurement differences between research and clinical settings. [needs source]

See [[contradictions]].
