---
type: concept
title: HFpEF Phenotype Profiling
summary: Two-layer treatment model for HFpEF — SGLT2i universal foundation for all patients, with additional phenotype-guided therapy based on 18 comorbidity phenotypes; operationalised by the HFA/ESC 2023 consensus statement and complementary to the ACC 2023 ECDP.
tags:
  - hfpef
  - phenotype
  - treatment
  - comorbidity
  - mechanism
created: 2026-05-06
last_updated: 2026-05-14
sources:
  - file: raw/2023-ESC-Anker_HFpEF_phenotyping.pdf
    citekey: Anker2023HFpEFPhenotype
  - file: raw/2023-JACC-Kittleson-ACC_expert_consensu_HFpEF.pdf
    citekey: Kittleson2023ACC
  - file: raw/2023-JACC-Borlaug-HFpEF_scientific_statement.pdf
    citekey: borlaug2023statement
  - file: raw/2023-FrontCardiovascMed-Manabe-sympathic_hemodynamics_exercise.pdf
    citekey: manabe2023sympathetic
---
# HFpEF Phenotype Profiling

> HFpEF is a heterogeneous syndrome driven by multiple comorbidities; the 2023 consensus approach provides a two-layer model — SGLT2i for all patients, with add-on therapy targeted to the dominant comorbidity phenotype.

---

## Aliases
| Alias | Type | Notes |
|---|---|---|
| Phenotype-guided therapy | descriptive | clinical application of the two-layer model |
| Comorbidity phenotypes | descriptive | the 18 comorbidity phenotypes in the HFA/ESC framework |
| HFA phenotype statement | abbreviation | refers to Anker 2023 HFA/ESC consensus document |
| Precision medicine HFpEF | descriptive | broader framing; overlaps with [[ml-ai-hfpef]] |
| Treatment wheel | descriptive | informal name for Figure 2 in Anker 2023 phenotype statement |
| Phenomapping | research-name | data-driven phenotype derivation; see also [[shah2015phenomapping]] |

---

## Mechanism

HFpEF is not a single disease but a phenotypically heterogeneous clinical syndrome. LV diastolic dysfunction may reflect cardiovascular, metabolic, pulmonary, renal, or geriatric drivers operating in varying combinations. A single pharmacological agent cannot address all these pathways simultaneously, which partly explains the repeated failure of universal HFpEF pharmacotherapy trials. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

The phenotype profiling framework proposes that optimal outcomes require:
1. **Universal treatment** targeting pathways active in all or most HFpEF patients
2. **Phenotype-specific add-on** targeting the dominant individual comorbidity

---

## The Two-Layer Model

### Layer 1: Universal — SGLT2i for All HFpEF

SGLT2 inhibitors (dapagliflozin, empagliflozin) are the **only pharmacotherapy proven to improve clinical outcomes across the HFmrEF/HFpEF spectrum** (LVEF >40%). Both EMPEROR-Preserved and DELIVER showed consistent benefit regardless of LVEF, sex, or T2DM status. A 5-trial meta-analysis confirmed significant reduction in HHF + CV death. SGLT2i are thus the universal foundation. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

Diuretics are added for decongestion when fluid retention is present.

### Layer 2: Phenotype-Guided Add-On (Figure 2, Anker 2023)

| Phenotype | Prevalence | Specific add-on |
|---|---|---|
| Arterial hypertension | 60–80% | ACEi/ARB/ARNi, indapamide, nebivolol, MRA, Ca-channel blockers |
| Iron deficiency | 20–50% | Ferric carboxymaltose (IV; FAIR-HFpEF, PREFER-HF ongoing) |
| Obesity | 30–40% | Semaglutide (STEP-HFpEF, NEJM 2023); tirzepatide (SUMMIT, NEJM 2025 — event reduction HR 0.62) |
| Type 2 diabetes | 20–40% | GLP-1 RA, metformin, finerenone (if CKD) |
| Atrial fibrillation | 15–30% | Dronedarone, PVI; CABA-HFpEF ongoing |
| Ischaemic heart disease | 40–70% | Beta-blockers, Ca-channel blockers, ranolazine, trimetazidine |
| COPD | 15–20% | LAMA/LABA; β1-selective beta-blockers |

