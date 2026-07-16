---
page-type: concept-page
title: Worsening Heart Failure (WHF)
summary: "Worsening heart failure (WHF) is a clinical-trial construct denoting an\
  \ episode of HF decompensation requiring treatment escalation; standard trial\
  \ definitions require hospitalisation with IV diuretics, but an expanded, hierarchical\
  \ definition (hospitalisation / urgent outpatient IV-or-oral-diuretic escalation\
  \ / nonurgent oral-diuretic-only escalation) increases event rates and trial power\
  \ without adding independent mortality-prediction value beyond the hospitalisation\
  \ tier; WHF status (recent, ongoing risk of, or as a trial endpoint) defines the\
  \ population or primary outcome of several major HFpEF trials."
tags:
  - hfpef
  - worsening-heart-failure
  - trial-design
  - endpoint-definition
  - prognosis
  - clinical-trials
created: 2026-07-15
last_updated: 2026-07-15
sources:
  - citekey: chaudhary2025worseninghf
    doi: 10.1016/j.jchf.2025.102571
---
# Worsening Heart Failure (WHF)

> An episode of heart failure decompensation requiring escalation of HF-directed therapy — used across clinical trials both as a population-enrollment criterion ("recent WHF") and as a primary/composite endpoint ("WHF event"); definitions range from hospitalisation-only to an expanded three-tier hierarchy that trades mortality specificity for statistical power.

## Aliases
| Alias | Type | Notes |
|---|---|---|
| WHF | abbreviation | worsening heart failure |
| WHF event | related-term | the countable unit in trial endpoints/composites |
| decompensation event | alternate-name | used interchangeably in some trial reports |
| post-WHF population | related-term | trial-enrollment framing (e.g. [[paraglide-hf]], [[soloist-whf]]) |

---

## Definition and Taxonomy

There is no single standardised clinical or research definition of WHF (source: chaudhary2025worseninghf). Historically, trials defined WHF narrowly as **hospitalisation for HF requiring intravenous (IV) diuretic therapy** — the definition underlying the Standardized Data Collection for Cardiovascular Trials Initiative and used in most pivotal HF outcome trials to date (source: chaudhary2025worseninghf).

Chaudhary et al. 2025 (post hoc analysis of [[reduce-lap-hf-ii]]) formalised an **expanded, hierarchical three-level WHF taxonomy**:

| Level | Definition | Setting |
|---|---|---|
| **Level 1** | Hospitalisation requiring IV diuretic agents | Inpatient — the conventional/"standard" WHF definition |
| **Level 2** | Urgent outpatient encounter (e.g. emergency department) treated with IV diuretic agents, or intensification of oral diuretic agents | Urgent outpatient |
| **Level 3** | Any other clinical encounter with ≥1 documented HF symptom + ≥2 objective findings of HF, plus any escalation of HF therapy (typically oral diuretic augmentation) | Nonurgent/routine visit |

Levels are applied hierarchically (a patient with a level 3 event who later has a level 1 event is classified level 1 for cumulative-incidence purposes), and three nested composite definitions can be constructed: **level 1 alone**, **level 1-or-2**, and **any WHF** (levels 1–3 combined). (source: chaudhary2025worseninghf)

## Clinical Relevance

**As an endpoint-broadening strategy:** Adding levels 2 and 3 to the classical level 1 (hospitalisation) definition substantially increases the total WHF event rate — in REDUCE LAP-HF II, incidence rose from 17.4% (level 1 alone) to 25.9% (any WHF) over 24 months (P=0.0003 for the difference). In the pre-specified low-PVR "responder" subgroup, this event-rate increase converted a nonsignificant device treatment effect (level 1 alone, P=0.103) into a statistically significant one (any WHF, rate ratio 0.56, 95% CI 0.33–0.96, P=0.009 for interaction) — i.e., **broadening the endpoint definition increased statistical power to detect a true treatment effect without needing a larger sample size.** Analogous strategies in DAPA-HF and [[deliver]] (adding outpatient oral-diuretic intensification to the primary composite) increased event counts by 36% and 54% respectively while preserving the treatment hazard ratio. (source: chaudhary2025worseninghf)

