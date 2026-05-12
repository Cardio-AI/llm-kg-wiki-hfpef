---
type: concept
title: Machine Learning and AI in HFpEF
summary: Application of artificial intelligence and machine learning to HFpEF diagnosis, phenotyping, prognosis, and treatment selection
tags:
  - ml-ai
  - mechanism
  - diagnosis
  - hfpef
created: 2026-05-05
last_updated: 2026-05-05
sources:
  - file: raw/2025-jjcc-Yi-AI_in_HFpEF.pdf
    citekey: Yi2025AI
---
# Machine Learning and AI in HFpEF

> AI/ML is particularly suited to HFpEF because heterogeneous pathophysiology, diverse clinical trajectories, and complex multimodal data exceed the pattern-recognition capacity of traditional statistical methods; 38 published studies across four domains — diagnosis, phenotyping, risk prediction, and management — demonstrate consistent proof-of-concept but limited prospective validation.

---

## Mechanism

HFpEF poses challenges that AI is designed to address:
- **Heterogeneity:** No single aetiology; multiple pathophysiological axes (inflammation, obesity/cardiometabolic, fibrosis, ageing, ischaemia) contribute to the same syndrome
- **Multimodal complexity:** Diagnosis requires integration of echo, ECG, biomarkers, symptoms, and clinical history — traditional scoring systems (H₂FPEF, HFA-PEFF) capture only cross-sectional snapshots
- **Underdiagnosis:** NLP-based studies identify ~75% of cases undiagnosed in routine clinical practice (Garan 2023, in [[yi2025ai]])
- **Treatment heterogeneity:** Population-level RCTs miss subgroup benefit; ML can identify who responds to which therapy

**Four AI application domains:**

| Domain | N studies (Yi 2025) | Maturity | Best signal |
|---|---|---|---|
| Diagnosis | 14 | Proof-of-concept | ECG-AI AUC 0.87; Echo 3D-CNN AUC 0.79 |
| Phenotyping | 11 | Consistent phenotype axes identified | 3–4 clusters with 2–4× HR difference |
| Risk prediction | 10 | Moderate — retrospective | Readmission AUC 0.90; C-stat 0.72–0.76 |
| Management | 3 | Early | Spironolactone responder ML |

## Clinical Relevance

### Diagnosis
- **ECG deep learning** (Unterhuber 2021, Kwon 2021): AUC ~0.87 from 12-lead ECG alone; NPV 0.98 — scalable screening rule-out in resource-limited settings; standard clinical ECG is non-diagnostic for HFpEF
- **3D-CNN echocardiography** (Akerman 2023): single apical 4-chamber clip sufficient; outperforms HFA-PEFF and H₂FPEF scores in non-diagnostic rate reduction; sensitivity 0.87
- **NLP on EHR** (Garan 2023): F1=0.91 for ESC HFpEF identification; found 75.4% of meeting-criteria patients undiagnosed — largest underdiagnosis estimate in HFpEF literature; implications for trial recruitment and population burden estimates

### Phenotyping
Consistent phenotypic axes across 11 studies (source: [[yi2025ai]]):
- **Cardiometabolic cluster** (obesity, DM, CKD, high BNP): most common; responds better to beta-blockers/ARBs in some analyses (Gu 2021); highest comorbidity burden
- **Inflammatory/fibrotic cluster** (elevated inflammatory markers, fibrosis biomarkers): identified in obese HFpEF subset (Sabbah 2020)
- **Age/AF-dominant cluster**: lower filling pressure; atrial myopathy as mechanism
- **Ischaemic cluster**: prior MI, CAD; distinct from pure pressure overload HFpEF

Shah 2015 highest-risk phenotype: HR 4.2 (95% CI 2.0–9.1) for HF hospitalization — clinically actionable risk stratification.

### Risk prediction
Consistent top ML predictors across studies: NT-proBNP/BNP, eGFR, EF, E/e', age, BMI, AF history, loop diuretic use, NYHA class. These overlap substantially with MAGGIC risk score variables ([[pocock2013maggic]]), validating the conventional prognostic model while adding non-linear interactions.

Specific ML-derived insights:
- LAD (left atrial dimension) is a top XGBoost feature for 90-day readmission (Zheng 2024)
- Monocytes-to-lymphocytes ratio predicts 1-year readmission (Hu 2025) — inflammatory signature detectable from CBC
- Fall risk and nutritional status captured in ML but absent from traditional scores

