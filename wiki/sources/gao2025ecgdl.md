---
type: study
title: Deep Learning-Based Electrocardiogram for Screening Heart Failure With Preserved
  Ejection Fraction
citekey: Gao2025ECGDL
year: 2025
authors: Gao Z, Yang Y, Yang Z, Zhang X, Liu C
journal: ESC Heart Failure
study_type: observational
evidence_level: moderate
tags:
- hfpef
- ml-ai
- ecg
- diagnosis
- screening
created: 2026-05-12
last_updated: 2026-05-13
sources:
- file: raw/2025-ESC-Gao-ECG_DL_detection_HFpEF.pdf
  citekey: Gao2025ECGDL
page-type: source-summary-page
---
# CNN-LSTM ECG Model for HFpEF Screening (Gao 2025)

> A CNN-LSTM deep learning model applied to standard 12-lead ECGs achieves 78% accuracy in training (Cohort A) and 71.8% accuracy (71.7% sensitivity, 71.9% specificity) in prospective validation (Cohort B) for identifying HFpEF risk using invasive LVEDP >12 mmHg as reference standard, without relying on BNP or echocardiographic E/e'. Precordial leads perform better than limb leads.

**File:** `raw/2025-ESC-Gao-ECG_DL_detection_HFpEF.pdf` · **Authors:** Gao Z, Yang Y (Yuqing), Yang Z (Zhiqiang), Zhang X, Liu C (corresponding author)  
**Affiliations:** Department of Cardiology, First Hospital of Hebei Medical University, Shijiazhuang; Cangzhou Central Hospital and Cangzhou Medical College, China  
**Year:** 2025 (published online October 27, 2024) · **Journal:** ESC Heart Failure 2025;12:631–639 · **DOI:** 10.1002/ehf2.15120  
**Study type:** Observational model development (Cohort A) + prospective external validation (Cohort B)  
**N:** Cohort A (training) 238 (116 high-risk LVEDP >12 mmHg; 122 low-risk LVEDP ≤12 mmHg); Cohort B (prospective validation) 117 (58 high-risk; 59 low-risk)  
**Population:** LVEF >50%; patients undergoing invasive left ventricular catheterisation (left heart catheterisation using pigtail conduit); Cohort A Feb 2021–Aug 2023; Cohort B Aug 2023–Apr 2024; single centre (First Hospital of Hebei Medical University, Shijiazhuang, China)  
**Exclusions:** AF, sinus arrhythmia, myocardial ischaemia, post-pacemaker, prior MI, coronary atherosclerotic heart disease  
**Follow-up:** Cross-sectional (single LHC visit)  
**Intervention/Exposure:** 10-second 12-lead ECG → CNN-LSTM model (6 precordial leads only; 5,000 amplitudes per lead at 500 Hz; input matrix 5,000×12)  
**Primary outcome:** HFpEF risk classification (high vs. low risk); reference standard = invasive LVEDP threshold **12 mmHg** (not 15–16 mmHg as previously stated)

---

## Key Findings

- Cohort A (training, N=238): 78% accuracy (training set); DLM achieved 75% accuracy when applied to assign Cohort A patients (per results section)
- Cohort B (prospective validation, N=117): 71.8% overall accuracy; 71.7% sensitivity; 71.9% specificity; confusion matrix: TP=41, TN=43, FP=16, FN=17
- LVEDP threshold for HFpEF high-risk: **>12 mmHg** (explicitly stated); LVEF >50% required for all participants
- BNP did **not** differ between DLM-identified high- and low-risk groups in Cohort B: 22 (8.38–32.38) vs. 20 (11.5–31.5) pg/mL, P=0.71
- E/e' did **not** differ between groups: 8.25 (7.33–10.2) vs. 8.5 (7.65–9.9), P=0.66
- LVEDP (by definition, reference standard): high-risk 19 (10–20) mmHg vs. low-risk 11 (9.5–13) mmHg; P<0.01
- High-risk group features (Cohort B): more diabetes (22.03% vs. 11.86%, P<0.01); higher BMI (25.92 [24.44–27.85] vs. 24.22 [22.17–26.85] kg/m², P<0.01)
- Low-risk group features: more CCB use (28.81% vs. 11.76%, P=0.05)
- Hypertension: not significantly different (41.38% vs. 34.57%, P=0.62 in Cohort B — note: baseline Table 1 shows 24 [41.38%] vs 34 [57.63%])
- Precordial leads (V1–V6) perform better than limb leads for HFpEF risk assessment in this model
- Model architecture: CNN (256 filters) → CNN (128) → Reshape → LSTM (70 units) → Dense (64) → output; 163,690 total parameters; built in TensorFlow/Python 3.7

## Methods (brief)

**Architecture:** Hybrid CNN-LSTM. Input: 5,000 amplitudes × 12 leads (500 Hz, 10-second ECG) arranged as matrix; precordial leads V1–V6 selected (limb leads performed worse). Convolutional layers extract local morphology features; LSTM (70 units) captures temporal dependencies. Pipeline: CNN(256) → CNN(128) → Reshape → LSTM(70) → Dense(64) → output layer. 163,690 total parameters. Forward/backward propagation optimised via model.fit.

**Reference standard:** Invasive LVEDP measured via pigtail conduit during left ventricular catheterisation, with baroreceptor zeroed and pressure transducer at midaxillary level. LVEDP threshold: **>12 mmHg** = high risk (HFpEF); ≤12 mmHg = low risk. Note: ESC 2023 guideline uses LVEDP >15 mmHg for grey zone; this study used 12 mmHg (more sensitive/lower threshold).

