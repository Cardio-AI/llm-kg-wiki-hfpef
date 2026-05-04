---
type: study
title: "TOPCAT Design Paper: Rationale, Design, and Baseline Characteristics"
citekey: Desai2011TOPCAT
year: 2011
authors: Desai AS, Lewis EF, Li R, et al. (TOPCAT Investigators)
journal: American Heart Journal
study_type: observational
evidence_level: moderate
tags:
  - trial
  - hfpef
  - spironolactone
  - mra
  - design
created: 2026-05-04
last_updated: 2026-05-04
sources:
  - file: raw/2011-AHA-Desai-TOPCAT_study.pdf
    citekey: Desai2011TOPCAT
---
# TOPCAT Design Paper (Desai 2011)

> Design and baseline characteristics paper for TOPCAT — a multi-national RCT of spironolactone vs. placebo in HFpEF with a dual-pathway enrollment strategy (hospitalization-based OR natriuretic peptide-based) that later proved critical to understanding the trial's contested results.

**File:** `raw/2011-AHA-Desai-TOPCAT_study.pdf` · **Authors:** Desai AS et al. · **Year:** 2011 · **Journal:** American Heart Journal  
**Study type:** Design/methods paper · **N:** 3,445 (planned) · **Population:** HF with LVEF ≥45%, age ≥50  
**Follow-up:** Minimum 2 years (mean ~3.3 years) · **Intervention:** Spironolactone vs. placebo (titrated 15→30→45 mg/day)  
**Primary outcome:** Composite of CV death + resuscitated cardiac arrest + HF hospitalization

---

## Key Findings

This is the design paper — no efficacy results reported here. See [[pitt2014topcat]] for primary outcomes. Key methodological features documented:

1. **Dual enrollment pathway** — two entirely different qualification criteria within the same trial
2. **266 sites across 6 countries** — introduced geographic heterogeneity that later explained the Americas vs. non-Americas result divergence
3. **Spironolactone titration schema** — gradual dose escalation with pre-specified stopping rules for hyperkalaemia and renal insufficiency
4. **Comprehensive parameter collection** — imaging, biomarkers, QoL, functional capacity

---

## Methods (brief)

### Disease Definition for Enrollment

**LVEF ≥45%** on echocardiography within 6 months of screening, confirmed by local site reading.

NYHA class II–IV, age ≥50 years (or any age if hospitalised for HF in the 12 months preceding randomisation).

**Exclusion criteria:**
- Any documented LVEF <45% within the preceding 6 months
- eGFR <30 mL/min/1.73m²
- Serum potassium >5.0 mEq/L
- Systolic BP <100 mmHg
- Planned CABG, PCI, or valve surgery
- Severe primary valvular disease (not secondary to LV dysfunction)
- Current MRA use
- Contra-indication to aldosterone antagonist

### Dual Qualification Pathway

Patients qualified via **one of two routes** — this distinction later became critical:

| Pathway | Criterion |
|---|---|
| **Hospitalization-based** | ≥1 HF hospitalization in the 12 months before screening |
| **NP-based (no hospitalization)** | BNP ≥100 pg/mL OR NT-proBNP ≥360 pg/mL within the prior 60 days |

Both pathways required LVEF ≥45% and signs/symptoms of HF. The NP pathway was intended to capture outpatient HFpEF without a recent hospitalisation. (source: 2011-AHA-Desai-TOPCAT_study.pdf)

### Sites and Countries

- **266 centers** across **6 countries**: United States, Canada, Brazil, Argentina, Russia, Georgia
- Site breakdown: Americas (US, Canada, Brazil, Argentina) vs. Eastern Europe (Russia, Georgia)
- Centers included academic medical centres and community hospitals; local echo reading used for LVEF qualification

### Intervention

Spironolactone titration schema (Figure 1):
- Run-in: Spironolactone 15 mg/day for 2 weeks (safety check)
- Week 4: Uptitrate to 30 mg/day
- Week 8+: Uptitrate to 45 mg/day target dose
- Down-titration mandated if K+ >5.5 mEq/L or Cr rises >50% from baseline
- Permanent discontinuation if K+ >6.0 mEq/L or eGFR <30

### Parameters Collected

**Imaging:**
- Transthoracic echocardiography (TTE): LVEF, LV volumes, LV mass, LA volume, E/e' ratio, E wave, A wave, deceleration time, septal and lateral e' velocities (tissue Doppler)
- No mandatory CMR

**Biomarkers / Laboratory:**
- BNP and NT-proBNP (qualifying and serial)
- Serum aldosterone, renin, creatinine, potassium (serial monitoring)
- Complete metabolic panel
- Urinary spironolactone metabolites (collected post-hoc to assess adherence/compliance — later used to detect non-Americas contamination)

**Functional / Clinical:**
- NYHA class (serial)
- 6-minute walk distance (6MWD)
- Kansas City Cardiomyopathy Questionnaire (KCCQ) — QoL
- ECG (12-lead)
- Blood pressure, weight, HR

**Endpoints:**
- Primary: CV death + resuscitated cardiac arrest + HF hospitalisation
- Secondary: All-cause mortality; HF hospitalization alone; change in KCCQ; change in 6MWD; renal events; AF incidence

---

## Results

Design paper — see [[pitt2014topcat]] for outcomes. This paper reports baseline characteristics showing:
- Mean age ~68 years
- ~52% female
- Mean LVEF ~56–57%
- ~90% NYHA II–III
- ~95% on diuretics at baseline
- Higher NP levels and more prior hospitalisations in hospitalization-pathway cohort vs. NP-only pathway

---

## Limitations

- Dual enrollment pathway introduced population heterogeneity; hospitalization-pathway patients likely sicker and more definitely HFpEF than NP-pathway
- Local echo reading for LVEF — no central reader for qualification
- Non-Americas sites (Russia, Georgia) showed markedly lower urinary metabolite levels in controls, suggesting placebo patients were receiving open-label spironolactone outside the trial — a fundamental trial integrity issue
- LVEF ≥45% threshold is permissive; includes patients who might now qualify as HFmrEF (LVEF 41–49%)

---

## Connections
- Describes: [[topcat]] — full trial design and site infrastructure
- Describes: [[pitt2014topcat]] — methods foundation for the results paper
- Supports: [[hfpef-diagnosis]] — documents what LVEF ≥45% with dual NP/hospitalisation criteria captures
- Relates to: [[spironolactone]] — MRA pharmacology and dose-titration protocol
- Registry: NCT00094302 (ClinicalTrials.gov)

## Secondary Analyses & Data Reuse

| Citekey | Focus | Wiki page |
|---------|-------|-----------|
| Pitt2014TOPCAT | Primary outcomes (CV death + HF hospitalization) | [[pitt2014topcat]] |
| [Americas subgroup] | Post-hoc Americas vs. Eastern Europe | — |
| [Metabolite analysis] | Urinary spironolactone metabolites; non-Americas integrity | — |

## Related Pages
- Concepts: [[hfpef-treatment-gap]], [[hfpef-diagnosis]], [[hf-phenotype-classification]]
- Entities: [[hfpef]], [[spironolactone]], [[topcat]]
- Sources: [[pitt2014topcat]], [[mcdonagh2021esc]], [[heidenreich2022aha]]

## Contradictions
- The dual-pathway design means TOPCAT enrolled at least two partially distinct populations. Americas vs. non-Americas result divergence may reflect both population differences and trial integrity problems simultaneously — the proportional contribution of each is unresolved. See [[contradictions]].
