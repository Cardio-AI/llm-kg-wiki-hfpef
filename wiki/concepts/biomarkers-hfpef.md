---
type: concept
title: Biomarkers in HFpEF
summary: "Circulating biomarkers in HFpEF span six functional categories \u2014 natriuretic\
  \ peptides, inflammatory, fibrosis, leukocyte, iron deficiency, and metabolic/renal\
  \ \u2014 each reflecting a distinct pathophysiological axis; no single biomarker\
  \ is sufficient for diagnosis or prognostication; biomarker panels and AI-integrated\
  \ approaches are the direction of the field."
tags:
- biomarker
- diagnosis
- prognosis
- hfpef
- mechanism
created: 2026-05-19
last_updated: 2026-05-19
sources:
- citekey: ammar2025bnp
  doi: null  # needs source — see wiki/citations-doi-review.md
- citekey: hage2026ntprobnp
  doi: 10.1016/j.ijcard.2026.134554
- citekey: boralkar2019nlr
  doi: null  # needs source — see wiki/citations-doi-review.md
- citekey: fu2024inflammation
  doi: null  # needs source — see wiki/citations-doi-review.md
- citekey: verma2024inflammation
  doi: 10.1016/j.jacc.2024.08.028
page-type: concept-page
---
# Biomarkers in HFpEF

> Circulating biomarkers in HFpEF reflect the syndrome's heterogeneous pathophysiology; no single marker is sufficient for diagnosis or prognostication, and the field is moving toward multi-marker panels and AI-integrated biomarker interpretation.

---

## Aliases
| Alias | Type | Notes |
|---|---|---|
| Cardiac biomarkers | descriptive | broader term including structural markers |
| Circulating biomarkers | descriptive | distinguishes from imaging-derived biomarkers (e.g., GLS) |
| HFpEF biomarker panel | descriptive | multi-marker approach |
| Natriuretic peptides | alternate-name | most clinically used subcategory — see [[natriuretic-peptides]] |

---

## Mechanism

Biomarkers in HFpEF reflect six pathophysiological axes, each with distinct clinical correlates:

### 1. Natriuretic Peptides (NPs)

**BNP and NT-proBNP** are secreted by cardiomyocytes in response to increased wall stress and volume overload. They are the only Class I diagnostic biomarkers for HF across all guidelines. See [[natriuretic-peptides]] for full detail.

**Key HFpEF-specific limitations:**
- **Reduced sensitivity** in HFpEF vs. HFrEF: NPs are lower in HFpEF for any given degree of symptomatic HF (mean NT-proBNP in HFpEF ~3× lower than HFrEF at diagnosis)
- **Obesity suppression:** Adipose tissue degrades BNP; obese patients (BMI ≥30) have lower NPs independent of HF severity — EMPEROR-Preserved used obesity-adjusted thresholds
- **AF elevation:** AF per se raises NP levels; most trials require higher NT-proBNP thresholds for AF-positive patients (e.g., EMPEROR-Preserved: >300 pg/mL without AF vs. >900 pg/mL with AF)
- **Glycosylation underestimation (Hage 2026):** Standard Elecsys NT-proBNP assays miss glycosylated NT-proBNP; tNT-proBNP (research-use-only) is ~3.6× higher than standard NT-proBNP in HFpEF; glycosylation is higher in HFpEF than HFrEF (ratio NT-proBNP/tNT-proBNP: 0.27 vs. 0.32; p=0.019), driven by obesity/diabetes/AF (source: [[hage2026ntprobnp]])
- **Prognostic:** Meta-analysis (Ammar 2025) confirms both BNP and NT-proBNP predict outcomes in HFpEF; NT-proBNP may have marginal superiority in sensitivity; tNT-proBNP trended toward better prognostic accuracy (AUROC 0.710 vs. 0.682; p=0.068) (source: [[ammar2025bnp]], [[hage2026ntprobnp]])

**MR-proANP:** ESC-endorsed alternative to NT-proBNP for HFpEF diagnosis (same diagnostic criteria apply).

### 2. Inflammatory Biomarkers