**Cohort A** (N=238, Feb 2021–Aug 2023): Training set. Single centre (First Hospital of Hebei Medical University). 116 high-risk (LVEDP >12 mmHg), 122 low-risk. ECG and LVEDP data not publicly released for security reasons.  
**Cohort B** (N=117, Aug 2023–Apr 2024): Prospective validation. Same institution. 58 high-risk, 59 low-risk. ECG and LVEDP data available in Data S2–S3.

BNP (B-type natriuretic peptide), E/e' (echocardiographic), and UCG (ultrasound cardiogram) measures collected in all Cohort B patients and compared between DLM-identified high/low risk groups.

## Results

### Model Performance

| Cohort | N | Accuracy | Sensitivity | Specificity |
|--------|---|----------|-------------|-------------|
| Cohort A (training, per abstract) | 238 | 78% | — | — |
| Cohort A (DLM assignment result) | 238 | 75% | — | — |
| Cohort B (prospective validation) | 117 | 71.8% | 71.7% | 71.9% |

Confusion matrix (Cohort B): TP=41, TN=43, FP=16, FN=17. Note: AUC/AUROC not reported in this study.

### Baseline Characteristics (Cohort B, DLM-stratified)

| Variable | High-risk (n=58) | Low-risk (n=59) | P |
|----------|-----------------|----------------|---|
| Age (median, IQR) | 60 [49.25, 68] | 59 [48.5, 67] | 0.76 |
| Male (%) | 22 (47.83%) | 22 (47.37%) | 1 |
| BMI (kg/m², median [IQR]) | 25.92 [24.44, 27.85] | 24.22 [22.17, 26.85] | <0.01 |
| Diabetes (%) | 13 (22.03%) | 7 (11.86%) | <0.01 |
| Hypertension (%) | 24 (41.38%) | 34 (57.63%) | — |
| CCB use (%) | 6 (11.76%) | 17 (28.81%) | 0.05 |
| SGLT2i use (%) | 3 (5.08%) | 1 (1.69%) | 0.61 |
| LVEF (%) | 62.67 ± 4.30 | 62.76 ± 4.47 | 0.91 |
| LVEDP (mmHg, median [IQR]) | 19 [10, 20] | 11 [9.5, 13] | <0.01 |
| BNP (pg/mL, median [IQR]) | 22 [8.38, 32.38] | 20 [11.5, 31.5] | 0.71 |
| E/e' | 8.25 [7.33, 10.2] | 8.5 [7.65, 9.9] | 0.66 |

Both BNP and E/e' were in normal/near-normal range and did not differ between groups — consistent with the known insensitivity of resting BNP and E/e' in early/subclinical HFpEF where LVEDP elevation is the only hemodynamic signal.

## Limitations

- Both cohorts from northern China (single institution); generalisability to Western populations, different ethnicities, or different hospital settings unknown
- LVEDP threshold of 12 mmHg is lower than the ESC 2023 grey zone (12–15 mmHg) and diagnostic threshold (>15 mmHg); the study "high-risk" group includes patients in the ESC grey zone who may not have definitive HFpEF
- LVEDP alone does not constitute HFpEF diagnosis per ESC/ACC/AHA criteria (requires LVEF + symptoms + structural/functional evidence)
- N=238/117 — very small for a deep learning model; 163,690 parameters trained on 238 patients is highly susceptible to overfitting despite prospective validation
- No AUC/AUROC reported — only accuracy, sensitivity, specificity; AUROC would allow comparison to biomarker performance
- Cohort B is prospective from the same hospital (not an independent external centre); reduces generalisability claim
- AF, prior MI, and pacemaker patients excluded — these are common in HFpEF populations, limiting real-world applicability
- Clinical utility over simple ECG pattern recognition (LVH criteria, P-wave morphology, QRS axis, PR interval) not demonstrated by ablation studies
- Funding body (Hebei Province Health Commission) played a role in study design and data collection per authors' statement — potential influence on outcome reporting
- Patent application filed on DLM method (Chinese patent 2023110099031.9) — potential conflict of interest

## Connections

- Supports: [[hfpef-diagnosis]] — ECG-based deep learning can capture haemodynamic information beyond BNP or standard echocardiographic parameters
- Connects to: [[pandey2021deepnnecho]] — parallel ML approach (echo-based DeepNN vs. ECG-based CNN-LSTM); both target early HFpEF risk identification
- Supports: [[paulus2013novelparadigm]] — ECG model risk factors (DM, obesity/BMI) align with Paulus comorbidity-driven paradigm
- Suggests: ECG carries haemodynamic signal independent of conventional biomarkers in early LVDD — potentially useful for screening in resource-limited settings

## Secondary Analyses & Data Reuse

| Citekey | Focus | Wiki page |
|---------|-------|-----------|
| — | — | — |

## Related Pages

- Concepts: [[hfpef-diagnosis]], [[hfpef-phenotype-profiling]], [[diastolic-dysfunction]]
- Entities: [[hfpef]]
- Sources: [[pandey2021deepnnecho]], [[paulus2013novelparadigm]], [[shah2015phenomapping]]

## Contradictions

BNP and E/e' did not differ between high/low risk groups identified by the ECG model — consistent with known insensitivity of resting BNP and E/e' in early/subclinical HFpEF (see [[hfpef-diagnosis]]). This is not a contradiction per se but underscores the diagnostic gap the model addresses.