### Treatment response (management)
**Spironolactone responder analyses** (most clinically actionable ML finding in HFpEF):
- Kresoja 2023 (TOPCAT N=3,445 + Aldo-DHF N=422): ML identifies responders; spironolactone reduces CV events in responders (log-rank P=0.008) vs non-responders (P=0.52) — treatment effect is real but population-level diluted
- Desai 2024 (TOPCAT N=3,445): individualized treatment effect prediction; **BMI top contributor (33.7%)**; eGFR 27.3%, EF 15.1%, age 12.8% — high-BMI patients are the spironolactone responders

**Implication:** TOPCAT's overall null result (Pitt 2014 P=0.14) may be an enrichment failure, not a class failure. SGLT2i class likely has similar enrichment considerations; AI tools to identify SGLT2i high-responders not yet published.

**Empagliflozin mechanism (in silico):** Bayes-Genis 2021 — primary mechanism is NHE1 (Na⁺/H⁺ exchanger 1) inhibition → reduced cardiomyocyte oxidative stress. Not clinically actionable yet but provides first computational pharmacological target model for HFpEF.

## History

- **2015** — Shah et al. first applied hierarchical clustering to HFpEF (N=397); 3 phenotypes with HR 4.2 for hospitalization in highest-risk cluster; established feasibility of ML phenotyping (source: [[yi2025ai]])
- **2019** — Przewlocka-Kosmala: exercise echocardiography + galectin-3 clustering; cardiovascular reserve as phenotyping dimension
- **2020–2021** — Multiple independent phenotyping studies (TOPCAT subsets, SwedeHF registry, HFN trial cohorts) converge on 3–4 phenotype axes; Sabbah identifies obese-inflammatory subtype
- **2021** — First ECG deep learning studies (Unterhuber, Kwon) validate ECG-AI for HFpEF detection; AUC ~0.87; establishes ECG as scalable screening modality
- **2022–2024** — Shift from phenotyping to prediction and treatment-response; XGBoost readmission models (AUC ~0.90); AIM-HFpEF EHR-based diagnosis; spironolactone responder ML (Kresoja, Desai); first multimodal models
- **2025** — Yi review synthesises 38 studies; field identified as moving from retrospective proof-of-concept toward prospective implementation; major gaps: external validation, regulatory pathway (TRIPOD-AI), algorithmic equity [expand as sources added]

## Evidence

Current evidence is largely **retrospective observational** — 35/38 studies in Yi 2025 review. Three RCT-based analyses (Kresoja 2023, Desai 2024, Angraal 2020) applied ML to existing TOPCAT data post-hoc. No prospective trial has used AI-derived phenotype or risk score for patient selection or treatment assignment in HFpEF.

Evidence quality for individual claims:
- ECG-AI diagnostic performance: moderate (internal validation consistent; external validation N=2); AUC 0.80–0.87
- Phenotyping consistency: moderate (independent replication in ≥3 datasets); clinical outcomes validation patchy
- Spironolactone responder prediction: moderate (two independent analyses of same TOPCAT dataset; mechanistically plausible)
- AI management guidance in prospective settings: **low** — no evidence yet

## Open Questions

- Can AI-identified phenotypes be used prospectively to enrich clinical trials (similar to PARAGON's LVEF <57% and female sex subgroup signal)?
- Does spironolactone benefit in ML-identified high-BMI/obese HFpEF phenotype hold in a prospective enrichment RCT?
- Can ECG-AI (AUC ~0.87) be integrated into primary care EHR workflows as a HFpEF screening trigger?
- How does ML phenotyping interact with the HFA-PEFF and H₂FPEF diagnostic algorithms? Are AI phenotypes captured or missed by conventional scoring?
- Algorithmic equity: most studies lack adequate representation of women, non-White, and non-English populations; generalisability uncertain
- Regulatory pathway: TRIPOD-AI, FDA AI/ML-based SaMD action plan — when will AI diagnostic tools for HFpEF receive approval?

## Related Pages
- Concepts: [[hfpef-diagnosis]], [[hfpef-treatment-gap]], [[exercise-intolerance]]
- Entities: [[hfpef]], [[spironolactone]], [[sglt2-inhibitors]]
- Sources: [[yi2025ai]], [[pitt2014topcat]], [[pocock2013maggic]]

## Contradictions
- ML spironolactone responders (Kresoja 2023; Desai 2024) conflict with TOPCAT overall null (HR 0.89 P=0.14 in Pitt 2014). ML post-hoc analysis of the same trial data showing significant benefit in a subgroup is subject to overfitting — neither Kresoja nor Desai has been prospectively validated. However, consistency between two independent analyses using different algorithms (ML-based analysis vs. individualized treatment effect) strengthens the signal. See [[contradictions]].