Inflammation is a central pathophysiological axis in HFpEF — particularly the cardiometabolic phenotype (obesity + DM + comorbidities → systemic inflammation → coronary microvascular EndoMT → myocardial fibrosis). Key biomarkers:

| Marker | Role in HFpEF | Notes |
|---|---|---|
| hs-CRP | General inflammation; elevated in HFpEF vs. HFrEF proportionally | Reduced by SGLT2i (empagliflozin) and GLP-1 RA (tirzepatide −38.8% hs-CRP in SUMMIT) |
| IL-6 | Drives CRP; mediates STAT3 → fibrosis | Targeted by tocilizumab (no HFpEF RCT) |
| IL-1β | Direct myocardial depression; target of anakinra (D-HART2) | D-HART2: IL-1 blockade reduced hs-CRP but NOT VO₂ (source: [[vantassell2018dhart2]]) |
| TNF-α | Promotes apoptosis and fibrosis | TNF inhibition trials in HFrEF were neutral; HFpEF untested |
| Galectin-3 | Macrophage-secreted; fibrosis marker; predicts HF events | TOPCAT subanalysis: galectin-3 predicted outcomes in spironolactone-treated patients |
| sST2 (soluble ST2) | Decoy receptor for IL-33; higher sST2 = worse HF prognosis | sST2 elevated in HFpEF; predicts HF hospitalisation (source: [[shi2022sst2]]) |

Inflammatory biomarkers collectively support the **systemic inflammation → myocardial fibrosis** pathway described in the Paulus–Tschöpe paradigm (source: [[paulus2013novelparadigm]]). None is in routine clinical use for HFpEF management.

### 3. Fibrosis Markers

| Marker | Mechanism | Evidence |
|---|---|---|
| Collagen III N-terminal propeptide (PIIICP) | Cross-linked collagen synthesis; correlates with LV stiffness | Reduced GLS (suboptimal LVEF preservation) correlates with increased PIIICP in HFpEF (source: [[upadhya2025echo]]) |
| TGF-β | Master fibrosis regulator; activates myofibroblasts | Elevated in HFpEF myocardial biopsies (source: [[fayyaz2025pathophys]]) |
| Galectin-3 | Both inflammatory and fibrotic (also above) | Dual classification reflects crossover between axes |
| TIMP-1 / MMP ratios | Matrix remodelling balance | Elevated TIMP-1 (reduced MMP activity) → net fibrosis |

### 4. Leukocyte/Haematological Biomarkers

Simple complete blood count (CBC)-derived ratios that capture the inflammatory state without dedicated assays:

| Marker | Evidence | Key Study |
|---|---|---|
| NLR (neutrophil-to-lymphocyte ratio) | Higher NLR predicts HF hospitalisation and mortality in HFpEF; OR ~2–3× per tertile increase | Boralkar 2019 (n=1,155 HFpEF); Tamaki 2023 (source: [[boralkar2019nlr]], [[tamaki2023nlrplr]]) |
| PLR (platelet-to-lymphocyte ratio) | Weaker predictor than NLR; platelet activation marker | Tamaki 2023 (source: [[tamaki2023nlrplr]]) |
| Monocyte-to-lymphocyte ratio (MLR) | Predicts 1-year readmission in HFpEF (ML study) | Hu 2025 — cited in [[ml-ai-hfpef]] |

NLR and PLR are derived from standard clinical CBC — no additional cost. Clinically, elevated NLR (>3.0) signals high inflammatory burden and poor prognosis. The mechanism: neutrophil-dominant inflammation → myocardial oxidative stress; lymphopenia → impaired immune regulation of fibrosis.

### 5. Iron Deficiency Markers

Iron deficiency (ID) affects ~50–60% of HFpEF patients (source: [[beale2019iron]]). ID is associated with worse VO₂, 6MWT, and QoL independent of anaemia.

| Marker | Threshold for ID in HF | Notes |
|---|---|---|
| Ferritin | <100 ng/mL (absolute ID) or 100–299 ng/mL (functional ID if TSAT <20%) | ESC guidelines apply to HFmrEF; HFpEF evidence is emerging (FAIR-HFpEF N=39) |
| Transferrin saturation (TSAT) | <20% | Combined with ferritin for functional ID |
| Serum iron | Low | Less reliable than ferritin/TSAT in chronic disease |

