---
type: concept
title: Pulmonary Hypertension in HFpEF
summary: PH is present in ~50–80% of HFpEF patients (PASP >35 mmHg); ESC classifies as Group 2 PH (LHD); two haemodynamic subtypes — IpcPH (isolated post-capillary; pure passive) and CpcPH (combined pre+post-capillary; with pulmonary vasculopathy); PAC is a stronger outcome predictor than PVR in HFpEF-PH.
tags:
  - hfpef
  - mechanism
  - diagnosis
  - pulmonary
  - haemodynamics
created: 2026-05-13
last_updated: 2026-05-13
sources:
  - file: raw/2015-JACC-Al-Naamani-pulmonary-arterial-capacitance.pdf
    citekey: AlNaamani2015PAC
  - file: raw/2013-JACC-Paulus-Tschoeppe-HFpEF_novel_paradigm.pdf
    citekey: Paulus2013NovelParadigm
---
# Pulmonary Hypertension in HFpEF

> PH is present in 50–80% of HFpEF patients and is an independent predictor of mortality; CpcPH (with pulmonary vasculopathy) carries worse prognosis than IpcPH (pure passive congestion); PAC outperforms PVR for outcome prediction in this population.

---

## Aliases
| Alias | Type | Notes |
|---|---|---|
| PH-HFpEF | abbreviation | common research shorthand |
| Group 2 PH | research-name | ESC/ERS classification — left heart disease |
| CpcPH | abbreviation | combined pre- and post-capillary PH |
| IpcPH | abbreviation | isolated post-capillary PH |
| PH-LHD | abbreviation | pulmonary hypertension due to left heart disease |

---

## Mechanism

HFpEF elevates left atrial and pulmonary venous pressures chronically. This passive pressure transmission raises pulmonary arterial pressure (PAP), initially without pulmonary vascular disease. Over time, ~30–40% of HFpEF-PH patients develop superimposed pulmonary vasculopathy — vasoconstriction, vascular remodelling, endothelial dysfunction — converting IpcPH to CpcPH.

Paulus and Tschöpe (2013) proposed that obesity and metabolic comorbidities cause systemic inflammation (elevated TNF-α, IL-6) → coronary microvascular endothelial inflammation → reduced NO bioavailability → cGMP/PKG deficiency → cardiomyocyte hypertrophy and titin hypophosphorylation. The same inflammatory milieu drives pulmonary endothelial dysfunction and early vasculopathy. Additionally, right atrial dilatation in HFpEF exceeds what is expected for the degree of pulmonary pressure elevation — attributed partly to high obesity prevalence and increased plasma volume rather than pressure load alone. (source: raw/2013-JACC-Paulus-Tschoeppe-HFpEF_novel_paradigm.pdf)

---

## Haemodynamic Classification (ESC/ERS 2015)

| Type | mPAP | PAWP | PVR | DPG | Notes |
|---|---|---|---|---|---|
| IpcPH | >20 mmHg | >15 mmHg | ≤3 WU | <7 mmHg | Passive; no pulmonary vasculopathy; elevated PAWP explains PAP rise |
| CpcPH | >20 mmHg | >15 mmHg | >3 WU | ≥7 mmHg | Reactive; pulmonary vasculopathy on top of elevated PAWP |

DPG (diastolic pressure gradient) = dPAP − PAWP; PVR = (mPAP − PAWP) / CO in Wood units.

---

## Pulmonary Arterial Capacitance (PAC) — Key Diagnostic Variable

Al-Naamani 2015 (JACC): In HFpEF patients with PH (N≈100), PAC (= stroke volume / pulse pressure of PA) was a significantly stronger predictor of outcomes than PVR or DPG:

| Variable | AUC for outcome prediction |
|---|---|
| PAC | 0.73 |
| PVR | 0.37 |
| DPG | — (inferior) |

PAC reflects pulmonary vascular stiffness — captures early vasculopathy before PVR rises. PVR is a late and insensitive marker in HFpEF-PH because the haemodynamic phenotype is a stiffness problem before it becomes a resistance problem. (source: raw/2015-JACC-Al-Naamani-pulmonary-arterial-capacitance.pdf)

**Contradiction with guidelines:** Current ESC/ACC PH guidelines classify and guide CpcPH vs. IpcPH using PVR and DPG. Al-Naamani 2015 shows PVR is a worse prognostic predictor than PAC in this population — guidelines may be using the wrong haemodynamic variable. See [[contradictions]].

---

## Clinical Relevance

- **Prevalence:** ~50–80% of HFpEF patients have PASP >35 mmHg on echo; invasive confirmation via right heart catheterisation required for classification
- **Prognosis:** CpcPH independently associated with higher mortality vs. IpcPH or no PH in HFpEF; RV failure develops in advanced CpcPH
- **Diagnosis:** Echo PASP >35 mmHg raises suspicion; right heart catheterisation required to distinguish IpcPH vs. CpcPH (PAWP >15 mmHg in both)
- **Treatment gap:** No specific pharmacological therapy proven for CpcPH in HFpEF; PDE5i (sildenafil) neutral in RELAX (HFpEF without PH-specific selection); ERA and prostanoids carry risk in Group 2 PH (may worsen pulmonary oedema by increasing venous return to a stiff LV)
- **SGLT2i:** Post-hoc signals of pulmonary pressure reduction in EMPEROR-Preserved subanalyses — mechanism unclear; no dedicated PH-HFpEF RCT

---

## Open Questions

- Does PAC measurement replace PVR/DPG as the preferred haemodynamic phenotyping variable? No RCT uses PAC as an enrolment criterion yet.
- Can CpcPH be reversed by aggressive HFpEF treatment (SGLT2i, diuresis, weight loss) before vascular remodelling becomes fixed?
- Does tirzepatide's paracardiac fat reduction (SUMMIT CMR: −45 mL, P<0.001) translate to pulmonary vascular benefit in obese HFpEF-PH?

---

## Related Pages

- Concepts: [[diastolic-dysfunction]], [[hfpef-phenotype-profiling]], [[exercise-intolerance]]
- Entities: [[hfpef]], [[relax]], [[sglt2-inhibitors]]
- Sources: [[alnaamani2015pac]], [[paulus2013novelparadigm]], [[redfield2013relax]]

## Contradictions

- PAC (AUC 0.73) > PVR (AUC 0.37) for outcome prediction in HFpEF-PH; but ESC/ACC PH guidelines classify CpcPH vs. IpcPH using PVR threshold (>3 WU). See [[contradictions]].
- PDE5i/nitrate class failure in HFpEF (RELAX, NEAT-HFpEF) — yet NO/cGMP pathway is implicated in pulmonary vasculopathy. The agents may not reach sufficient pulmonary vascular concentrations or the vasculopathy in HFpEF-PH is a stiffness rather than vasoconstriction problem. See [[hfpef-treatment-gap]].
