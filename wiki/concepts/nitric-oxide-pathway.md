---
page-type: mechanism-page
title: Nitric Oxide Pathway in HFpEF
summary: Reduced NO bioavailability is a central mechanism in HFpEF linking systemic inflammation and endothelial dysfunction to impaired LV relaxation, exercise arterial stiffening, and diastolic dysfunction; impaired cGMP-PKG signalling downstream of NO deficiency reduces titin phosphorylation, increases cardiomyocyte stiffness, and impairs myofilament calcium sensitivity; inorganic nitrite partially restores exercise hemodynamics.
tags:
  - hfpef
  - nitric-oxide-pathway
  - mechanism
  - endothelial-dysfunction
  - treatment
created: 2026-05-19
last_updated: 2026-05-19
sources:
  - citekey: Reddy2017ArtStiff
    doi: 10.1016/j.jacc.2017.05.029
  - citekey: Paulus2013NovelParadigm
    doi: 10.1016/j.jacc.2013.02.092
---

# Nitric Oxide Pathway in HFpEF

> Endothelial NO deficiency creates a downstream cGMP-PKG signalling deficit that impairs cardiomyocyte relaxation and increases passive stiffness; the same NO deficit prevents exercise-induced vasodilation, amplifying arterial stiffness and filling pressure elevation during exercise.

## Aliases
| Alias | Type | Notes |
|---|---|---|
| NO/cGMP/PKG pathway | mechanism | full signalling cascade |
| cGMP-PKG pathway | abbreviation | downstream of NO |
| Endothelial dysfunction | broader-term | includes NO deficit and other mechanisms |

## Mechanism

### Upstream: NO Deficiency

Comorbidities in HFpEF (hypertension, obesity, diabetes, aging) → endothelial activation:
1. Systemic inflammation → ROS production → NO scavenging (peroxynitrite formation)
2. Endothelial eNOS uncoupling → impaired NO synthesis
3. Oxidative stress → reduced BH4 availability → eNOS dysfunction
4. Result: **chronically reduced NO bioavailability** (source: [[paulus2013novelparadigm]])

### Downstream: Cardiac cGMP-PKG Signalling Deficit

Reduced NO → ↓ soluble guanylate cyclase (sGC) activation → ↓ cGMP → ↓ PKG activity:

| PKG function lost | Consequence in HFpEF |
|---|---|
| Titin phosphorylation (N2B element) | ↑ titin-based passive stiffness → ↑ diastolic stiffness |
| Myofilament calcium sensitivity ↓ | Slowed relaxation, longer isovolumetric relaxation time |
| RhoA/ROCK pathway inhibition | ↑ myosin phosphorylation → impaired relaxation |
| Anti-hypertrophic signalling | ↑ concentric hypertrophy |

This is the core cellular mechanism linking inflammation to diastolic dysfunction (source: [[paulus2013novelparadigm]])

### Exercise-Induced Arterial Stiffening

In HFpEF, exercise-induced vasodilation is blunted due to reduced NO availability:
- Normal: exercise → endothelium-dependent NO release → arteriolar dilation → ↓ wave reflections
- HFpEF: impaired NO release → failure to dilate → ↑ arterial elastance (Ea), ↑ augmentation index (AIx)
- Consequence: exercise PCWP elevation + reduced CO (source: [[reddy2017artstiff]])

## Evidence: Nitrite Restoration

Inorganic sodium nitrite (NaNO₂) is a NO precursor; at exercise:
- **PCWP: −8±1 mmHg** (P<0.0001) — reduced filling pressures
- **CO: +0.8±0.3 L/min** (P=0.01) — improved output
- **TACI: +0.10±0.02** (P=0.0005) — improved arterial compliance
- **AIx: −8±2%** (P<0.0001) — reduced wave reflections

Confirms that acute NO delivery can partially reverse exercise-induced hemodynamic impairment in HFpEF (source: [[reddy2017artstiff]])

## Therapeutic Implications

- **Nitrates (organic):** NEAT-HFpEF showed no benefit with isosorbide mononitrate in stable HFpEF — likely tolerance, neurohormonal activation, or wrong population (source: [[redfield2015neat]])
- **Inorganic nitrite/nitrate:** Avoids organic nitrate tolerance; preclinical and phase 2 data promising; no large RCT
- **PDE5 inhibitors (sildenafil):** RELAX trial: no benefit in HFpEF — possible compensatory downregulation of sGC (source: [[redfield2013relax]])
- **sGC stimulators (e.g., vericiguat):** SOCRATES-PRESERVED (phase 2): reduced NT-proBNP trend but primary endpoint not significant; large HFpEF trial not completed
- **SGLT2 inhibitors:** Indirect — reduce ROS, improve endothelial function, restore NO bioavailability
- **GLP-1 RA:** Improve endothelial function and reduce systemic inflammation → partial NO restoration

## Open Questions

- Why do organic nitrates fail despite the NO deficit hypothesis? (neurohormonal reflex, tolerance, wrong phenotype targeted)
- Which HFpEF phenotype is most likely to respond to NO-pathway augmentation?
- Can sGC stimulators overcome the failure of PDE5 inhibitors in HFpEF?

## Related Concepts

- [[arterial-stiffness]] — exercise arterial stiffening driven by NO deficiency
- [[diastolic-dysfunction]] — cGMP-PKG pathway deficit causes titin-based diastolic stiffness
- [[coronary-microvascular-dysfunction]] — endothelial dysfunction impairs microvascular NO-mediated dilation
- [[inflammation-hfpef]] — inflammation is the upstream driver of NO deficiency
- [[sgc-stimulators]] — downstream pharmacological target of the NO/cGMP/PKG pathway
- [[ranolazine]] — late Na⁺ current inhibitor with a parallel, NO-independent effect on diastolic stiffness

## References
- Reddy YNV, Andersen MJ, Obokata M, Koepp KE, Kane GC, Melenovsky V, Olson TP, Borlaug BA. Arterial Stiffening With Exercise in Patients With Heart Failure and Preserved Ejection Fraction. *J Am Coll Cardiol.* 2017;70(2):136–148. doi:[10.1016/j.jacc.2017.05.029](https://doi.org/10.1016/j.jacc.2017.05.029)
- Paulus WJ, Tschöpe C. A Novel Paradigm for Heart Failure With Preserved Ejection Fraction: Comorbidities Drive Myocardial Dysfunction and Remodeling Through Coronary Microvascular Endothelial Inflammation. *J Am Coll Cardiol.* 2013;62(4):263–271. doi:[10.1016/j.jacc.2013.02.092](https://doi.org/10.1016/j.jacc.2013.02.092)
- Redfield MM, Anstrom KJ, Levine JA, et al.; NHLBI Heart Failure Clinical Research Network. Isosorbide Mononitrate in Heart Failure with Preserved Ejection Fraction. *N Engl J Med.* 2015;373(24):2314–2324. doi:[10.1056/NEJMoa1510774](https://doi.org/10.1056/NEJMoa1510774)
- Redfield MM, Chen HH, Borlaug BA, et al.; NHLBI Heart Failure Clinical Research Network. Effect of Phosphodiesterase-5 Inhibition on Exercise Capacity and Clinical Status in Heart Failure With Preserved Ejection Fraction: A Randomized Clinical Trial. *JAMA.* 2013;309(12):1268–1277. doi:[10.1001/jama.2013.2024](https://doi.org/10.1001/jama.2013.2024)