No Class I recommendation for IV iron in HFpEF from any guideline society (ESC Class IIa for HFmrEF only). FAIR-HFpEF (N=39) showed +49 m 6MWD with ferric carboxymaltose (p=0.029) — underpowered but directionally positive (source: [[sauer2026pharmacological]]).

### 6. Metabolic and Renal Markers

| Marker | HFpEF relevance |
|---|---|
| HbA1c | T2DM prevalence ~40% in HFpEF; marker of glycaemic burden driving glycosylation of NT-proBNP |
| Cystatin C / eGFR-cystatin | Preferred eGFR marker for HFpEF patients on incretin-based therapy (SGLT2i, GLP-1 RA) — no early dip artifact (SUMMIT CKD subanalysis: net improvement +3.3 mL/min/1.73m² at 52 weeks with tirzepatide) |
| Uric acid | Hyperuricaemia in HFpEF; xanthine oxidase-mediated oxidative stress |
| Adiponectin / leptin | Dysregulation in obesity-HFpEF phenotype; leptin promotes cardiac fibrosis |
| Troponin (hs-TnI/T) | Subtle cardiomyocyte injury in HFpEF; prognostic but not diagnostic |

### 7. Structural / Imaging-Derived Biomarkers

Echo-derived markers that function like biomarkers in clinical risk stratification:
- **GLS (global longitudinal strain):** Subclinical systolic dysfunction in HFpEF; <−16% = minor HFA-PEFF criterion; correlates with PIIICP collagen synthesis (source: [[upadhya2025echo]])
- **LASr (LA reservoir strain):** Superior LVFP estimator to TRV; <18% = third criterion in updated ASE/EACVI algorithm; predicts composite outcomes in HFpEF (source: [[upadhya2025echo]])
- **E/e' ratio:** Continuous predictor of LVFP (OR per unit: 1.22; CI 1.16–1.30); most studied single echo biomarker for HFpEF diagnosis
- **CMR-derived markers:** LV mass (tirzepatide −11 g; p=0.004 in SUMMIT CMR substudy), ECV (extracellular volume fraction for fibrosis) — see [[cardiac-mri]]

---

## Clinical Relevance

**For diagnosis:**
Standard clinical workflow uses NT-proBNP ≥125 pg/mL (at rest) or ≥360 pg/mL (after exercise) as a necessary (not sufficient) HFpEF criterion. However:
- Obese or diabetic patients may have falsely normal NT-proBNP despite true HFpEF (glycosylation problem; Hage 2026)
- NT-proBNP negative predictive value is high (NPV ~85–90%) — a truly low NT-proBNP makes HFpEF less likely, but not impossible
- H₂FPEF and HFA-PEFF scores incorporate NT-proBNP as one of several parameters — single-marker diagnosis is insufficient

**For prognosis:**
Multiple biomarkers independently predict outcomes in HFpEF:
- NT-proBNP/BNP: strongest, most consistent predictor
- NLR: independent of NPs; adds prognostic information from simple CBC
- sST2 and galectin-3: add fibrosis/inflammation dimension
- GLS and LASr: echo-derived biomarkers superior to volumetric markers alone

**For treatment targeting:**
- Inflammatory biomarkers (hs-CRP, IL-6, IL-1β): no validated treatment targets yet; D-HART2 (anakinra) reduced inflammation but not VO₂
- SGLT2i reduce hs-CRP and NT-proBNP — both anti-inflammatory and haemodynamic mechanisms
- Tirzepatide (SUMMIT) reduced hs-CRP by 38.8% vs. placebo — largest anti-inflammatory effect of any HFpEF drug
- Iron supplementation targets ferritin/TSAT deficiency

---

## History

