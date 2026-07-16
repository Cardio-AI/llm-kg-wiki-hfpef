---
page-type: mechanism-page
title: CaMKII in HFpEF
summary: Ca²⁺/calmodulin-dependent protein kinase II (CaMKII) overactivation is a shared molecular mechanism between sleep-disordered breathing and HFpEF; intermittent hypoxia/reoxygenation from OSA → ROS → CaMKII oxidation → dysregulated Na⁺/Ca²⁺ homeostasis → impaired diastolic SR Ca²⁺ reuptake + late Na⁺ current activation → afterdepolarisations → atrial arrhythmias and worsened diastolic dysfunction.
tags:
  - hfpef
  - camkii
  - mechanism
  - calcium-signaling
  - sleep-disordered-breathing
  - arrhythmia
created: 2026-05-19
last_updated: 2026-05-19
sources:
  - citekey: Wester2023SDB
    doi: 10.3390/biomedicines11113038
---

# CaMKII in HFpEF

> CaMKII overactivation is a newly identified molecular pathway linking sleep-disordered breathing to HFpEF diastolic dysfunction and atrial arrhythmia; intermittent hypoxia oxidizes CaMKII, causing dysregulated calcium handling and creating an arrhythmogenic substrate.

## Aliases
| Alias | Type | Notes |
|---|---|---|
| Ca²⁺/calmodulin-dependent protein kinase II | full-name | formal biochemical designation |
| CaMKII oxidation | mechanism | specific activation mode in hypoxia/SDB |
| CaMKII-MMP2 pathway | mechanism | leads to myocardial fibrosis via MMP2 |

## Molecular Mechanism

**Intermittent hypoxia/reoxygenation (from OSA) → CaMKII overactivation:**

1. Intermittent hypoxia/reoxygenation → ↑ mitochondrial ROS production
2. ROS oxidize CaMKII at Met281/282 → **constitutive activation** (independent of Ca²⁺)
3. Activated CaMKII → **hyperphosphorylation of:**
   - Ryanodine receptor (RyR2) → ↑ SR Ca²⁺ leak → ↑ diastolic [Ca²⁺]
   - Phospholamban (PLN) → initially ↑ SR Ca²⁺ uptake; with chronic overactivation → desensitization
4. Net result: **dysregulated Na⁺/Ca²⁺ homeostasis** → impaired diastolic SR Ca²⁺ reuptake → slower LV relaxation

(source: [[wester2023sdb]])

## Consequences in HFpEF

| CaMKII effect | Cardiac consequence |
|---|---|
| ↑ SR Ca²⁺ leak (RyR2 phospho) | Elevated diastolic Ca²⁺ → impaired relaxation |
| Late Na⁺ current (INaL) activation | Ca²⁺ overload → afterdepolarisations (EADs, DADs) |
| Atrial EADs/DADs | Atrial fibrillation substrate |
| CaMKII-mediated MMP2 upregulation | ↑ collagen degradation/remodelling → ↑ passive LV stiffness + fibrosis |
| ACE2 reduction in women (sex-specific) | ↑ angiotensin II → pathological remodelling → sex-specific HFpEF development |

(source: [[wester2023sdb]])

## Link to Atrial Fibrillation

CaMKII-dependent atrial arrhythmogenesis:
- Late Na⁺ current (INaL) activation → Ca²⁺ overload → triggered afterdepolarisations
- Atrial EADs/DADs → re-entrant arrhythmia → atrial fibrillation
- SDB → CaMKII → AF may explain the strong epidemiological link between OSA and AF in HFpEF
- This pathway complements EAST-AFNET4 findings (source: [[rillig2021eastafnet4]]): treating AF may not address the upstream CaMKII-driven arrhythmia substrate

## Therapeutic Targeting

- **CaMKII inhibition:** Preclinically promising (KN-93, autocamtide-2-related inhibitory peptide); clinical translation limited by:
  - Specificity: CaMKII inhibition may affect normal cardiac function
  - Bioavailability: poor CNS/cardiac tissue penetration of current inhibitors
  - No completed clinical trial
- **Indirect reduction:**
  - SGLT2 inhibitors: reduce CaMKII activity in preclinical models (mechanism: ↓ mitochondrial ROS, ↓ INaL)
  - PAP therapy for OSA: reduces intermittent hypoxia → reduces oxidative CaMKII activation
  - GLP-1 RA: weight loss → reduced OSA severity → reduced CaMKII drive

[knowledge gap: no clinical data directly measuring CaMKII activity or its modification by treatments in human HFpEF]

## Related Concepts

- [[sleep-disordered-breathing]] — OSA is the primary driver of CaMKII overactivation in HFpEF
- [[diastolic-dysfunction]] — CaMKII impairs SR Ca²⁺ reuptake, slowing LV relaxation
- [[atrial-fibrillation]] — CaMKII-driven arrhythmogenesis creates AF substrate
- [[myocardial-fibrosis]] — CaMKII-MMP2 pathway contributes to fibrosis
- [[nitric-oxide-pathway]] — parallel pathway; both involve ROS-mediated cardiomyocyte dysfunction

## References
- Wester M, Arzt M, Sinha F, Maier LS, Lebek S. Insights into the Interaction of Heart Failure with Preserved Ejection Fraction and Sleep-Disordered Breathing. *Biomedicines.* 2023;11(11):3038. doi:[10.3390/biomedicines11113038](https://doi.org/10.3390/biomedicines11113038)
- Rillig A, Magnussen C, Ozga AK, Suling A, Brandes A, Breithardt G, Camm AJ, Crijns HJGM, Eckardt L, Elvan A, Goette A, Gulizia M, Haegeli L, Heidbuchel H, Kuck KH, Ng A, Szumowski L, van Gelder I, Wegscheider K, Kirchhof P. Early Rhythm Control Therapy in Patients With Atrial Fibrillation and Heart Failure. *Circulation.* 2021;144(11):845–858. doi:[10.1161/CIRCULATIONAHA.121.056323](https://doi.org/10.1161/CIRCULATIONAHA.121.056323)