**As a prognostic marker — but only at the hospitalisation tier:** All-cause mortality at 24 months was strongly associated with WHF by any definition (HR 2.60, 95% CI 1.35–5.01 for "any WHF" vs. no WHF), but level 1 (hospitalisation) alone carried the strongest hazard (HR 3.54, 95% CI 1.83–6.87) — adding level 2/3 events did not sharpen, and slightly attenuated, mortality prediction, because the great majority of deaths occurred in patients who had experienced a level 1 event. **Non-hospitalisation WHF events add trial power but not independent mortality signal.** (source: chaudhary2025worseninghf)

**As a quality-of-life correlate:** WHF occurrence by any definition was associated with less improvement in KCCQ-Overall Summary Score at 24 months; broadening the definition to include level 2/3 events modestly strengthened this association relative to level 1 alone — WHF (including its nonurgent, outpatient forms) is not merely a hospitalisation proxy but a patient-experienced burden with quality-of-life consequences even when hospitalisation is avoided. (source: chaudhary2025worseninghf)

**As a population-selection criterion:** Several trials in this wiki enrol patients specifically because of a recent WHF event, on the premise that this identifies a higher-risk, treatment-responsive population and shortens time-to-event for trial efficiency:
- [[soloist-whf]] — enrolled patients with type 2 diabetes and "recently worsening heart failure," at or shortly after hospital discharge
- [[paraglide-hf]] — explicit inclusion criterion of a WHF event within 30 days (hospitalisation, ED visit, or ambulatory urgent visit requiring IV diuretics — corresponding to level 1/2 of the Chaudhary taxonomy, but not level 3)
- [[empulse]] — in-hospital initiation of SGLT2i during an acute WHF admission
- [[strong-hf]] — high-intensity GDMT uptitration initiated around an acute WHF admission

And as an endpoint-construction criterion:
- [[finearts-hf]] — primary endpoint is "total WHF events + CV death" (a total, first-plus-recurrent events composite structurally analogous to the framework Chaudhary et al. use methodologically)
- [[deliver]] and DAPA-HF ([[mcmurray2019dapahf]]) — both use "worsening HF (hospitalisation or urgent visit) or CV death" as the primary composite, with post hoc sensitivity analyses testing further expansion to outpatient oral-diuretic escalation

## History

- **Historically** (pre-2020 era trials, e.g. [[topcat]], [[paragon-hf]], [[i-preserve]]) — WHF/HF hospitalisation was defined narrowly and essentially always required inpatient admission with IV diuretic or IV vasoactive therapy; this remains the regulatory-grade "standard" definition (source: chaudhary2025worseninghf)
- **2016–2020** — MADIT-CRT and Ambrosy et al. observational analyses (cited in Chaudhary 2025) began documenting that outpatient WHF events (urgent visits with IV diuretics) carried mortality risk similar in magnitude to hospitalisation-defined events, and that a substantial minority (~27.6% in a 103,138-patient integrated health-system population) of all WHF events were nonurgent outpatient encounters — motivating broader endpoint definitions (source: chaudhary2025worseninghf)
- **2020–2023** — DAPA-HF and [[deliver]] (dapagliflozin) both formally tested expanded WHF/primary-composite definitions (adding outpatient oral-diuretic intensification) in exploratory analyses, finding preserved treatment effect with increased event counts; VICTORIA (Felker et al., cited in Chaudhary 2025) used independent CEC re-adjudication to identify "probable" WHF events not meeting the strict protocol definition, similarly preserving treatment effect estimates with improved precision (source: chaudhary2025worseninghf)
- **2025** — Chaudhary et al. formalise the three-tier (level 1/2/3) hierarchical WHF taxonomy in a post hoc analysis of [[reduce-lap-hf-ii]], explicitly quantifying the trade-off between statistical-power gain (from broadening the definition) and loss of mortality-prediction specificity (source: chaudhary2025worseninghf)