- **Pre-2010** — BNP/NT-proBNP established as diagnostic markers for acute HF; role in HFpEF recognised but thresholds uncertain (lower NPs in HFpEF than HFrEF)
- **2013** — Paulus & Tschöpe paradigm: systemic inflammation → myocardial fibrosis as HFpEF mechanism; inflammatory biomarkers (IL-6, TNF-α, hs-CRP) gain mechanistic relevance (source: [[paulus2013novelparadigm]])
- **2015** — Shah phenomapping: galectin-3, sST2, NPs cluster with distinct HFpEF phenotypes; inflammation markers identify highest-risk cluster (source: [[shah2015phenomapping]])
- **2018** — Beale 2019 systematic review: iron deficiency prevalence 59% in HFpEF; independent association with reduced VO₂ (source: [[beale2019iron]])
- **2019** — Boralkar 2019: NLR independently predicts HF hospitalisation in HFpEF N=1,155; first large study of CBC-derived inflammatory markers in HFpEF (source: [[boralkar2019nlr]])
- **2022** — sST2: Shi 2022 confirms prognostic role in HFpEF cohort; sST2 predicts HF hospitalisation independent of NT-proBNP (source: [[shi2022sst2]])
- **2025** — Ammar 2025 meta-analysis: systematic comparison of BNP vs. NT-proBNP in HFpEF prognosis; NT-proBNP marginally superior in sensitivity (source: [[ammar2025bnp]])
- **2026** — Hage 2026: tNT-proBNP (total, including glycosylated forms) systematically higher than standard NT-proBNP; HFpEF has higher glycosylation ratio than HFrEF; obesity/DM/AF drive glycosylation; tNT-proBNP trended toward better prognostic AUROC (source: [[hage2026ntprobnp]])

---

## Evidence

Current biomarker evidence in HFpEF is largely **observational and prognostic**, not interventional:
- NT-proBNP/BNP: Class I diagnostic; strong prospective prognostic evidence across multiple cohorts
- sST2, galectin-3: moderate prognostic evidence; no treatment response use established
- NLR/PLR: consistent observational data; simple and low-cost; no interventional evidence
- tNT-proBNP: promising but exploratory (N=83 HFpEF; research assay only)
- Iron biomarkers (ferritin/TSAT): strong HF evidence (HFrEF); limited HFpEF-specific RCT data

---

## Open Questions

- Will tNT-proBNP (measuring glycosylated forms) improve HFpEF diagnosis and prognosis sufficiently to justify commercial assay development, particularly for obese/DM populations?
- Can multi-biomarker panels (NP + inflammatory + fibrosis + iron) improve prognostication over NT-proBNP alone sufficiently to change clinical management?
- Do inflammatory biomarkers (sST2, galectin-3, IL-6) predict treatment response to specific therapies (e.g., high-sST2 → SGLT2i responder)?
- Is there an NLR or inflammatory threshold that should trigger anti-inflammatory therapy workup in HFpEF?
- How should NT-proBNP diagnostic thresholds be adjusted for obese HFpEF patients given the glycosylation underestimation demonstrated by Hage 2026?
- Does SGLT2i-mediated hs-CRP reduction (observed in EMPEROR-Preserved) translate to greater benefit in high-inflammatory phenotype HFpEF?

---

## Related Pages

- Concepts: [[natriuretic-peptides]], [[hfpef-diagnosis]], [[hfpef-phenotype-profiling]], [[ml-ai-hfpef]], [[diastolic-dysfunction]]
- Entities: [[echocardiography]], [[cardiac-mri]], [[finearts-hf]], [[summit]], [[sglt2-inhibitors]]
- Sources: [[ammar2025bnp]], [[hage2026ntprobnp]], [[boralkar2019nlr]], [[tamaki2023nlrplr]], [[shi2022sst2]], [[beale2019iron]], [[fu2024inflammation]], [[verma2024inflammation]], [[paulus2013novelparadigm]]

## Contradictions

- **tNT-proBNP vs. standard NT-proBNP (Hage 2026):** tNT-proBNP tends to be more prognostic (AUROC 0.710 vs. 0.682) but the difference is NS (p=0.068) in a small cohort (N=83). Whether this reflects a true analytic advantage or noise is unresolved. See [[contradictions]].
- **NT-proBNP obesity paradox:** Standard NT-proBNP is lower in obese HFpEF patients, yet obese HFpEF has similar or worse outcomes — partly explained by glycosylation suppression (Hage 2026) and adipose tissue degradation of BNP. The relative contribution of each mechanism is uncertain.