(source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

---

## Clinical Relevance

### Primary HFpEF Phenotypes

**Age:** Two distinct age-phenotypes. Younger (<65): male predominance, obesity/DM, higher CV death risk. Older (>65): white women, AF/CKD/hypertension, more non-CV mortality.

**Sex:** Women predisposed via concentric remodelling, lower diastolic compliance, mitochondrial differences. PARAGON-HF sex-treatment interaction (women HR 0.73, men HR 1.03) supports sex-stratified ARNI therapy — consistent with [[kittleson2023acc]] recommendation.

**LVEF 50–55% (Borderline subgroup):** Distinct from normal LVEF (male 52–72%, female 54–74%). Worse outcomes. Beneficial treatment responses across TOPCAT (spironolactone), PARAGON-HF (sacubitril/valsartan ≤median LVEF 57%), and EMPEROR-Preserved (empagliflozin ≥50% to <64%). Not a simple HFmrEF equivalent.

**Very high LVEF (>65%/>70%):** U-shaped mortality (lowest at 60–65%). Mandates secondary HFpEF workup: ATTR (ATTRwt in 13% of HFpEF with LVH), HOCM, paradoxical low-gradient aortic stenosis, Fabry disease. Specific treatments exist for each aetiology.

**Iron deficiency (50–75%):** Most underrecognised. Mechanism: reduced O2 delivery + skeletal muscle iron-dependent oxidative phosphorylation. Ferric carboxymaltose trials ongoing (FAIR-HFpEF, PREFER-HF). (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

**Coronary microvascular dysfunction (CMD):** Present in ~71–91% of HFpEF (PROMIS-HFpEF: 66% endothelium-independent + 24% endothelium-dependent). CMD → myocardial fibrosis → worse diastolic function → worse outcomes. Therapeutic target but no large RCT yet. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

**Chronotropic incompetence (30–50%):** Beta-blocker withdrawal significantly increased functional capacity and VO2 in this subgroup — beta-blockers harmful when chronotropic incompetence is dominant. However, warranted in hypertension or ischaemic disease subgroups. Rate-adaptive pacing: did not improve exercise capacity. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

**Cancer therapy-induced HFpEF:** Doxorubicin → diastolic dysfunction in 60% at 1 year, 80% at 3 years. All major HFpEF RCTs (including SGLT2i trials) excluded cancer patients. No evidence base for SGLT2i in this subgroup; general HFpEF principles apply with caution. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)

### Borlaug 2023 Five-Phenotype Model (JACC Scientific Statement)

Distinct from the HFA comorbidity wheel (which is comorbidity-driven), the Borlaug 2023 model proposes five overlapping pathophysiological phenogroups based on dominant mechanistic driver:

| Phenogroup | Core Pathophysiology | Key Marker |
|---|---|---|
| Obese/cardiometabolic | Volume excess, pericardial fat, metabolic stress | BMI ≥30, T2DM, metabolic syndrome |
| Arterial stiffening | Increased LV afterload, impaired ventriculovascular coupling | Elevated pulse pressure, aortic stiffness |
| Ischemic (CMD/epicardial CAD) | Coronary microvascular dysfunction → myocardial fibrosis | Stress imaging, coronary CTA |
| Pulmonary vascular disease | RV-pulmonary coupling impairment, elevated PVR | TR velocity, mPAP, RV strain |
| LA myopathy | LA reservoir/booster dysfunction, AF as biomarker | LA strain, LAVI, AF burden |

These phenogroups overlap substantially — a single patient may fall into 3–4 simultaneously. The model is not mutually exclusive but helps identify the dominant mechanistic target. Non-HFpEF "masqueraders" (ATTR, HCM, sarcoidosis, Fabry, restrictive CMP, high-output HF) must be excluded first (Table 2, Borlaug 2023). (source: 2023-JACC-Borlaug-HFpEF_scientific_statement.pdf)

**Disease Progression Spectrum (Central Illustration):** 4-chamber sequential involvement — LV filling pressure elevation → LA enlargement/dysfunction → pulmonary venous hypertension → secondary PH → RV dysfunction → "Stage D" right heart failure. ~80% of HFpEF patients develop PH; PH drives eventual RV failure. AF present in ~80% of those with resting LA hypertension — AF is both a cause and consequence of LA myopathy.

### Autonomic Dysfunction as Phenotypic Axis

Excessive sympathetic activation during dynamic exercise — paradoxical MSNA increase during cycling — is an underrecognised phenotypic axis. Distinct from HFrEF pattern (both show MSNA increase during dynamic exercise, but HFpEF response appears greater; during static exercise HFpEF MSNA resembles controls). Excessive MSNA → elevated SVR → reduced skeletal muscle blood flow → VO₂ limitation. May explain the HFpEF-specific response to candesartan (reduced peak SBP and improved exercise duration) not seen in hypertensive controls. (source: 2023-FrontCardiovascMed-Manabe-sympathic_hemodynamics_exercise.pdf)

### Secondary HFpEF (Mimics)
Four main categories requiring specific management rather than standard HFpEF treatment: restrictive cardiomyopathy (ATTR, AL amyloidosis, Fabry), hypertrophic cardiomyopathy, constrictive pericarditis, valvular heart disease. Secondary HFpEF requires extended diagnostic workup (CMR, Tc-PYP, biopsy, genetic testing). See [[hfpef-diagnosis]] and [[kittleson2023acc]] Table 1.

---

## History

- **Pre-2021:** HFpEF treated as one entity; universal pharmacotherapy approach repeatedly failed (CHARM-Preserved, I-PRESERVE, TOPCAT, PARAGON-HF)
- **2021–2022:** EMPEROR-Preserved (2021) and DELIVER (2022) — first positive trials; both tested SGLT2i across full HFpEF spectrum. AHA 2022: SGLT2i Class 2a.
- **2023 — HFA/ESC consensus (Anker 2023):** Formal phenotype profiling framework proposed; SGLT2i as universal layer; comorbidity-based add-on structured into 7 phenotype categories. Concurrent with ACC 2023 ECDP ([[kittleson2023acc]]) — two complementary 2023 documents from opposite sides of the Atlantic that operationalise the same treatment concept. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf)
- **2023 — Borlaug JACC Scientific Statement:** Proposed five overlapping pathophysiological phenogroups with Venn diagram framing (see below). Central Illustration: sequential disease progression — exercise-induced LA hypertension → resting LA hypertension → pulmonary hypertension → RV dysfunction. Autonomic dysfunction (chronotropic incompetence, sympathetic excess) added as a cross-cutting phenotypic axis. (source: 2023-JACC-Borlaug-HFpEF_scientific_statement.pdf)
- **2023–2025 published:** STEP-HFpEF (semaglutide, NEJM 2023 — symptomatic benefit), FINEARTS-HF (finerenone, NEJM 2024 — RR 0.84; P=0.007), SUMMIT (tirzepatide, NEJM 2025 — HR 0.62 event reduction). Ongoing: CABA-HFpEF, FAIR-HFpEF, SPIRIT-HF — results will further populate specific phenotype branches.