## Evidence

| Definition | 24-month incidence (any WHF event, MITT n=621) | Mortality HR vs. no WHF (95% CI) | Shunt treatment effect (responder subgroup, per-patient) |
|---|---|---|---|
| Level 1 alone | 17.4% (108/621) | 3.54 (1.83–6.87), P=0.0002 | P=0.103 (nonsignificant) |
| Level 1 or 2 | ~21–22% | 3.27 (1.70–6.29), P=0.0004 | P=0.046 |
| Any WHF (level 1–3) | 25.9% (161/621) | 2.60 (1.35–5.01), P=0.0042 | P=0.034 |

(source: chaudhary2025worseninghf)

Recurrent (total first-plus-recurrent) events analysis in the responder subgroup: rate ratio 0.56 (95% CI 0.33–0.96), P=0.009 for the treatment-by-responder interaction using the "any WHF" definition — statistically significant only once level 2/3 events were included. (source: chaudhary2025worseninghf)

## Open Questions

- Is level 3 (nonurgent, oral-diuretic-only escalation) a reproducible, standardisable definition across trial sites and health systems, or does its diagnosis depend too heavily on routine clinic visit frequency and access (a point the source paper itself raises as a limitation)?
- Would prospectively pre-specifying an expanded WHF definition (rather than applying it post hoc, as in this analysis) change trial sample-size calculations and time-to-completion in a way that materially accelerates HFpEF drug/device development?
- Does the mortality-attenuation pattern seen here (broader WHF definition → weaker per-event mortality hazard) generalise to pharmacological trials (DAPA-HF, DELIVER, FINEARTS-HF), or is it specific to the device/mechanical-unloading context of REDUCE LAP-HF II?
- How should trials that already enrol "post-WHF" populations (SOLOIST-WHF, PARAGLIDE-HF) define WHF at the eligibility stage to maximise both risk enrichment and generalisability — level 1 only, or level 1-2?
- Should quality-of-life impact (KCCQ) rather than mortality be the benchmark against which an expanded WHF definition is validated, given that level 2/3 events tracked with worse QoL even without added mortality signal?

## Related Pages
- Concepts: [[acute-hf]], [[hfpef-treatment-gap]], [[hf-phenotype-classification]]
- Entities: [[reduce-lap-hf-ii]], [[soloist-whf]], [[paraglide-hf]], [[finearts-hf]], [[deliver]], [[empulse]], [[strong-hf]], [[kansas-city-cardiomyopathy-questionnaire]]
- Sources: [[chaudhary2025worseninghf]], [[patel2024reducelaphf]], [[mentz2023paraglide]], [[solomon2022deliver]], [[solomon2024finearts]], [[mcmurray2019dapahf]]

## Contradictions
Broadening the WHF definition to include nonhospitalisation events increases statistical power to detect a treatment effect (device benefit reached significance in the responder subgroup only with the expanded definition) while simultaneously *diluting* the definition's mortality specificity (level 1 alone predicts mortality at least as strongly as the expanded composite). A positive trial result on a broadened WHF composite should not be read as implying a proportionate reduction in hospitalisation or death. See [[contradictions]] #37.

## References
- Chaudhary RS, Hussain SMD, Wang YS, Komtebedde J, Hasenfuß G, Borlaug BA, Kaye DM, Cleland JGF, Leon MB, Shah SJ, van Veldhuisen DJ, Solomon SD, Cikes M, Cutlip DE. Expanded Definition of Worsening Heart Failure: Impact on Clinical Outcomes and Quality-of-Life Assessment. *JACC Heart Fail.* 2025;13(9):102571. doi:[10.1016/j.jchf.2025.102571](https://doi.org/10.1016/j.jchf.2025.102571)
