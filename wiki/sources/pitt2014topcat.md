---
type: study
title: "TOPCAT: Spironolactone in HFpEF"
citekey: Pitt2014TOPCAT
year: 2014
authors: Pitt B, Pfeffer MA, Assmann SF, et al. (TOPCAT Investigators)
journal: New England Journal of Medicine
study_type: RCT
evidence_level: moderate
tags:
  - trial
  - hfpef
  - spironolactone
  - mra
created: 2026-04-30
last_updated: 2026-05-04
sources:
  - file: raw/[not yet ingested — outcomes paper]
    citekey: Pitt2014TOPCAT
  - file: raw/2011-AHA-Desai-TOPCAT_study.pdf
    citekey: Desai2011TOPCAT
---
# TOPCAT

> Spironolactone was neutral vs. placebo on the primary composite endpoint in HFpEF overall, but the Americas subgroup showed significant benefit; suspected enrollment contamination in Eastern Europe (Russia/Georgia) has made the overall result permanently contested.

**File:** `raw/[outcomes paper not yet ingested]` · Design paper: `raw/2011-AHA-Desai-TOPCAT_study.pdf` · **Authors:** Pitt B et al. · **Year:** 2014 · **Journal:** NEJM  
**Study type:** RCT · **N:** 3,445 · **Sites:** 266 centers in 6 countries (US, Canada, Brazil, Argentina, Russia, Georgia)  
**Population:** HF with LVEF ≥45%, NYHA II–IV, age ≥50; dual enrollment: ≥1 HF hospitalisation in past year OR BNP ≥100/NT-proBNP ≥360 pg/mL  
**Follow-up:** Mean ~3.3 years (minimum 2 years) · **Intervention:** Spironolactone 15→30→45 mg/day vs. placebo  
**Primary outcome:** CV death + resuscitated cardiac arrest + HF hospitalization

---

## Key Findings

- Primary endpoint **neutral overall**
- Americas subgroup (US, Canada, Brazil, Argentina): spironolactone **significantly reduced** primary endpoint
- Post-hoc EF analysis: significant benefit in patients with LVEF <55%
- Urinary spironolactone metabolite levels dramatically lower in non-Americas (Russia/Georgia) controls — suspected enrollment contamination

## Methods (brief)

**Disease definition for enrollment:** LVEF ≥45% by echocardiography within 6 months of screening. NYHA II–IV, age ≥50 years (or any age if hospitalised for HF in the prior 12 months).

**Dual qualification pathway** (see [[desai2011topcat]] for full design details):
- *Hospitalization-based:* ≥1 HF hospitalization in the 12 months before screening
- *NP-based (no required hospitalization):* BNP ≥100 pg/mL OR NT-proBNP ≥360 pg/mL within the prior 60 days

**Key exclusion:** LVEF <45% in prior 6 months; eGFR <30 mL/min; K+ >5.0 mEq/L; systolic BP <100 mmHg; planned CABG/PCI/valve surgery.

**Intervention:** Spironolactone titrated from 15 mg → 30 mg → 45 mg over 8 weeks. Down-titrated or discontinued for hyperkalaemia (K+ >5.5) or renal deterioration (eGFR <30 or Cr rise >50%).

**Sites:** 266 centers across 6 countries (US, Canada, Brazil, Argentina, Russia, Georgia). Americas vs. Eastern Europe distinction later became critical to interpretation.

**Parameters collected:**
- *Imaging (echo)*: LVEF, LV volumes, LV mass, LA volume, E/e', tissue Doppler (septal and lateral e')
- *Biomarkers*: BNP, NT-proBNP, aldosterone, renin, potassium, creatinine (serial)
- *Functional*: NYHA class, 6MWD, KCCQ (QoL), 12-lead ECG
- *Urinary*: Spironolactone metabolites (post-hoc, used to assess adherence by region)

## Results

Results from Pitt 2014 (outcomes paper not yet ingested; see [[topcat]] entity page and ESC 2021 summary for key numbers):

- **Primary endpoint overall:** Neutral — spironolactone did not significantly reduce the primary composite of CV death + resuscitated cardiac arrest + HF hospitalisation across the full trial population
- **Americas subgroup (US, Canada, Brazil, Argentina):** Spironolactone significantly reduced the primary endpoint (HR approximately 0.82; p<0.05)
- **Non-Americas (Russia, Georgia):** No benefit detected; event rates in placebo arm unusually low; urinary spironolactone metabolite levels in placebo patients were near-zero, suggesting open-label spironolactone use outside the trial
- **Post-hoc LVEF subgroup:** Significant benefit in LVEF <55%; less benefit in LVEF ≥55%
- Hyperkalaemia more frequent with spironolactone; renal events similar between arms

(source: 2021-ESC-Guidelines-Heart-Failure.pdf; outcomes paper figures pending ingest)

## Limitations

- Suspected enrollment of patients without true HFpEF in non-Americas cohort: urinary spironolactone metabolites near-zero in Russia/Georgia placebo patients → likely receiving open-label spironolactone outside the trial, making the control arm ineffective and the treatment effect undetectable
- Two different inclusion pathways (hospitalization vs. NP-based) enrolled biologically distinct populations; hospitalization-pathway patients were sicker with more definite HFpEF
- Americas vs. non-Americas result divergence: cannot fully separate population differences from trial integrity problems — proportional contribution of each unknown
- Post-hoc subgroup analyses for Americas and EF <55% were not the pre-specified primary hypotheses
- LVEF ≥45% threshold permissive by current standards — includes HFmrEF (LVEF 41–49%) patients
- Local echo reading for LVEF qualification (no central reader)

## Connections
- Supports: [[spironolactone]] — Americas subgroup positive signal
- Supports: [[hfpef-treatment-gap]] — overall neutral result
- Contradicts: [[spironolactone]] Americas vs. overall — fundamental tension

## Secondary Analyses & Data Reuse

| Citekey | Focus | Wiki page |
|---------|-------|-----------|
| Desai2011TOPCAT | Design, eligibility, site infrastructure, baseline characteristics | [[desai2011topcat]] |
| [Americas post-hoc] | Regional subgroup (Americas vs. Eastern Europe) | — |
| [Metabolite analysis] | Urinary spironolactone metabolites; trial integrity assessment | — |
| [LVEF subgroup] | HFmrEF (LVEF 45–55%) post-hoc analysis | — |

Registry: NCT00094302

## Related Pages
- Concepts: [[hfpef-treatment-gap]], [[hf-phenotype-classification]]
- Entities: [[hfpef]], [[hfmref]], [[spironolactone]], [[topcat]]
- Sources: [[mcdonagh2021esc]]

## Contradictions
- Americas vs. non-Americas results are directly contradictory; overall vs. subgroup interpretation remains the most contested issue in HFpEF pharmacotherapy. See [[contradictions]].