---

## Evidence

### Concordance with ACC 2023 ECDP
Anker 2023 and [[kittleson2023acc]] reach the same core conclusions independently: SGLT2i first; sex-stratified MRA/ARNI; GLP-1 RA for obesity; ATTR screening. Key difference: Kittleson operationalises via a sequential algorithm (Figure 9, EF + sex thresholds); Anker operationalises via a comorbidity wheel (Figure 2, phenotype categories). Both explicitly flag SUMMIT, STEP-HFpEF, and FINEARTS-HF as evidence gaps. (source: 2023-ESC-Anker_HFpEF_phenotyping.pdf; source: 2023-JACC-Kittleson-ACC_expert_consensu_HFpEF.pdf)

### Ongoing Trials that Will Define Future Phenotype Branches
| Trial | Intervention | Phenotype target | NCT |
|---|---|---|---|
| FINEARTS-HF | Finerenone | All HFpEF (LVEF ≥40%, eGFR ≥25) | NCT04435626 |
| SUMMIT | Tirzepatide (GLP-1/GIP; published NEJM 2025 — HR 0.62) | Obesity HFpEF | NCT04847557 |
| STEP-HFpEF | Semaglutide (published NEJM 2023 — KCCQ +7.8 pts) | Obesity HFpEF | NCT04788511 |
| CABA-HFpEF | Catheter ablation | HFpEF with AF | NCT05508256 |
| FAIR-HFpEF | Ferric carboxymaltose | HFpEF with iron deficiency | NCT03074591 |
| SPIRIT-HF | Spironolactone | All HFpEF | NCT04727073 |
| APPOLLO-B | Patisiran | ATTR-CM | NCT03997383 |

---

## Open Questions
- Can the phenotype profiling approach be validated in a prospective trial where therapy is phenotype-assigned vs. universal?
- At what point does comorbidity overlap (e.g., T2DM + obesity + hypertension) require prioritisation between add-on agents?
- Will CMD emerge as an actionable therapeutic target once RCT data exist?
- What is the safest approach to SGLT2i in cancer HFpEF patients on cytotoxic chemotherapy?
- Does LVEF 50–55% warrant an intermediate phenotype definition distinct from HFmrEF?

---

## Related Pages
- Concepts: [[hfpef-treatment-gap]], [[guideline-comparison]], [[hfpef-diagnosis]], [[exercise-intolerance]], [[diastolic-dysfunction]], [[ml-ai-hfpef]]
- Entities: [[hfpef]], [[sglt2-inhibitors]], [[spironolactone]], [[sacubitril-valsartan]], [[atrial-fibrillation]], [[supervised-exercise-training]]
- Sources: [[anker2023hfpefphenotype]], [[kittleson2023acc]], [[mcdonagh2021esc]], [[heidenreich2022aha]], [[anker2021emperor]], [[solomon2022deliver]], [[borlaug2023statement]], [[manabe2023sympathetic]]

## Contradictions
- Beta-blockers: harmful in chronotropic incompetence subgroup; beneficial in hypertension + ischaemic disease subgroups. Same drug with opposite effects across HFpEF phenotypes — phenotype identification is prerequisite for prescribing.
- SGLT2i benefit at LVEF >65% uncertain; "universal" recommendation may need secondary HFpEF exclusion first.

See [[contradictions]].
