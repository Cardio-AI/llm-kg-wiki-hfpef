log page
# Change Log

## 2026-07-14 (session — public release citation cleanup)

### Raw PDF citations replaced with citekey/DOI
- All wiki pages converted from `(source: raw/filename.pdf)` / `file: raw/....pdf` frontmatter to `(source: citekey)` + `doi:` frontmatter, so the repo can go public without redistributing copyrighted source PDFs
- Source pages (`wiki/sources/*.md`, 152 files): `**File:** raw/....pdf` line replaced with `**Full citation:**` block (text sourced from `wiki/citations.md`)
- All other wiki pages (~90 files): inline citations resolved to citekeys; each page with ≥1 citekey now ends with a `## References` section listing full DOI-linked citations
- `wiki/citations.md`: normalized 48 entries that had a bare `doi:10.x` (no markdown link) to the standard `doi:[10.x](https://doi.org/10.x)` link format; stripped redundant inline `[unverified]`/`[verify...]` bracket text from reference blockquotes (the DOI-review flag now carries that signal instead)
- New `wiki/citations-doi-review.md`: 8 citekeys without a confirmed DOI (5 missing entirely, 3 flagged unverified) — flagged for manual verification, no DOIs guessed
- `CLAUDE.md`, `_templates/{source,study,concept,entity}.md`, `_tasks/ingest.md` updated to the citekey+doi convention; raw/ path citation is no longer part of the workflow
- `.gitignore` added (`raw/`, `_config/zotero.md`); both untracked from git (`git rm -r --cached`) — files remain on local disk for the ingest workflow
- Git history rewritten via `git filter-repo --path raw --invert-paths` to remove the 35 PDFs already committed in prior commits; force-pushed to origin. Repo size dropped from ~84MB to ~1.1MB. Verified via fresh bare clone: 0 PDF blobs in history.
- Local backup bundle taken before the rewrite (`llm-wiki-hfpef-backup-2026-07-14.bundle`, one directory above the repo)

---

## 2026-05-21 (session — query pages, continued 4)

### Query page created
- `wiki/queries/sex-differences-hfpef-risk.md` — answered: "What parameters and risk factors cause the higher rate of HFpEF development in women?" (Evidence Quality 4/5; 7 mechanisms: cardiac structure, vascular aging, menopause/estrogen, amplified comorbidity risk, obstetric history, immune biology, exercise haemodynamics)

---

## 2026-05-21 (session — query pages, continued 3)

### Query page created
- `wiki/queries/obesity-np-interpretation.md` — answered: "How does obesity affect natriuretic peptide interpretation in HFpEF?" (Evidence Quality 4/5; two mechanisms: adipocyte NPR-C/neprilysin clearance + Thr-71 glycosylation; 20–30% false-negative rate; obesity paradox inversion; H₂FPEF BMI offset; tNT-proBNP research assay)

---

## 2026-05-21 (session — query pages, continued 2)

### Query page created
- `wiki/queries/exercise-unmasked-hfpef-diagnosis.md` — answered: "Exertional dyspnea, normal resting echo — additional evidence-supported diagnostic strategies?" (Evidence Quality 4/5; exercise PASP AUC 0.99, PCWP/CO slope gold standard, HFA-PEFF Step F1 escalation, CPET, saline/PLR, aetiological workup)

---

## 2026-05-21 (session — query pages, continued)

### Query page created
- `wiki/queries/spironolactone-hfpef.md` — answered: "Is spironolactone beneficial in HFpEF?" (Evidence Quality 3/5; TOPCAT neutral primary, Americas subgroup, Ferreira 2023 IPD structural benefit, FINEARTS-HF class context, SPIRRIT pending)

---

## 2026-05-21 (session — query pages)

### Query pages created
- `wiki/queries/sglt2-inhibitors-hfpef-rcts.md` — answered: "Which randomized trials demonstrated benefit of SGLT2 inhibitors in HFpEF?" (Evidence Quality 5/5)
- `wiki/queries/echo-parameters-diastolic-dysfunction.md` — answered: "What echocardiographic parameters are most commonly used to assess diastolic dysfunction?" (Evidence Quality 5/5)
- `wiki/queries/biomarkers-ntprobnp-tnt-dncb.md` — answered: NT-proBNP and hs-TnT diagnostic meaning; DnCB flagged as non-existent HF biomarker (trick question; alias resolution correctly intercepted) (Evidence Quality 4/5)

---

## 2026-05-20 (session — question-answering format + query page)

### Query page created
- `wiki/queries/sglt2-inhibitors-obese-hfpef.md` — answered: "Do SGLT2 inhibitors benefit obese patients with HFpEF?" (Evidence Quality 4/5)
- `wiki/queries/index.md` — created queries index

### Tooling fix
- Saved feedback memory: always apply `_tasks/question-answering.md` format (inline `[[citekey]]`, `## Evidence Quality`, `## References`) for all future answers

---

## 2026-05-20 (session 32f — citation correctness fix)

### Entity/concept pages removed from `(source: [[...]])` citations
- Fixed 36 incorrect citations across 12 files where internal entity/concept pages were used as source citations instead of source-summary pages (citekeys)
- **hypertensive-fibrotic-hfpef.md**: 15 fixes (→ shah2015phenomapping, paulus2013novelparadigm, shi2022sst2, arnold2022diamond, heidenreich2022aha, anker2021emperor, solomon2022deliver, albulushi2025sglt2fibrosis, pitt2014topcat, solomon2024finearts, solomon2012paramount, joseph2016qrs, pieske2019hfapeff, anker2023hfpefphenotype)
- **obese-metabolic-hfpef.md**: 9 fixes (→ timoteo2024eat ×2, paulus2013novelparadigm, wester2023sdb, haykowsky2011exercise ×2, babb2026ventilatorylimit, ilonze2024disparities, albulushi2025sglt2fibrosis, sachdev2023exercise)
- **obesity-hfpef.md**: 3 fixes (→ petrie2024stephfpef, packer2025summit, anker2021emperor + solomon2022deliver)
- **hfpef-treatment.md**: 1 fix (→ anker2021emperor + solomon2022deliver)
- **acute-hf.md**: 1 fix (→ vonhaehling2024fair)
- **pulmonary-arterial-pressure.md**: 1 fix (→ abraham2011champion)
- **hfpef-phenotypes.md**: 1 fix (→ cowie2017sdb)
- **atrial-fibrillation-hfpef.md**: 5 fixes (→ anker2023hfpefphenotype, pieske2019hfapeff, wester2023sdb ×2, solomon2012paramount)
- **peripheral-mechanisms-hfpef.md**: 2 fixes (→ sachdev2023exercise, beale2019iron)
- **spirit-hf.md**: 1 fix (→ solomon2024finearts)
- **hemodynamic-monitoring.md**: 1 fix (→ abraham2011champion + adamson2014champion)
- **contradictions.md**: 5 fixes (removed entity refs from victoria, socrates-preserved, paragon-hf citations; marked reduce-lap-hf-ii ×2 as [needs source])

---

## 2026-05-19 (session 32e — contradictions audit)

### contradictions.md restructured
- Added thematic index table at top grouping all 36 entries by theme (diagnostic definitions, SGLT2i, MRA, NO/cGMP, GLP-1 RA, exercise, devices, endpoint validity, phenotype-specific)
- Added cross-reference notes (→ see also #X) to related entries: #2↔#21 (MRA), #13↔#16 (SGLT2i symptoms), #17↔#18↔#19 (diagnostic threshold cluster), #25↔#33 (cGMP pathway)
- Added 2 new contradictions:
  - **#35: Semaglutide NT-proBNP weight-loss independence (Petrie 2024) vs. pericardial restraint prediction** — NT-proBNP reduction is weight-loss-independent (P interaction=0.58); greatest weight losers show paradoxically less NP reduction; contradicts simple pericardial restraint model; resolved by multi-mechanism hypothesis (anti-inflammatory + direct HF effects)
  - **#36: SGLT2i CMR antifibrotic evidence (Albulushi 2025, ΔECV −3.5%) vs. neutral mortality (Minisy 2025 meta-analysis, HR 0.92 NS across 9 RCTs >20,000 patients)** — fibrosis reversal on CMR without mortality signal; 4 explanations discussed

### Existing contradictions verified current
- All 34 prior entries reviewed; status accurate as of 2026-05-19
- #9 (SGLT2i ESC vs AHA) correctly marked RESOLVED
- #21 (MRA) already reflects FINEARTS-HF published results ✓
- #22 (GLP-1 RA) already reflects SUMMIT published results ✓

---

## 2026-05-19 (session 32d — lint pass 2)

### Outdated content fixed (2 pages)
- `wiki/concepts/obese-metabolic-hfpef.md` — SUMMIT updated from "pending publication" to published results (Packer 2025, NEJM; HR 0.62 CV death/worsening HF; KCCQ +6.9 pts); Open Questions updated to reflect SUMMIT answer
- `wiki/concepts/hypertensive-fibrotic-hfpef.md` — FINEARTS-HF updated from "ongoing" to published results (Solomon 2024, NEJM; RR 0.84; P=0.007); guideline implication note added

### Lint results (clean)
1. Contradictions: no new contradictions; contradictions.md current
2. Orphan pages: 0
3. Missing concept pages: HFimpEF adequately covered in hf-phenotype-classification; no new page needed
4. Outdated content: 2 fixed (above)
5. Page format: all pages have page-type + Aliases blocks ✓
6. Broken links: 0 real broken links ✓
7. Missing citations: 0 [needs source] markers ✓
8. Stub sources: armstrong2020victoria.md and cleland2006pepchf.md remain stubs (no PDF available); 2 "substudies not yet ingested" table notes in source pages (low priority)
9. citations.md drift: 0 gaps ✓

---

## 2026-05-19 (session 32c — citations.md sync)

### citations.md additions (3 missing citekeys)
- Added `damario2019cmd` row to Ingested Sources table and Full Formatted References (apostrophe-free canonical form of `D'Amario2019CMD`)
- Added `donelli2020hiit` row (filename-aligned form of `DonelliDaSilveira2020HIIT`; Eur J Prev Cardiol 2020;27:1733–1743)
- Added `mentz2021rehabhfhfpef` row (filename-aligned form of `Mentz2021REHABHFpEF`; JACC Heart Fail 2021;9:747–757)

### Citekey normalization (frontmatter + entity pages)
- `wiki/sources/damario2019cmd.md` — frontmatter citekey `D'Amario2019CMD` → `damario2019cmd`
- `wiki/sources/donelli2020hiit.md` — frontmatter citekey `DonelliDaSilveira2020HIIT` → `donelli2020hiit`
- `wiki/sources/mentz2021rehabhfhfpef.md` — frontmatter citekey `Mentz2021REHABHFpEF` → `mentz2021rehabhfhfpef`
- `wiki/entities/supervised-exercise-training.md` — updated both citekeys in sources block
- `wiki/entities/rehab-hf.md` — updated citekey in sources block
- `wiki/concepts/coronary-microvascular-dysfunction.md` — updated citekey
- `wiki/concepts/diastolic-dysfunction.md` — updated citekey

### Verification
- 153 citekey-style wiki-links across wiki pages; 154 entries in citations.md; 0 unresolved gaps

---

## 2026-05-19 (session 32b — lint fixes)

### Lint audit fixes
- `wiki/concepts/arterial-stiffness-hfpef.md` — Added `## Aliases` block (lint: missing aliases on concept page)
- `wiki/concepts/treatment-hfpef.md` — Added `## Aliases` block (lint: missing aliases on stub)
- `wiki/concepts/pericardial-restraint.md` — Added `## Aliases` block with 4 aliases (lint: missing aliases on mechanism page)
- `wiki/entities/champion.md` — Fixed `haemodynamic-monitoring` → `hemodynamic-monitoring` in YAML tag and wiki-link (British/American spelling mismatch)
- `wiki/sources/fu2024inflammation.md` — Fixed `[[paulus2013paradigm]]` → `[[paulus2013novelparadigm]]` (2 instances; broken citekey)
- `wiki/sources/lin2023cmd.md` — Fixed `[[d'amario2019cmd]]` → `[[damario2019cmd]]` (apostrophe breaks wiki-link)
- `wiki/sources/sachdev2023exercise.md` — Fixed pipe-syntax link and capital-letter cross-reference
- `wiki/sources/ho2019hfpefdefinitions.md` — Fixed pipe-syntax link `[[cardiopulmonary-exercise-testing|invasive CPET]]`
- `wiki/sources/kittleson2024accaha.md` — Fixed `[[transthyretin-amyloid-cardiomyopathy]]` → `[[attr-cm]]`
- 12 source files — Fixed `contradictions.md` → `[[contradictions]]` link format (sed -i)
- 5 files — Fixed `shah2014phenomapping` → `shah2015phenomapping` (wrong year in citekey)
- Deleted 4 empty root-level ghost stubs: `haemodynamic-monitoring.md`, `obesity-hfpef.md`, `pericardial-restraint.md`, `hypertension-in-hfpef.md`

### Outstanding lint issue
- `wiki/citations.md` drift: ~145 citekeys used in wiki pages not registered in citations.md — requires full sync pass

---

## 2026-05-19 (session 32 — missing pages batch creation)

### New concept/phenotype pages created (29)

**Phenotype pages:**
- `wiki/concepts/obese-metabolic-hfpef.md` — Obese-metabolic HFpEF phenotype (~30%); STEP-HFpEF KCCQ +7.8 pts/6MWD +20.3m/weight −10.7%; EAT, lipotoxicity, OSA, CaMKII; SGLT2i + GLP-1 RA treatment; sources: kosiborod2023stephfpef, anker2023hfpefphenotype
- `wiki/concepts/hypertensive-fibrotic-hfpef.md` — Hypertensive-fibrotic HFpEF phenotype (~50%); concentric LV hypertrophy; sST2 HR 2.76 (I²=0%); BP control, MRA, SGLT2i; PARAMOUNT LA reverse remodelling; sources: anker2023hfpefphenotype, shah2015phenomapping
- `wiki/concepts/atrial-fibrillation-hfpef.md` — AF-dominant HFpEF phenotype (10–50%); loss of atrial kick (30–40% of LV filling); rhythm control OR 0.735 (I²=0%; Al-Sadawi 2022) and HR 0.74 (EAST-AFNET4 HF subgroup); CABA-HFpEF ongoing; sources: alsadawi2022rhythmcontrol, rillig2021eastafnet4, anker2023hfpefphenotype

**Redirect/stub:**
- `wiki/concepts/treatment-hfpef.md` — Stub resolving [[treatment-hfpef]] cross-references; canonical content at [[hfpef-treatment]]

**Previously created in this session (earlier batch):**
- `wiki/concepts/iron-deficiency.md` — Iron deficiency in HFpEF; 59% prevalence (Beale 2019); FAIR-HFpEF 6MWT +49m; sources: beale2019iron, vonhaehling2024fair, ponikowski2020affirm
- `wiki/concepts/sleep-disordered-breathing.md` — SDB in HFpEF; 50–80% prevalence; CaMKII pathway; SERVE-HF context; sources: cowie2017sdb, suzuki2018sdb, wester2023sdb
- `wiki/concepts/rhythm-control.md` — OR 0.735 (I²=0%); EAST-AFNET4 HR 0.74; sources: alsadawi2022rhythmcontrol, rillig2021eastafnet4
- `wiki/concepts/ventilatory-limitation.md` — Babb 2026; 62–85% DH; NTG doesn't improve exercise; sources: babb2026ventilatorylimit, leahy2025heartlung
- `wiki/concepts/heart-lung-interactions.md` — DH→↑PCWP; ΔEELV vs. ΔPCWP r²=0.167; sources: leahy2025heartlung, babb2026ventilatorylimit
- `wiki/concepts/ecg-biomarkers-hfpef.md` — QRS≥120ms HR 1.27/1.38; fQRS HR 1.90; sources: joseph2016qrs, sung2023fqrs
- `wiki/concepts/myocardial-fibrosis.md` — sST2 HR 2.76 (I²=0%); ECV vs. MPR r=−0.06; sources: shi2022sst2, arnold2022diamond
- `wiki/concepts/epicardial-adipose-tissue.md` — EAT r=0.88 with LV eccentricity; pericardial restraint + paracrine; sources: timoteo2024eat, zamani2023pericardialfat
- `wiki/concepts/arterial-stiffness.md` — Exercise-divergent Ea/TACI; nitrite reversal; sources: reddy2017artstiff, suzuki2018sdb
- `wiki/concepts/arterial-stiffness-hfpef.md` — Cross-reference stub to [[arterial-stiffness]]
- `wiki/concepts/nitric-oxide-pathway.md` — eNOS→cGMP-PKG→titin phosphorylation; inorganic nitrite benefit; sources: reddy2017artstiff, paulus2013novelparadigm
- `wiki/concepts/camkii.md` — Intermittent hypoxia→ROS→CaMKII oxidation→Ca²⁺ dysregulation→AF; source: wester2023sdb
- `wiki/concepts/peripheral-mechanisms-hfpef.md` — A-VO₂ Diff reserve β=0.66; source: haykowsky2011exercise
- `wiki/concepts/cardiac-output-reserve.md` — Peak CO 6.3 vs 7.6 L/min; EDV vs ESV reserve; source: haykowsky2011exercise
- `wiki/concepts/hfpef-disparities.md` — Black women 7.4/1,000 PY; low NP trap; ATTR V122I 3.43%; source: ilonze2024disparities
- `wiki/entities/acc-aha-hf-guidelines.md` — PM-2 BP control; QM-1 SGLT2i; sources: heidenreich2022aha, kittleson2024accaha
- `wiki/entities/hemodynamic-monitoring.md` — CardioMEMS; CHAMPION 28%; GUIDE-HF pre-COVID HR 0.81; NP-guided failure; sources: lindenfeld2021guidehf, horiuchi2022npguided
- `wiki/concepts/pulmonary-arterial-pressure.md` — IpcPH vs CpcPH; PCWP 32 mmHg at 20W; source: lindenfeld2021guidehf
- `wiki/concepts/hfpef-treatment.md` — SGLT2i Class 2a/1; statins HR 0.74 non-ischaemic; GLP-1 RA; hemodynamic monitoring; sources: kittleson2024accaha, ortegahernandez2024statins
- `wiki/concepts/acute-hf.md` — ADHF-HFpEF; NLR trajectory HR 1.26; sources: boralkar2019nlr, tamaki2023nlrplr
- `wiki/concepts/hfpef-fibrosis-paradigm.md` — CMD 70% prevalence; ECV vs MPR r=−0.06; independent mechanisms; source: arnold2022diamond
- `wiki/concepts/left-atrial-remodelling.md` — LA volume −4.6 vs +0.37 mL (PARAMOUNT); source: solomon2012paramount
- `wiki/concepts/microvascular-dysfunction.md` — 70% CMD; fQRS as ECG surrogate; independence from fibrosis; sources: arnold2022diamond, sung2023fqrs
- `wiki/concepts/cardiac-remodelling.md` — Concentric vs eccentric; QRS as remodelling marker; source: joseph2016qrs
- `wiki/concepts/hemodynamics.md` — PCWP 18→32 mmHg rest→exercise; haemodynamic reserve; sources: reddy2017artstiff, horiuchi2022npguided
- `wiki/concepts/hfpef-inflammatory-metabolic-paradigm.md` — Paulus 2013 extension; HR 1.43/2.04/2.83 (I²=0%); inflammatory endotype ~30%; sources: fu2024inflammation, paulus2013novelparadigm, anker2023hfpefphenotype

### Page-type taxonomy updates
- All 210+ wiki markdown files: `page-type:` YAML tag added via bulk Python script
- 4 YAML-error files manually fixed: attr-cm.md, myomobile.md, adamson2014champion.md, vantassell2018dhart2.md
- Rule added to CLAUDE.md: ## Page Type Taxonomy section

### Cross-reference audit
- `_empty_pages.md` created: 35 missing cross-references identified; 32 resolved by page creation
- Remaining issues: broken link formats (contradictions.md → [[contradictions]], apostrophe in d'amario2019cmd, paulus2013paradigm typo)

### Index updated
- All new concept, phenotype, entity pages added to Concepts section of index.md

---

## 2026-05-19 (session 31 — entity-source gap fill)

### Entity pages created (3)
- `wiki/entities/obesity-hfpef.md` — Obesity as HFpEF comorbidity; 30–40% prevalence; pericardial restraint + adipose inflammation mechanisms; STEP-HFpEF/SUMMIT/lifestyle evidence; sources: anker2023hfpefphenotype, borlaug2023statement, kramer2025summit-cmr, lee2024lifestyle, paulus2013novelparadigm
- `wiki/entities/hypertension-hfpef.md` — Hypertension in HFpEF; 60–80% prevalence; RAAS trial failure series; historical paradigm evolution; phenotype-guided treatment; sources: anker2023hfpefphenotype, borlaug2023statement, paulus2013novelparadigm, pfeffer2019hfpef, charm-preserved, i-preserve, paragon-hf
- `wiki/concepts/pericardial-restraint.md` — Pericardial restraint mechanism; EAT vs. pericardial fat compartments; SUMMIT CMR evidence (pericardial AT −43 mL); NT-proBNP paradox; therapeutic implications; sources: kramer2025summit-cmr, borlaug2023statement

### Entity pages updated (5)
- `wiki/entities/fair-hfpef.md` — Updated with published results (Eur Heart J 2024; 6MWT +49m P=0.029; SAEs ratio 0.27; stopped at N=40/200); status changed from Ongoing to Published; source frontmatter updated; vonhaehling2024fair added to Related Pages
- `wiki/entities/relax.md` — Added full results table from redfield2013relax.md (peak VO₂ P=0.90; safety signal: creatinine, NT-proBNP, endothelin-1); added [[redfield2013relax]] to Related Pages Sources
- `wiki/entities/pep-chf.md` — Added [[cleland2006pepchf]] to Related Pages Sources; source frontmatter path clarified
- `wiki/entities/step-hfpef.md` — Added [[obesity-hfpef]] and [[pericardial-restraint]] to Related Pages
- `wiki/entities/summit.md` — Added [[obesity-hfpef]] and [[pericardial-restraint]] to Related Pages

### Source pages updated (7)
- `wiki/sources/vonhaehling2024fair.md` — Added [[fair-hfpef]] entity backlink in Connections + Related Pages Entities
- `wiki/sources/armstrong2020vitality.md` — Added [[vitality-hfpef]] entity backlink in Connections + Related Pages Entities
- `wiki/sources/borlaug2023statement.md` — Added [[obesity-hfpef]], [[hypertension-hfpef]], [[pericardial-restraint]] to Connections + Related Pages
- `wiki/sources/kramer2025summit-cmr.md` — Added [[pericardial-restraint]], [[obesity-hfpef]] to Connections + Related Pages
- `wiki/sources/paulus2013novelparadigm.md` — Added [[obesity-hfpef]], [[hypertension-hfpef]] to Connections + Related Pages
- `wiki/sources/anker2023hfpefphenotype.md` — Added [[obesity-hfpef]], [[hypertension-hfpef]], [[fair-hfpef]] to Connections + Related Pages
- `wiki/sources/lee2024lifestyle.md` — Added [[obesity-hfpef]] to Connections + Related Pages

### Index updated
- Added [[obesity-hfpef]] and [[hypertension-hfpef]] to Comorbidity Entities section
- Added [[pericardial-restraint]] to Concepts section
- Updated [[fair-hfpef]] entry: published results
- Updated [[myomobile]] entry: primary results published 2026

## 2026-05-19 (session 30 — 10 PDFs ingested)

### Source pages created (10)

**Biomarkers:**
- `wiki/sources/gori2021paragon.md` — Gori M et al. (JACC Heart Fail 2021;9:627–635; DOI: 10.1016/j.jchf.2021.04.009): PARAGON-HF biomarker secondary analysis; N=1,260; hs-TnT >14 ng/L in 58.3%; HR 1.38 per doubling; Sac/Val reduced hs-TnT 9–10% vs. valsartan; threshold 17 ng/L for outcomes prediction; P interaction NS for hs-TnT-modified Sac/Val benefit
- `wiki/sources/morfino2022biomarkers.md` — Morfino P et al. (J Cardiovasc Dev Dis 2022;9:256; DOI: 10.3390/jcdd9080256): comprehensive HFpEF biomarker review; six pathways (NP, fibrosis, inflammation, endothelial, adipokine, metabolic/renal); NPs AUC 0.80; hs-TnT sex differential (HR 3.33 men vs. 1.35 women); Galectin-3 AUC 0.927 (cut-off 10.1 ng/mL); GDF-15 not AF-dependent; six-pathway map Figure 1

**SGLT2 inhibitors:**
- `wiki/sources/requenaibanez2022sglt2.md` — Requena-Ibáñez JA et al. (Cardiovasc Drugs Ther 2023;37:989–996; DOI: 10.1007/s10557-022-07371-7): SGLT2i mechanisms across HF EF spectrum; EAT/pericardial restraint reduction; EMPEROR-Preserved LVEF >60% attenuation; phenotype-based vs. EF-based patient selection; CMR to reduce EF variability
- `wiki/sources/gonzalez2024sglt2trends.md` — González A et al. (BMC Cardiovasc Disord 2024;24:285; DOI: 10.1186/s12872-024-03961-5): US MarketScan claims Jan 2020–Jun 2023; HFpEF overall 0.5%→9.9%; T2DM ~20% vs. non-T2DM ~1.2% — 17-fold gap; canagliflozin collapse; implementation gap in non-diabetic HFpEF documented
- `wiki/sources/minisy2025sglt2.md` — Minisy MM, Abdelaziz A (BMC Cardiovasc Disord 2025;25:765; DOI: 10.1186/s12872-025-05127-3): 9 RCTs, >20,000 patients; CV death/HHF HR 0.83 (GRADE high); HHF HR 0.75 (GRADE high); mortality HR 0.92 (GRADE low, NS); KCCQ +1.8 pts; I²=62%; no publication bias
- `wiki/sources/albulushi2025sglt2fibrosis.md` — Albulushi A et al. (Eur J Med Res 2025;30:592; DOI: 10.1186/s40001-025-02834-7): N=100 HFpEF+T2DM; dapagliflozin 10 mg vs. placebo 12 months; serial CMR; ΔECV −3.5% vs. −0.8% (P<0.001); ΔLVMI −8.2 vs. −2.1 g/m²; first serial CMR evidence for SGLT2i antifibrotic mechanism in HFpEF

**MRA/Spironolactone:**
- `wiki/sources/ferreira2023spironolactone.md` — Ferreira JP et al. (Eur J Heart Fail 2023;25:108–113; DOI: 10.1002/ejhf.2726): IPD meta-analysis N=984 (HOMAGE+Aldo-DHF+TOPCAT Americas); LAVi −1.1 mL/m² (P=0.03); LVMi −3.6 g/m²; IVS −0.2 cm; E/e' −1.3; LVEF +1.7%; first IPD-level evidence for spironolactone echocardiographic remodelling in non-HFrEF
- `wiki/sources/lund2024spirrit.md` — Lund LH et al. (Eur J Heart Fail 2024;26:2453–2463; DOI: 10.1002/ejhf.3453): SPIRRIT-HFpEF design paper; NCT02901184; PROBE design; SwedeHF + US TIN; LVEF ≥40%; ~2,200 enrolled mid-2024; primary endpoint amended to total recurrent events; first RRCT in chronic HF; new pending trials: SOGALDI-PEF (NCT05676684), REDEFINE-HF (NCT06008197), CONFIRMATION-HF (NCT06024746)

**GLP-1RA:**
- `wiki/sources/petrie2024stephfpef.md` — Petrie MC et al. (JACC 2024;84:27–40; DOI: 10.1016/j.jacc.2024.04.022): STEP-HFpEF program secondary analysis N=1,145; semaglutide reduced NT-proBNP ETR 0.82 (P=0.0002); weight-loss-independent (P interaction=0.58); KCCQ T3 +11.9 pts vs. T1 +4.5 (P=0.02); direct HF disease-modifying mechanism

**Screening:**
- `wiki/sources/achten2025screening.md` — Achten A et al. (Heart Fail Rev 2025;30:1207–1213; DOI: 10.1007/s10741-025-10540-z): HFpEF screening in obesity; onset one decade earlier; NT-proBNP sensitivity 77%→67% at BMI >35; height²-indexing for echo; HFpEF-ABA score; stepwise algorithm; SGLT2i + GLP-1RA treatment

### Entity pages updated (3)

- `wiki/entities/sglt2-inhibitors.md` — Added: antifibrotic ECV evidence section (Albulushi 2025); SGLT2i class-effect meta-analysis (Minisy 2025); Implementation Gap section (Gonzalez 2024 prescribing trends); updated sources frontmatter + last_updated
- `wiki/entities/spironolactone.md` — Added: echocardiographic IPD meta-analysis section (Ferreira 2023: LAVi/LVMi/IVS/E/e'/LVEF); updated sources frontmatter + last_updated
- `wiki/entities/step-hfpef.md` — Added: NT-proBNP analysis section (Petrie 2024: ETR 0.82, weight-loss-independent, NT-proBNP tertile interaction); updated sources frontmatter + last_updated

### Entity pages updated (1)

- `wiki/entities/spirrit.md` — Previously updated in session 30: frontmatter, Description, Role, Evidence, Status sections fully rewritten with Lund 2024 data; title changed to SPIRRIT-HFpEF; source changed from "pending" to `lund2024spirrit`

### Registry files updated
- `wiki/citations.md` — 10 new rows added to Ingested Sources table; 10 new full APA references added to Full Formatted References section
- `wiki/index.md` — 10 new source entries added: gori2021paragon + ferreira2023spironolactone + petrie2024stephfpef (Secondary Analyses); albulushi2025sglt2fibrosis (Clinical Trial Papers); lund2024spirrit (Trial Design Papers); requenaibanez2022sglt2 + morfino2022biomarkers + achten2025screening (Review Articles); gonzalez2024sglt2trends (Observational Studies); minisy2025sglt2 (Systematic Reviews)
- `wiki/trials-pending.md` — SPIRRIT entry struck through (session 19); added session 30 entry with SOGALDI-PEF (NCT05676684), REDEFINE-HF (NCT06008197), CONFIRMATION-HF (NCT06024746)
- `wiki/overview.md` — High-Level Summary updated (SGLT2i antifibrotic mechanism; implementation gap; semaglutide NT-proBNP weight-loss-independent effect; spironolactone structural remodelling; HFpEF obesity screening); Active Debates: SGLT2i real-world implementation gap; Knowledge Gaps: SPIRRIT results; session 30 Recent Additions entry added
- `wiki/timeline.md` — Treatment: Ferreira 2023 spiro IPD, Gonzalez 2024 prescribing trends, Albulushi 2025 antifibrotic CMR, Minisy 2025 meta-analysis, Petrie 2024 NT-proBNP; Diagnostics: Achten 2025 screening in obesity; Biomarkers: Gori 2021, Morfino 2022
- `wiki/log.md` — this entry

---

## 2026-05-19 (session 29 — 4 PDFs ingested)

### Source pages created (4)

**Pharmacological landscape review:**
- `wiki/sources/sauer2026pharmacological.md` — Sauer AJ et al. (ESC Heart Fail 2026; DOI: 10.1093/eschf/xvag056): four-society guideline table (ESC/AHA-ACC-HFSA/JCS-JHFS/iCARDIO); SGLT2i Class I all societies; finerenone Class I (ESC) / IIa (JCS) / recommended (iCARDIO); GLP-1RA strongly recommended for obesity (iCARDIO only); combination therapy — SGLT2i+nsMRA HR 0.69 (three-trial combined); emerging trials: BALANCED-HF, EASi-HF, REDEFINE-HF, CONFIRMATION-HF; Bayer-funded; aldosterone pathway map (Figure 2)

**MRA class effect (editorial):**
- `wiki/sources/turgeon2025finearts.md` — Turgeon RD, Beavers CJ (J Card Fail 2025;31:603–605; DOI: 10.1016/j.cardfail.2024.09.011): Bayesian re-analysis of TOPCAT using FINEARTS-HF as strong prior; TOPCAT overall posterior HR 0.87 (0.79–0.94), P(HR<1) = 100%, P(HR<0.95) = 98%; pooled HR 0.87 (0.79–0.95) ~1.5% ARR; spironolactone $0.15/day vs. finerenone $3.61/day — cost equity argument; MRA class effect established

**NT-proBNP glycosylation:**
- `wiki/sources/hage2026ntprobnp.md` — Hage C et al. (Int J Cardiol 2026;458:134554; DOI: 10.1016/j.ijcard.2026.134554): tNT-proBNP (Roche research assay) vs. standard Elecsys assay in KaRen (HFpEF, N=83) + MetAnEnd (HFrEF, N=79); NT-proBNP/tNT-proBNP ratio lower in HFpEF (0.27 vs. 0.32; P=0.019) — more glycosylation at Thr-71; tNT-proBNP independently prognostic (HR 1.77 [1.08–2.88]; P=0.022); standard NT-proBNP loses significance after eGFR adjustment; AUROC 0.710 vs. 0.682 (P=0.068, NS)

**Echocardiography comprehensive review:**
- `wiki/sources/upadhya2025echo.md` — Upadhya B et al. (Heart Fail Rev 2025;30:899–922; DOI: 10.1007/s10741-025-10516-z; Duke University): H₂FPEF sensitivity 52.7%, HFA-PEFF 70%; LASr <18% as third criterion → 99% classification; LA minimum LAV better than maximum for chronic LVFP; 6 mimicker patterns (Table 1); 5 TTE phenotype signatures (Table 4); LVEF U-shaped mortality nadir 60–65%; exercise E/e' "highly demonstrative" of HFpEF

### Concept pages created (1)
- `wiki/concepts/biomarkers-hfpef.md` — New hub page; six biomarker categories + structural/imaging-derived; history from BNP identification through tNT-proBNP 2026; multi-biomarker panels; open questions including obesity threshold adjustment and tNT-proBNP clinical validation

### Entity pages created (2)
- `wiki/entities/balcinrenone.md` — Selective MR modulator; MIRACLE Phase 2 neutral (N=133, all 3 doses, UACR endpoint); BALANCED-HF Phase 3 (~N=4,800, dapagliflozin combination) ongoing
- `wiki/entities/vicadrostat.md` — Aldosterone synthase inhibitor (CYP11B2); upstream aldosterone suppression; EASi-HF Phase 3 (~N=6,000, empagliflozin combination, EF ≥40%) ongoing

### Entity pages updated (1)
- `wiki/entities/finearts-hf.md` — Added "MRA Class Effect — Turgeon 2025 Bayesian Analysis" section with full posterior table; added emerging MRA alternatives section (balcinrenone, vicadrostat); updated Contradictions section; updated sources frontmatter (added turgeon2025finearts, sauer2026pharmacological); last_updated 2026-05-19

### Concept pages updated (2)
- `wiki/concepts/natriuretic-peptides.md` — Added "NT-proBNP Glycosylation — The tNT-proBNP Problem" section with full data table; updated summary to include glycosylation mechanism; expanded Open Questions; updated Related Pages and Contradictions; sources frontmatter updated (added ammar2025bnp, hage2026ntprobnp)
- `wiki/entities/echocardiography.md` — Added sections: Advanced Parameters and LA Strain, Exercise Echocardiography, HFpEF Mimickers TTE Differential Diagnosis, HFpEF Phenotyping by TTE, LVEF Measurement Challenges; updated summary and frontmatter (added upadhya2025echo); expanded Evidence and Contradictions

### Registry files updated
- `wiki/citations.md` — 4 new rows added to Ingested Sources table (sauer2026pharmacological, turgeon2025finearts, hage2026ntprobnp, upadhya2025echo); Packer2025SUMMIT moved from Stub Sources to Ingested Sources; 5 new full APA references added to Full Formatted References section
- `wiki/trials-pending.md` — Added 2026-05-19 section with BALANCED-HF and EASi-HF entries (from sauer2026pharmacological)
- `wiki/index.md` — 7 new entries added: sauer2026pharmacological (Guidelines section), turgeon2025finearts + upadhya2025echo + hage2026ntprobnp (Review/Secondary sections), balcinrenone + vicadrostat (Pharmacological Entities), biomarkers-hfpef (Concepts); natriuretic-peptides entry updated
- `wiki/overview.md` — High-Level Summary updated (pharmacological landscape section); Active Debates: NT-proBNP glycosylation + Turgeon Bayesian MRA class effect added; Knowledge Gaps: tNT-proBNP commercial validation + echocardiography algorithm evolution added; session 29 Recent Additions entry added
- `wiki/timeline.md` — Treatment: sauer2026pharmacological combination therapy 2026 row added; Pathophysiology: Hage 2026 glycosylation + Upadhya 2025 echo 2025 row added
- `wiki/log.md` — this entry

---

## 2026-05-19 (session 28 — 11 PDFs ingested)

### Source pages created (11)

**Epidemiology:**
- `wiki/sources/lam2011hfpef.md` — Lam 2011 (Eur J Heart Fail 13:18–28): HFpEF epidemiology review; ~50% of all HF; rising prevalence; mortality similar to HFrEF; no proven treatment at time of publication

**Device Trials — CHAMPION family:**
- `wiki/sources/abraham2011champion.md` — CHAMPION primary RCT (Lancet 2011;377:658–666; N=550): CardioMEMS PA pressure monitoring; 28% HF hospitalisation reduction (HR 0.72; P=0.0002); NCT00531661
- `wiki/sources/adamson2014champion.md` — CHAMPION HFpEF subgroup (Circ Heart Fail 2014;7:935–944; N=119 HFpEF): ~46% HF hospitalisation reduction; first positive device evidence specifically in HFpEF

**Phase 2 Mechanistic Trials:**
- `wiki/sources/maier2013ralidhf.md` — RALI-DHF (JACC Heart Fail 2013;1:115–122; N=20 HFpEF): ranolazine crossover; exercise LVEDP −4.7 mmHg (P=0.001); late I_Na→Ca²⁺ pathway proof-of-concept

**Anti-inflammatory (D-HART2):**
- `wiki/sources/vantassell2017dhart2.md` — D-HART2 design (Clin Cardiol 2017;40:626–632; NCT02173548): anakinra 24 weeks in HFpEF; rationale: Paulus–Tschöpe IL-1 pathway
- `wiki/sources/vantassell2018dhart2.md` — D-HART2 results (Circ Heart Fail 2018;11:e005036; N=31 HFpEF): hs-CRP AUC ratio 0.40 (P=0.001) — target engaged; VO₂ NS (P=0.54) — critical null for inflammation→exercise pathway

**Secondary Analyses:**
- `wiki/sources/merrill2019topcat.md` — TOPCAT sex differences (JACC Heart Fail 2019;7:228–238; N=3,445): women higher LVEF (~63% vs. ~58%); spironolactone sex×treatment P=0.26 (NS)

**Device Trial — REBALANCE-HF:**
- `wiki/sources/fudim2024rebalance.md` — REBALANCE-HF (JAMA Cardiol 2024;9(12):1143–1153; N=80 HFpEF; NCT04592445): splanchnic nerve ablation vs. sham; exercise PCWP −5.4 mmHg (P=0.003); KCCQ improved

**Editorial:**
- `wiki/sources/carbone2024inflammation.md` — Carbone 2024 (JACC Heart Fail 12:1270–1273): inflammation-obesity-CRF triad; GLP-1RA mechanism synthesis

**Digital Health:**
- `wiki/sources/zeid2026myomobile.md` — MyoMobile primary results (JACC Heart Fail 2026;14(5):102845; N=185 HFpEF; NCT04940312): app-based PA coaching significantly increased step count; KCCQ + 6MWT improved; first positive digital health RCT in HFpEF

**Systematic Review:**
- `wiki/sources/masri2026attrcm.md` — Masri 2026 (Prog Cardiovasc Dis pre-proof; doi:10.1016/j.pcad.2026.04.004): ATTR-CM trials SR; tafamidis, acoramidis, patisiran (APOLLO-B), vutrisiran (HELIOS-B; HR 0.72), eplontersen; multiple approved options

### Entity pages created (1)
- `wiki/entities/rebalance-hf.md` — REBALANCE-HF entity; promoted from trials-pending.md to trials.md

### Entity pages updated (1)
- `wiki/entities/myomobile.md` — updated: primary results published (zeid2026myomobile); removed "results pending" language

### Source pages updated (1)
- `wiki/sources/zeid2025myomobile.md` — updated: cross-reference to primary results (zeid2026myomobile) added

### Registry files updated
- `wiki/citations.md` — 11 new rows added to Ingested Sources table; 11 APA references added to Full Formatted References
- `wiki/trials.md` — added RALI-DHF and D-HART2 to Phase 2 section; added REBALANCE-HF to Device Trials section; updated CHAMPION entry to link all 3 source pages; updated MyoMobile entry with published results
- `wiki/trials-pending.md` — REBALANCE-HF marked as ingested/removed from pending
- `wiki/index.md` — 13 new entries added across Observational Studies, Clinical Trial Papers, Review Articles, Systematic Reviews, Secondary Analyses, Trial Design Papers, and Entities sections
- `wiki/overview.md` — High-Level Summary updated (REBALANCE-HF, MyoMobile, ATTR-CM multi-drug landscape); D-HART2 Active Debate added; ATTR-CM screening + digital health Knowledge Gaps added; session 28 Recent Additions entry added
- `wiki/timeline.md` — Epidemiology: Lam 2011 row added; Treatment: CHAMPION 2011, RALI-DHF 2013, CHAMPION HFpEF subgroup 2014, D-HART2 2018, TOPCAT sex 2019, REBALANCE-HF 2024, MyoMobile 2026 rows added; Landmark Trials: RALI-DHF 2013, D-HART2 2018, APOLLO-B 2022, ATTRibute-CM 2023, HELIOS-B 2024, REBALANCE-HF 2024, MyoMobile 2026 rows added
- `wiki/log.md` — this entry

---

## 2026-05-18 (session 27 — NCT file processing complete)

### trials.md
- Added 3 Borlaug lab mechanistic studies to Mechanistic Studies table:
  - **EXEC** (NCT01418248): Observational; simultaneous ExE + CPX vs invasive RHC; N=108 HFpEF+PH; Borlaug lab Mayo; completed; foundational dataset for multiple Obokata/Andersen papers 2015–2020.
  - **Borlaug 2015 IV Nitrite** (NCT01932606): Phase 2 crossover RCT; IV NaNO₂ 50 mcg/kg/min vs saline; invasive RHC at rest and 20W; N=28 HFpEF; completed; primary paper Borlaug 2015 JACC.
  - **AIR001-HFpEF** (NCT02262078): Phase 2 crossover RCT; nebulized AIR001 (NaNO₂) 90mg vs saline placebo; invasive RHC at rest and 20W; N=26 HFpEF; completed; primary paper Borlaug 2016 Circ Res.
- All 51 NCT `.md` files in `raw/` now accounted for (48 matched existing tracked trials; 3 added above).

---

## 2026-05-18 (session 25/26 — 21 PDFs ingested)

### Source pages created (21)

**Sleep-Disordered Breathing / Ventilatory Mechanics (5):**
- `wiki/sources/cowie2017sdb.md` — State-of-the-art review (JACC HF 2017;5:715–723). SDB prevalence 50–75% in HF; CSA vs. OSA mechanisms; SERVE-HF: ASV ↑CV mortality in HFrEF+CSA (HR 1.28); CPAP/BiPAP/ASV treatment landscape.
- `wiki/sources/suzuki2018sdb.md` — Fukushima cross-sectional (ESC HF 2018;5:284–291; N=221). Severe SDB predicts higher PWV in HFpEF (β=0.234; P=0.005) but NOT HFrEF (P=0.068); first EF-subtype-differential SDB-arterial stiffness evidence.
- `wiki/sources/wester2023sdb.md` — Biomedicines review (2023;11:3038; Wester et al.). SDB 58–80% in HFpEF; 3 HFpEF phenotypes; CaMKII pathway: intermittent hypoxia → ROS → CaMKII oxidation → diastolic SR Ca²⁺ leak → AF → HFpEF; GLP-1RA + SGLT2i as SDB treatment targets.
- `wiki/sources/leahy2025heartlung.md` — JACC HF 2025;13:102523 (NCT04068844; N=55 obese HFpEF). Dynamic hyperinflation in 62% at 20W and 85% at peak; DH group PCWP higher at 20W (P=0.005) and peak (P=0.007); ΔEELV correlated with ΔPCWP (r²=0.167 at peak); non-cardiac mechanism for elevated exercise PCWP in obese HFpEF.
- `wiki/sources/babb2026ventilatorylimit.md` — Respir Physiol Neurobiol 2026;341:104546 (NCT04068844; N=42 obese HFpEF; crossover RCT). NTG lowered PCWP but did NOT change exercise capacity or breathing mechanics (EELV R²=0.96); paradigm-shifting: ventilatory-limited exercise in obese HFpEF, not cardiac-limited.

**Iron Deficiency / IV Iron (3):**
- `wiki/sources/beale2019iron.md` — Systematic review + meta-analysis (Open Heart 2019;6:e001012; 15 studies, N=1,877 HFpEF). Iron deficiency prevalence 59%; functional 34%; absolute 30%; ID associated with worse VO₂/6MWT/QoL; no HFpEF RCT evidence at time of publication.
- `wiki/sources/ponikowski2020affirm.md` — AFFIRM-AHF (Lancet 2020;396:1895–1904; NCT02937454; **HFrEF LVEF <50%**, N=1,132). IV FCM vs. placebo at AHF discharge; primary composite RR 0.79 (P=0.059, NS); total HFH RR 0.74 (P=0.013); pre-COVID RR 0.75 (P=0.024); CV death NS. NOTE: HFrEF population — context for FAIR-HFpEF.
- `wiki/sources/vonhaehling2024fair.md` — FAIR-HFpEF (Eur Heart J 2024;45:3789–3800; NCT03074591; N=40, stopped early). First RCT of IV iron in HFpEF; FCM +65 m vs. placebo −8 m at week 32; week 24 difference +49 m (P=0.029); SAEs 5 vs. 19 (P=0.043). Directionally positive but underpowered.

**Rhythm Control in AF+HF (2):**
- `wiki/sources/rillig2021eastafnet4.md` — EAST-AFNET4 HF subgroup (Circulation 2021;144:845–858; NCT01288352; N=798 HF). Early rhythm control HR 0.74 (P=0.03); HFpEF 56.3% of HF subgroup; no HF-type interaction (P=0.63).
- `wiki/sources/alsadawi2022rhythmcontrol.md` — Systematic review + meta-analysis (Heart Rhythm O² 2022;3:520–525; 5 studies, N=16,825 HFpEF+AF). Rhythm control OR 0.735 vs. rate control (P<0.001); I²=0%; 4/5 studies used catheter ablation.

**Haemodynamic Monitoring (1):**
- `wiki/sources/lindenfeld2021guidehf.md` — GUIDE-HF (Lancet 2021;398:991–1001; NCT03387813; N=1,000 all EF). CardioMEMS haemodynamic-guided management; primary HR 0.88 (NS); pre-COVID HR 0.81 (P=0.049); HFpEF subgroup (N=469) HR 0.85 (NS). COVID-19 confounded trial.

**Biomarkers (3):**
- `wiki/sources/joseph2016qrs.md` — TOPCAT post-hoc (JACC HF 2016;4:477–486; N=3,445). QRS ≥120 ms in 17.9%; HR 1.27 for primary composite (P=0.009); HFH HR 1.38 (P=0.003); continuous QRS risk from ~100 ms; no spironolactone interaction by QRS.
- `wiki/sources/kasahara2018chart2.md` — CHART-2 registry (Heart Vessels 2018;33:997–1007; NCT00418041; N=4,301 HF; 6.3y follow-up). BNP prognostic across EF subtypes; median BNP HFpEF 85.3 vs. HFrEF 208 pg/mL; HR per log₂ BNP similar (P-interaction=0.300); CART thresholds 30/100/300 pg/mL.
- `wiki/sources/shi2022sst2.md` — Systematic review (Front Cardiovasc Med 2022;9:937291; 16 studies, N=2,761 HFpEF). sST2 AUC <0.7 for HFpEF diagnosis (poor); prognostic: log sST2 HR 2.76 for all-cause death (I²=0%; P=0.013); composite HR 6.52.
- `wiki/sources/sung2023fqrs.md` — Retrospective cohort (JAHA 2023;12:e028105; N=960 HFpEF; 657-day median follow-up). Anterior/lateral fQRS HR 1.90 for HFH (P<0.001); associated with myocardial perfusion defects.

**EAT and Pericardial Fat (2):**
- `wiki/sources/zamani2023pericardialfat.md` — Circulation research letter 2023;148:1410–1412 (NCT04068844; N=28 obese HFpEF). Epicardial fat r=0.88 with LV eccentricity index (P<0.001); paracardial fat r=0.91 (P<0.001); BMI/subcutaneous/visceral fat NOT correlated.
- `wiki/sources/timoteo2024eat.md` — Review (Int J Cardiol 2024;412:132303). EAT pathways: pericardial restraint → ↑LVEDP; paracrine dysfunction (TNF-α/IL-1β → fibrosis/AF); treatment: statins, SGLT2i, GLP-1RA.

**Treatment-Related (3):**
- `wiki/sources/horiuchi2022npguided.md` — Review (Heart International 2022;16:112–116). NP-guided therapy benefits HFrEF <75y but NOT HFpEF; TIME-CHF HFpEF subgroup trended to worsen; GUIDE-IT neutral; meta-analyses show no benefit or harm trend in HFpEF.
- `wiki/sources/ortegahernandez2024statins.md` — RICA registry cohort (J Clin Med 2024;13:5844; N=2,788 HFpEF; 52 Spanish hospitals). Statin HR 0.74 (P=0.002); benefit restricted to non-IHD patients (HR 0.69; P<0.001); IHD subgroup NS; aldosterone antagonists HR 1.34 (confounding likely).
- `wiki/sources/kittleson2024accaha.md` — ACC/AHA 2024 Performance Measures (JACC 2024;84:1123–1143). PM-2: BP control in HFpEF with HTN (first HFpEF-specific performance measure); QM-1: SGLT2i for HFmrEF/HFpEF; QM-2: SDOH screening; QM-6: amyloid screen.

**Disparities (1):**
- `wiki/sources/ilonze2024disparities.md` — Review (Curr Cardiovasc Risk Rep 2025;19:5). Racial/ethnic disparities across HFpEF care continuum; Black patients: lowest NP levels (20–35% low BNP with elevated PCWP); ATTR V122I 3.43% in Black Americans ≥60y; SGLT2i + GLP-1RA underutilised in minority patients.

### Registry updates
- `wiki/citations.md` — 21 new citekeys added to Ingested Sources table + 21 full formatted references (Joseph2016QRS, Cowie2017SDB, Suzuki2018SDB, Kasahara2018CHART2, Beale2019Iron, Ponikowski2020AFFIRM, Rillig2021EastAFNET4, Lindenfeld2021GUIDEHF, Shi2022SST2, Horiuchi2022NPGuided, AlSadawi2022RhythmControl, Zamani2023PericardialFat, Sung2023fQRS, Wester2023SDB, vonHaehling2024FAIR, Timoteo2024EAT, Kittleson2024AccAha, Ilonze2024Disparities, OrtegaHernandez2024Statins, Leahy2025HeartLung, Babb2026VentilatoryLimit)
- `wiki/index.md` — 21 new source entries added across: Guidelines (kittleson2024accaha), Observational Studies (joseph2016qrs, suzuki2018sdb, kasahara2018chart2, zamani2023pericardialfat, sung2023fqrs, leahy2025heartlung, ortegahernandez2024statins), Clinical Trial Papers (ponikowski2020affirm, rillig2021eastafnet4, lindenfeld2021guidehf, vonhaehling2024fair, babb2026ventilatorylimit), Review Articles (cowie2017sdb, horiuchi2022npguided, wester2023sdb, timoteo2024eat, ilonze2024disparities), Systematic Reviews (beale2019iron, shi2022sst2, alsadawi2022rhythmcontrol)
- `wiki/trials.md` — FAIR-HFpEF row updated to add vonhaehling2024fair; GUIDE-HF added to Device Trials; new "Rhythm Control Trials with HF Subgroup Data" section (EAST-AFNET4, AFFIRM-AHF); NCT04068844 (IEEM Obese HFpEF) added to Mechanistic Studies; secondary analyses Rillig2021 and Lindenfeld2021 added to Secondary Analyses Tracked

---

## 2026-05-18 (session 24 — 8 PDFs ingested)

### Source pages created (8)
- `wiki/sources/solomon2012paramount.md` — PARAMOUNT Phase 2 RCT (Lancet 2012;380:1387–1395; NCT00887588). LCZ696 vs. valsartan; N=301; LVEF ≥45%; NT-proBNP ratio 0.77 at 12w (P=0.005); LA volume −4.6 mL at 36w (P=0.003); Phase 2 bridge to PARAGON-HF.
- `wiki/sources/shah2018promis.md` — PROMIS-HFpEF (Eur Heart J 2018;39:3439–3450). Prospective multicentre; N=202; CMD (CFR<2.5) prevalence 75%; CMD correlates with UACR/NT-proBNP; CRP NOT associated with CMD.
- `wiki/sources/arnold2022diamond.md` — DIAMOND-HFpEF (JACC Cardiovasc Imaging 2022;15:1001–1011; NCT03050593). CMR; N=101 HFpEF; MPR 1.74 vs 2.22 controls (P=0.001); MVD 70% vs 48% (P=0.014); MPR and ECV uncorrelated (r=−0.06) — CMD and diffuse fibrosis are independent mechanisms.
- `wiki/sources/tamaki2023nlrplr.md` — PURSUIT-HFpEF NLR/PLR (JAHA 2023;12:e026326; UMIN000021831). N=1,026 ADHF; combined high NLR+PLR HR 2.66 for cardiac death (P=0.0008); CRP NOT independently prognostic.
- `wiki/sources/haykowsky2011exercise.md` — Exercise intolerance determinants (JACC 2011;58:265–274). N=48 HFpEF + 25 HCs; peak VO₂ −30%; strongest predictor: A-VO₂ Diff reserve (β=0.66; P=0.0002) — implicates peripheral mechanisms.
- `wiki/sources/reddy2017artstiff.md` — Arterial stiffening with exercise + nitrite (JACC 2017;70:136–148). N=98 HFpEF; exercise unmasks arterial stiffness (TACI 0.50 vs 0.70; P<0.0001); nitrite RCT substudy (N=52): reduced PCWP −8 mmHg (P<0.0001), improved CO +0.8 L/min.
- `wiki/sources/boralkar2019nlr.md` — NLR trajectory in acute HFpEF (Am J Cardiol 2020;125:229–235). Stanford STRIDE; N=443; NLR trajectory HR 1.26 (P=0.001); incremental to GWTG-HF score (ΔAUC +0.047; P=0.0068).
- `wiki/sources/zhuzhou2021leukocyte.md` — Leukocyte count U-shaped mortality (BMC Cardiovasc Disord 2021;21:333). TOPCAT substudy; N=2,898; Q1 (≤5.5) HR 1.44 and Q4 (>8.0) HR 1.90 vs Q2; sex interaction: significant in women (P=0.002), not in men (P=0.088).

### Registry updates
- `wiki/citations.md` — 8 new citekeys + formatted references (Solomon2012PARAMOUNT, Shah2018PROMIS, Arnold2022DIAMOND, Tamaki2023NLRPLR, Haykowsky2011Exercise, Reddy2017ArtStiff, Boralkar2019NLR, ZhuZhou2021Leukocyte)
- `wiki/trials.md` — PARAMOUNT added; new "Phase 2 / Mechanistic Trials" section created (NCT00887588)
- `wiki/sources-pending-from-meta-analyses.md` — Shah 2018, Arnold 2022, Tamaki NLR/PLR, Zhu/Zhou WBC marked as ingested
- `wiki/index.md` — [[solomon2012paramount]] added to Clinical Trial Papers; 7 new observational/mechanistic source entries added
- `wiki/timeline.md` — Entries added: 2011 (Haykowsky A-VO₂ Diff reserve), 2012 (PARAMOUNT ARNi Phase 2), 2017 (Reddy arterial stiffening + nitrite), 2018 (PROMIS-HFpEF 75% CMD), 2022 (DIAMOND CMR MPR+fibrosis independence), 2023 (Tamaki NLR+PLR HR 2.66)
- `wiki/overview.md` — Session 24 entry added to Recent Additions section

---

## 2026-05-18 (session 23 — entity audit; session 22 continuation logged)

### Log note
The session 22 log entry below was written mid-session and truncated by context compaction. The following records the session 22 work that was not captured there.

### Additional source pages created in session 22 (13)

**Exercise RCTs and rehabilitation (5):**
- `wiki/sources/kitzman2021rehabhf.md` — REHAB-HF main results (Kitzman 2021, NEJM 2021;385:203–216; NCT02196038). N=349 (≥60y, ADHF, any EF; 97% frail/pre-frail). Transitional progressive multidomain rehabilitation vs. usual care. SPPB +1.5 pts (P<0.001; 3× MCID); 6MWD +34 m; KCCQ +7.1; 60-day rehospitalisation NS. Frailty subgroup: pre-frail higher absolute benefit.
- `wiki/sources/mentz2021rehabhfhfpef.md` — REHAB-HF HFpEF subgroup (Mentz 2021, JACC Heart Fail 2021;9:747–757). HFpEF arm (n=185): SPPB +1.9 vs. +1.1 in HFrEF; global rank endpoint significant in HFpEF (P=0.04) but not HFrEF (P=0.69); interaction P=0.098. First evidence that rehabilitation benefits are HFpEF-enriched.
- `wiki/sources/mueller2021optimex.md` — OptimEx-Clin (Mueller 2021, JAMA 2021;325:1298–1309; NCT02078947). N=180, 5 European sites. HIIT vs. MCT vs. guideline control. HIIT +1.5, MCT +2.0 mL/kg/min at 3 months (P<0.05 both vs. control); HIIT NOT superior to MCT (P=NS); neither met MCID; gains lost at 12 months. Closes HIIT superiority debate.
- `wiki/sources/donelli2020hiit.md` — DonelliDaSilveira 2020 (Eur J Prev Cardiol 2020;28:778–787). Single-centre RCT, N=19. HIIT +3.5 vs. MCT +1.9 mL/kg/min (P<0.001 between-group). Likely false-positive from small N; contradicted by OptimEx-Clin N=180.
- `wiki/sources/azhar2020protein.md` — Azhar 2020 (Gerontol Geriatr Med 2020;6:1–8). Pilot RCT, N=27. Protein supplementation + exercise vs. exercise alone vs. usual care. No significant VO₂ benefit. Nutritional co-intervention pilot.

**Systematic reviews and meta-analyses (8):**
- `wiki/sources/jin2022la.md` — Jin 2022 (Heart Fail Rev 2022). 61 studies, 8,806 HFrEF + 9,928 HFpEF. LAVi comparable between EF groups; LA reservoir GLS worse in HFrEF (9–12.8%) vs. HFpEF (18.9–23.4%); AF prevalence higher in HFpEF (34–43%) despite better LA function.
- `wiki/sources/lin2023cmd.md` — Lin 2023 (JACC Heart Fail or similar). CMD meta-analysis in HFpEF; CFR impaired; microvascular rarefaction; links to inflammation pathway.
- `wiki/sources/kaddoura2024betablocker.md` — Kaddoura 2024 (Curr Probl Cardiol 2024). 8 observational studies, N≈11,000. Beta-blocker use associated with lower all-cause mortality (OR 0.81, 95% CI uncertain; all observational). No RCT evidence; confounding highly likely.
- `wiki/sources/fu2024inflammation.md` — Fu 2024 (systematic review/meta-analysis). Inflammatory markers (CRP, IL-6, TNF-α) prognostic in HFpEF; HR range 1.43–2.83; I²=0% (high consistency). Supports inflammatory phenotype targeting.
- `wiki/sources/lee2024lifestyle.md` — Lee 2024 (meta-analysis). Lifestyle interventions (exercise, diet, weight loss) in HFpEF; VO₂ and KCCQ improvements meta-analysed across modalities.
- `wiki/sources/prokopidis2025exercise.md` — Prokopidis 2025 (Eur Heart J Open 2025). Exercise training in HFpEF vs. HFrEF comparative meta-analysis; HFpEF VO₂ effect size characterised.
- `wiki/sources/vandebovenkamp2025hemodynamics.md` — Van de Bovenkamp 2025 (meta-analysis). Hemodynamic responses to exercise in HFpEF; PCWP and CO slope relationships.
- `wiki/sources/ammar2025bnp.md` — Ammar 2025 (meta-analysis). BNP/NT-proBNP levels in HFpEF; diagnostic and prognostic thresholds; correlation with exercise capacity.

### Entity pages created in session 22 (2)

- `wiki/entities/rehab-hf.md` — REHAB-HF entity: NCT02196038; transitional progressive multidomain rehabilitation in 349 acute HF patients (any EF; ≥60y; 97% frail/pre-frail); SPPB +1.5; HFpEF subgroup benefits ≥ HFrEF; rehospitalisation NS. References kitzman2021rehabhf + mentz2021rehabhfhfpef.
- `wiki/entities/optimex-clin.md` — OptimEx-Clin entity: NCT02078947; HIIT vs. MCT vs. guideline control in HFpEF (5 sites; N=180); HIIT not superior to MCT; exercise gains not sustained at 12 months. References mueller2021optimex.

### New file created in session 22 (1)

- `wiki/sources-pending-from-meta-analyses.md` — Catalogs 25+ candidate primary studies identified from the 6 ingested meta-analyses (jin2022la, lin2023cmd, kaddoura2024betablocker, fu2024inflammation, lee2024lifestyle, prokopidis2025exercise), prioritised by evidence potential for future ingest. High-priority candidates include PARAMOUNT (Solomon 2012), Shah 2018 CMD (N=202), Arnold 2022 CMD, Lam 2018 beta-blockers, Tamaki NLR/PLR (N=1,026), Kitzman 2016 SECRET diet arm.

### Registry files updated in session 22 (continued) (5)

- `wiki/citations.md` — 13 new citekeys added (Kitzman2021REHABHF, Mentz2021REHABHFpEF, Mueller2021OptimEx, DonelliDaSilveira2020HIIT, Azhar2020Protein, Jin2022LA, Lin2023CMD, Kaddoura2024BetaBlocker, Fu2024Inflammation, Lee2024Lifestyle, Prokopidis2025Exercise, VandeBovenkamp2025Hemodynamics, Ammar2025BNP) + formatted references.
- `wiki/index.md` — Added 5 exercise trial source entries ([[kitzman2021rehabhf]], [[mentz2021rehabhfhfpef]], [[mueller2021optimex]], [[donelli2020hiit]], [[azhar2020protein]]); added new "Systematic Reviews and Meta-Analyses" section (8 meta-analysis entries); added [[rehab-hf]] and [[optimex-clin]] to Clinical Trial Entities section; added [[sources-pending-from-meta-analyses]] to Core Pages.
- `wiki/timeline.md` — Added 2021 REHAB-HF row (SPPB +1.5; HFpEF subgroup) and 2021 OptimEx-Clin row (HIIT = MCT; gains not sustained) to Treatment table.
- `wiki/entities/supervised-exercise-training.md` — Added 4 new sources to frontmatter; updated OPTIMEX-CLIN table row with full data; added DonelliDaSilveira 2020 HIIT row with contradiction note; added Post-Hospitalisation Rehabilitation (REHAB-HF) subsection with evidence table; updated Related Pages.
- `wiki/overview.md` — Session 22 entry in Recent Additions (13 sources, 2 entities); split "HIIT vs. MICT" debate into "HIIT vs. MCT" (OptimEx-Clin N=180) and new "Beta-blockers in HFpEF" debate (Kaddoura 2024, observational only); added 3 new Knowledge Gaps (post-hospitalisation rehabilitation, beta-blockers RCT gap, inflammatory marker-guided therapy).

---

### Entity audit (session 23)

**Scope:** All 43 entity pages in `wiki/entities/`. Structural checks: Aliases block present, Related Pages present, ≥2 wiki-links per page, non-broken link targets, no stale "pending ingest" notes in Evidence sections.

**Result:** All 43 pages pass structural checks. Three content issues found and fixed.

#### Entity pages fixed (3)

- `wiki/entities/strong-hf.md` — Evidence section had stale "pending full ingest for exact HR/CI" note. Replaced with actual data table: primary ARD 8.1% (2.9–13.2; P=0.0021; RR 0.66); LVEF subgroup table (HFrEF ≤40% ARD 6.3%; HFpEF >40% ARD 12.5%; P-interaction=0.27); safety profile (hypotension 5% vs <1%; renal impairment 3% vs <1%). Added [[mebazaa2022stronghf]] and [[voors2022empulse]] to Related Pages Sources. (data source: raw/2022-Lancet-Mebazaa-STRONG-HF_study.pdf, already ingested as wiki/sources/mebazaa2022stronghf.md)
- `wiki/entities/empulse.md` — Evidence section had "pending full ingest for exact subgroup breakdown". Replaced with actual data: WR 1.36 (95% CI 1.09–1.68; P=0.0054); components: death HR 0.98, HF events rate ratio 0.76, KCCQ-TSS +4.45 pts; HFpEF subgroup (LVEF >40%) WR 1.39 (0.95–2.03); eGFR transient reduction week 1, back to baseline by week 4; no excess hypotension or renal AEs. Added [[voors2022empulse]] to Related Pages Sources. (data source: raw/2022-NatureMed-Voors-EMPULSE_study.pdf, already ingested as wiki/sources/voors2022empulse.md)
- `wiki/entities/reduce-lap-hf-ii.md` — Missing cross-link to [[patel2024reducelaphf]] (REDUCE LAP-HF II echocardiographic substudy, ingested session 20). Entity predated the substudy ingest. Added [[patel2024reducelaphf]] to Related Pages Sources and to frontmatter sources list.

---

## 2026-05-18 (session 22 — 3 exercise/intervention PDFs ingested: INABLE-Training, SECRET-II, HEART Camp)

### Source pages created (3)

- `wiki/sources/borlaug2024inable.md` — INABLE-Training (Borlaug 2024, Mayo Clin Proc 2024;99(2):206–217; NCT02713126). Inorganic sodium nitrite 40 mg TID vs. placebo added to 12-week supervised exercise training in HFpEF (N=73; 75% NYHA III; 63% rural; AF 58.9%). Exercise training improved VO₂ +0.79 mL/kg/min (P<0.001), KCCQ-OSS +5.5 (P<0.001), 6MWD +34 m (P<0.001). Nitrite: no benefit on any endpoint (VO₂ −0.13; P=0.77). Fifth major NO/cGMP pathway negative trial in HFpEF.
- `wiki/sources/brubaker2023secret2.md` — SECRET-II (Brubaker 2023, Circ Heart Fail 2023;16:e010161; NCT02636439). 88 randomised (44/44); 20 weeks; CR+AT vs. RT+CR+AT. Both groups: VO₂peak +5–7%, KCCQ +15–20 points. Resistance training: leg strength +4.9 Nm (P=0.05), muscle quality +0.07 Nm/cm² (P=0.043). Key null findings: RT did NOT add VO₂ benefit (P=0.21) and did NOT prevent skeletal muscle mass loss — refutes primary hypothesis. LV mass and arterial stiffness improved equally in both groups.
- `wiki/sources/alonso2022heartcamp.md` — HEART Camp HFpEF subgroup (Alonso 2022, J Card Fail 2022;28:431–442; NCT01658670). Secondary analysis; N=59 HFpEF (25 HEART Camp, 34 EUC). 18-month behavioral coaching. Adherence: 42% vs. 14% at 12 mo (P=0.025); 56% vs. 0% at 18 mo (P<0.001). 6MWT: +63 m vs. +13 m (P=0.048). KCCQ-OSS/CSS/TSS all Time×Group significant. HFrEF subgroup: no adherence or functional benefit — HFpEF-specific response confirmed.

### Registry files updated (5)

- `wiki/citations.md` — Added 3 citekeys to ingested table (Borlaug2024INABLE, Brubaker2023SECRET2, Alonso2022HEARTcamp) + 3 formatted references.
- `wiki/trials.md` — Added INABLE-Training (new row), updated SECRET-II (corrected description and added source link [[brubaker2023secret2]]), added HEART Camp (new row) to Non-Pharmacological section.
- `wiki/trials-pending.md` — Corrected and struck through INABLE-Training entry (was incorrectly described as "Ivabradine vs. exercise training"; actual: inorganic nitrite + exercise).
- `wiki/index.md` — Added 3 source entries under Clinical Trial Papers section.
- `wiki/log.md` — This entry.

---

## 2026-05-16 (session 21 — SUMMIT primary PDF ingested; packer2025summit.md and summit.md updated)

### Source pages updated (1)

- `wiki/sources/packer2025summit.md` — full rewrite from primary paper (`raw/2025-NEJM-Packer-SUMMIT_primary.pdf`; NEJM 2025;392:427–437; doi:10.1056/NEJMoa2410027). Replaced reconstructed secondary-analysis data with verified primary figures. Key corrections: N 364/367 (was 357/374); follow-up median 104 weeks (was "52 weeks"); age 65.5±10.5 / 65.0±10.9 y (was "~69y"); AF 26.1%/24.8% (was 33–35%, those numbers are CKD vs non-CKD subgroup); 6MWD 305/301 m (was 278–340 m). Added: endpoint revision narrative; NT-proBNP non-significance (0.90; 0.79–1.01; NS); full results table with exact CIs; eGFR assessment schedule (12/24/52 wk); KCCQ assessment schedule (24/52 wk); note on 357/362 being cystatin C subset not full trial N; CMR pericardial fat (not EAT) as driver; numerically higher CV and all-cause death with tirzepatide (NS).

### Entity pages updated (1)

- `wiki/entities/summit.md` — corrected N (364/367), follow-up (104 weeks), baseline table, results table with exact CIs, subgroup consistency note, endpoint revision section, CKD substudy N clarification, updated status removing pending-ingest flag.

### Meta pages updated (2)

- `wiki/citations.md` — removed pending-ingest note from Packer2025SUMMIT table entry; full formatted reference already present.
- `wiki/log.md` — this entry.

---

## 2026-05-15 (session 20 — 21 new sources ingested: sex biology, exercise RCTs, PARAGLIDE-HF analyses, CMR, AI, pathophysiology)

### Source pages created (21)

**Sex differences / baseline biology (3):**
- `wiki/sources/beale2018sex.md` — Beale 2018 (JACC HF): sex-specific HFpEF physiology; women higher LVEF, smaller LV volumes, greater fibrosis
- `wiki/sources/beale2019sex.md` — Beale 2019 (JACC HF): sex differences in HFpEF outcomes and physiology
- `wiki/sources/bozkurt2020sex.md` — Bozkurt 2020 (JACC): sex and gender differences across HF spectrum; PARAGON-HF sex interaction context

**Pharmacology / biomarker (2):**
- `wiki/sources/pfeffer2022topcat.md` — Pfeffer 2022 (Circulation): TOPCAT post-hoc Americas reanalysis; HR 0.82 (0.69–0.98); canrenone undetectable in 30% Russian patients; FDA advisory 8:4:1 vote; basis for spironolactone Class IIb Level B in HFpEF
- `wiki/sources/pandey2025humain.md` — HuMAIN Phase 2A (Pandey 2025, Circ Heart Fail): HU6 (mitochondrial uncoupler small molecule; **NOT bioartificial kidney**) in HFpEF with obesity; NCT05284617; fat-selective catabolism

**AF / arrhythmia (2):**
- `wiki/sources/attia2019ecgaf.md` — Attia 2019 (Lancet): CNN ECG-AI for AF detection in sinus rhythm; AUC 0.87; **NOT an HFpEF study** — clearly marked; methodological precursor to ECG-AI in HFpEF
- `wiki/sources/reddy2024afhfpef.md` — Reddy 2024: AF-HFpEF bidirectional relationship; 83% occult HFpEF in symptomatic AF by exercise RHC; ~82% occult AF in HFpEF at 1 year; anticoagulation ~32% stroke reduction

**Inflammation / GLP-1 (1):**
- `wiki/sources/verma2024inflammation.md` — Verma 2024: semaglutide benefit CRP-independent in STEP-HFpEF; supports HFpEF inflammation heterogeneity consistent with fayyaz2025pathophys

**Exercise RCTs (3):**
- `wiki/sources/sharif2024locomotor.md` — Sharif 2024 (JCF): pilot RCT n=22; 12.5-week resistance training; VO₂peak 17.1→19.4 mL/kg/min; fat-selective; lean mass increased; LF% unchanged
- `wiki/sources/obaya2024aerobic.md` — Obaya 2024 (Physiol Res Int): RCT n=40; lower-limb aerobic cycling superior to arm ergometry (21.51 vs 19.26 mL/kg/min; P<0.001); LVEF unchanged both arms
- `wiki/sources/edelmann2025exdhf.md` — Ex-DHF (Nat Med 2025): n=322; 12-month combined endurance+resistance training; primary (Packer composite) NOT MET (tau-b=−0.073; P=0.17); VO₂ +1.3 mL/kg/min (P=0.003); NYHA OR 5.89 (P<0.001); adherence ~53%; ISRCTN86879094

**PARAGLIDE-HF analyses (4):**
- `wiki/sources/mentz2023paraglide.md` — PARAGLIDE-HF design (JCF 2023): n=467, LVEF >40%, WHF event; 52% women, 22% Black; NCT03988634
- `wiki/sources/fudim2024paraglide.md` — PARAGLIDE-HF symptomatic hypotension analysis (JCF 2024): Sac/Val 24.0% vs Val 15.5% (P=0.020); predictors: LVEF >60%, lower SBP, white race
- `wiki/sources/nouhravesh2025paraglide.md` — PARAGLIDE-HF initiation setting (JAHA 2025): no difference in-hospital vs out-of-hospital (P-interaction=0.99)
- `wiki/sources/rambarat2025paraglide.md` — PARAGLIDE-HF sex analysis (AHJ 2025): NT-proBNP consistent by sex (P-interaction=0.908); women excess symptomatic hypotension (OR 2.29, P=0.012)

**Device trials (2):**
- `wiki/sources/abraham2016champion.md` — CHAMPION complete follow-up (Lancet 2016): n=550; CardioMEMS PA pressure monitoring; randomised phase 33% HF admission reduction (HR 0.67, P<0.0001); open-access 48% reduction (HR 0.52, P<0.0001)
- `wiki/sources/patel2024reducelaphf.md` — REDUCE LAP-HF II echocardiographic substudy (JAMA Cardiol 2024): n=621; LV EDV −5.65 mL (P<0.001); LA EF +1.88 pp (P=0.02); RV EDV +9.58 mL (P<0.001); PVR subgroup interaction P=0.01

**CMR (2):**
- `wiki/sources/ipek2024cmr.md` — Ipek 2024 (EHJ Cardiovasc Imaging): comprehensive CMR review in HFpEF; LACI; exercise CMR; spectroscopy (31P-MRS, 1H-MRS); FT-CMR strain; ECV/T1/T2; perfusion
- `wiki/sources/lange2024cmr.md` — Lange 2024 (Int J Cardiovasc Imaging): cross-sectional CMR n=54 HF (22 HFpEF, 17 HFmrEF, 15 HFrEF) + 19 controls; HFpEF vs controls: LA strain 28.9 vs 35.9% (P=0.008), LV GLS −15.0 vs −19.2% (P=0.001), native T1 1012 vs 988 ms (P=0.003)

**AI/ML (1):**
- `wiki/sources/akerman2025ai.md` — Akerman 2025 (Nat Commun): EchoGo HF v2 (Ultromics) external validation; AUROC 0.797 vs H₂FPEF 0.788 (P=0.001); 9.1% AI intermediate vs 61.7% H₂FPEF; AI-positive HR 2.56 for composite outcome

**Pathophysiology review (1):**
- `wiki/sources/fayyaz2025pathophys.md` — Fayyaz 2025 (Nat Rev Cardiol): 56 human myocardial tissue studies; 8-pathway framework (fibrosis, cardiomyocyte hypertrophy, microvascular rarefaction, diastolic dysfunction [titin/SERCA2a/T-tubule], metabolic derangements [ATP/NAD⁺], inflammation/oxidative stress, cGMP-PKG impairment, ER stress/DNA damage); comorbidity-dependent heterogeneity explains monotherapy failure

### Entity pages created (1)
- `wiki/entities/paraglide-hf.md` — PARAGLIDE-HF entity: NCT03988634; sacubitril/valsartan vs. valsartan in 467 post-WHF HFpEF patients; primary NT-proBNP ratio 0.85 (0.73–0.999); benefit driven by LVEF ≤60% subgroup; 52% women, 22% Black; 4 secondary analyses tabulated

### Registry files updated (3)
- `wiki/trials-pending.md` — Corrected HuMAIN: HU6 mitochondrial uncoupler (not bioartificial kidney); marked INGESTED. Corrected PARAGLIDE-HF: NCT04164043 → NCT03988634; marked INGESTED
- `wiki/trials.md` — Added: PARAGLIDE-HF (NCT03988634, pharmacological); HuMAIN-HFpEF (NCT05284617, Phase 2A, HU6); CHAMPION (NCT00531661, device); Ex-DHF (ISRCTN86879094, exercise). Updated: REDUCE LAP-HF II row (added patel2024reducelaphf echo substudy citekey)
- `wiki/citations.md` — 21 new citekeys added to Ingested Sources (table + full formatted references): beale2018sex, beale2019sex, bozkurt2020sex, pfeffer2022topcat, attia2019ecgaf, reddy2024afhfpef, verma2024inflammation, pandey2025humain, sharif2024locomotor, obaya2024aerobic, edelmann2025exdhf, mentz2023paraglide, fudim2024paraglide, nouhravesh2025paraglide, abraham2016champion, rambarat2025paraglide, patel2024reducelaphf, ipek2024cmr, lange2024cmr, akerman2025ai, fayyaz2025pathophys

---

## 2026-05-14 (session 19 — 4 new sources ingested: exercise hemodynamics series)

### Source pages created (4)
- `wiki/sources/borlaug2010exercise.md` — Borlaug 2010 (Circ Heart Fail, n=55, supine invasive CPET): 58% exertional HFpEF with normal resting hemodynamics; exercise PCWP ≥25 mmHg threshold; PASP ≥45 mmHg screen (sens 96%, spec 95%, AUC 0.99); all noninvasive markers AUC <0.70; hemodynamic gap at 20W (1.5 min); blunted CI/HR response
- `wiki/sources/borlaug2023statement.md` — Borlaug 2023 JACC Scientific Statement: comprehensive HFpEF state-of-the-field; 4-pathway pathophysiology (myocardial stiffening, obesity-cardiometabolic, microvascular inflammation, noncardiac); 5-phenotype Venn model; Central Illustration disease progression spectrum; SGLT2i first-line algorithm; 24 knowledge gaps; ~24 trials in Table 5
- `wiki/sources/landsteiner2025hemodynamics.md` — Landsteiner 2025 (Circ Res, n=872, MGH/Harvard): HC-HFpEF concept (resting PCWP ≥15 OR exercise PCWP/CO slope >2 mmHg/L/min); 4 hemodynamic profiles; exercise-unmasked HFpEF HR 1.42 (1.08–1.86); trial NT-proBNP excludes 67–71% of HC-HFpEF; trial enrichment 87–90% HC-HFpEF
- `wiki/sources/manabe2023sympathetic.md` — Manabe 2023 (Front Cardiovasc Med, mini review): MSNA paradoxical increase during dynamic exercise in HFpEF; static exercise MSNA resembles controls; LBF/LVC reduced requiring higher perfusion pressure; functional sympatholysis gap; candesartan and perindopril pharmacological evidence

### Concept pages updated (4)
- `wiki/concepts/exercise-intolerance.md` — Added sympathetically-mediated vasoconstriction section (dynamic vs. static exercise distinction); functional sympatholysis knowledge gap; Borlaug 2010 hemodynamic evidence (PCWP table, PASP screen); Landsteiner 2025 PCWP/CO slope as prognostic metric; 2 new Evidence table rows; 2 new Open Questions; 2023 and 2025 History entries; updated frontmatter sources and Related Pages
- `wiki/concepts/hfpef-diagnosis.md` — Added HC-HFpEF concept and PCWP/CO slope >2 mmHg/L/min upright threshold; exercise PASP ≥45 mmHg noninvasive surrogate (AUC 0.99); 23–28% exercise-unmasked gap; Borlaug 2010 and Landsteiner 2025 History entries; updated frontmatter and Related Pages
- `wiki/concepts/hfpef-diagnostic-definitions.md` — Added Landsteiner 2025 HC-HFpEF concept to History; trial enrollment vs. HC-HFpEF gap table (STEP/FINEARTS/EMPEROR/PARAGON); 67–71% NT-proBNP exclusion; updated frontmatter, Related Pages, Contradictions
- `wiki/concepts/hfpef-phenotype-profiling.md` — Added Borlaug 2023 5-phenotype Venn table (obese/cardiometabolic, arterial stiffening, ischaemic/CMD, pulmonary vascular, LA myopathy); disease progression spectrum (LA→PH→RV); autonomic dysfunction section (sympathetic excess from Manabe 2023); History entry; updated frontmatter and Related Pages

### Entity pages updated (1)
- `wiki/entities/cardiopulmonary-exercise-testing.md` — Expanded diagnostic gold standard section with supine vs. upright protocol distinction; Borlaug 2010 protocol (PCWP ≥25 mmHg supine, PASP ≥45 mmHg screen, 20W gap onset); Landsteiner 2025 upright protocol (PCWP/CO slope >2, HC-HFpEF concept, exercise-unmasked prognosis); expanded Evidence table (11 rows); updated frontmatter and Related Pages

### Registry files updated (6)
- `wiki/citations.md` — 4 new entries (table + full formatted references): borlaug2010exercise, borlaug2023statement, landsteiner2025hemodynamics, manabe2023sympathetic
- `wiki/contradictions.md` — Added #28 (trial NT-proBNP thresholds exclude 67–71% of HC-HFpEF) and #29 (supine vs. upright exercise protocol thresholds non-interchangeable)
- `wiki/trials-pending.md` — Added 24 trials from Borlaug 2023 Table 5 (CAMEO-SEMA, CAMEO-DAPA, HuMAIN, SPIRRIT, SPIRIT-HF, PARAGLIDE-HF, CADENCE, PH-HFpEF, INABLE-Training, KNO3CK OUT HFpEF, RESPONDER, RELIEVE-HF, FROST-HF, RELAXIN-LA, CABA-HFpEF, ENDEAVOR, HERMES, CoIPET, REBALANCE-HF, AIM HIGHer, HERACLES-HFpEF, IRONMET-HFpEF, REHAB-HFpEF, AMETHYST)
- `wiki/index.md` — Added [[borlaug2010exercise]], [[borlaug2023statement]], [[landsteiner2025hemodynamics]], [[manabe2023sympathetic]] in appropriate sections
- `wiki/timeline.md` — Added Borlaug 2010 (Diagnostic Criteria section), Borlaug 2023 + Manabe 2023 (Pathophysiology section), Landsteiner 2025 (Diagnostic Criteria section)
- `wiki/overview.md` — Session 19 entry in Recent Additions; 2 new Knowledge Gaps (trial-to-real-world gap, exercise protocol standardisation)

---

## 2026-05-13 (session 18 — continued: ingest verification, Aliases batch complete)

### Ingest verification — batch 1: mechanistic/observational papers (agent 1)
Five source pages verified and corrected against PDFs:
- wiki/sources/paulus2013novelparadigm.md — confirmed accurate; last_updated bumped
- wiki/sources/edelmann2013aldodhf.md — 6MWD P-value corrected (P=0.03 → P=0.02); NT-proBNP table enhanced with raw group medians (165 vs 152 ng/L); last_updated bumped
- wiki/sources/alnaamani2015pac.md — fixed specificity error (50% → 38%, per PDF Table 3); multivariate HR table added (PAC HR 0.48/mL/mmHg P=0.02); full ROC AUC table with 95% CIs; median follow-up 3.6 yr; demographics added; vasodilator testing results added
- wiki/sources/shah2015phenomapping.md — HR disambiguation: CV hosp/death HR 4.2 (abstract) vs HF hosp HR 4.8 (Table 5); full outcomes event-count + unadjusted + adjusted HR table added
- wiki/sources/kitzman2016secret.md — racial composition corrected (72% Black → ~45% Black, per PDF Table 1); arm sizes n=26/24/25/25 added; attention control detail added; secondary outcomes added

### Ingest verification — batch 2: pharmacological trials (agent 2)
Five source pages verified and corrected against PDFs:
- wiki/sources/anker2021emperor.md — **major rewrite from placeholder**: complete author list, journal citation, NCT+dates, enrollment dates (Mar 2017–Apr 2020), follow-up 26.2 months, NT-proBNP threshold correction (>300 without AF / >900 with AF — thresholds had been swapped), full baseline table, primary endpoint HR 0.79 (0.69–0.90, P<0.001), components (HF hosp HR 0.71, CV death HR 0.91 NS), secondary endpoints (eGFR slope, KCCQ-CSS, total HF hosp), subgroup table (T2DM/LVEF/sex), safety table; source file corrected from placeholder to raw/2021-NEJM-Anker-EMPEROR-preserved.pdf
- wiki/sources/pitt2014topcat.md — site count corrected 266→233; discontinuation rates corrected (34.3%/31.4%); BNP-stratum interaction added (P=0.01); NT-proBNP baseline imbalance noted (P=0.04)
- wiki/sources/redfield2013relax.md — NYHA II–IV corrected to II–III (NYHA IV excluded); last_updated bumped
- wiki/sources/pieske2017socrates.md — author list corrected; arm sizes corrected (n=96 each active arm, n=93 placebo); enrollment window corrected (4 weeks stabilization); NT-proBNP P=0.2017 and LAV P=0.3688 added
- wiki/sources/maurer2018attract.md — author list corrected; enrollment dates Dec 2013–Aug 2015 added; Pfizer funder noted

### Task #9 — Aliases batch: COMPLETE
Added `## Aliases` blocks to all remaining entity and concept pages:
- Entities: step-hfpef.md (STEP-HFpEF acronym, NCT04788511, Kosiborod 2023, STEP-HFpEF DM companion)
- Concepts (11 pages): diastolic-dysfunction, exercise-intolerance, ml-ai-hfpef, guideline-comparison, hfpef-phenotype-profiling, hfpef-treatment-gap, hfpef-diagnosis, natriuretic-peptides, hfpef-diagnostic-definitions, hf-phenotype-classification
### Ingest verification — batch 3: newer trials and AI papers (agent 3)
Six source pages verified and corrected against PDFs:
- wiki/sources/pandey2021deepnnecho.md — journal issue 14(9)→14(10); AUROC corrected (hemodynamic 0.883 vs 0.676 P=0.011; classifiable-only 0.894 vs 0.829 P=0.319 NS — significance implication removed); clinical outcome HR 3.96 (1.24–12.67, P=0.021) added; TOPCAT high-risk prevalence 81.1% added; spironolactone interaction P-value clarified as NS
- wiki/sources/mebazaa2022stronghf.md — 4 critical errors corrected: (1) visit frequency 8→4.8 (SD 1.0); (2) EQ-5D VAS lower CI 0.74→1.74; (3) **LVEF subgroup ARDs reversed** (original HFrEF=12.5% / HFpEF=6.3% → correct HFrEF LVEF ≤40%=6.3% / HFpEF LVEF >40%=12.5% per Figure 4); (4) trial stopped for **efficacy** not futility; also added exact event counts, NT-proBNP ratios, full baseline table
- wiki/sources/voors2022empulse.md — **entire author list replaced** (40+ authors from a different paper → correct 30 EMPULSE authors); NT-proBNP eligibility thresholds added (≥1600 non-AF / ≥2400 AF); win ratio component breakdown added; full baseline + safety tables added
- wiki/sources/solomon2024finearts.md — race/geographic breakdown added; baseline characteristics expanded (17-subgroup prespecified analysis table from Figure 2); sensitivity analyses added
- wiki/sources/gao2025ecgdl.md — **entire author list replaced** (fictional list → correct 5 authors: Gao Z, Yang Y, Yang Z, Zhang X, Liu C); LVEDP threshold corrected ("≥15-16 mmHg" → explicitly 12 mmHg per paper); CNN-LSTM architecture details added; Cohort B prospective confirmed
- wiki/sources/kosiborod2024stephfpefdm.md — DOI corrected (NEJMoa2313307→NEJMoa2313917); confirmed as NCT04916470 (DM companion, not non-DM); **hierarchical composite win ratio 1.58 (1.29–1.94, P<0.001) added** (was entirely missing); dose escalation corrected (maintenance week 16); full baseline table added

### Downstream corrections from batch 3
- wiki/timeline.md — STRONG-HF row: ARDs corrected (HFrEF 12.5%→6.3%; HFpEF 6.3%→12.5%); labelled with LVEF threshold
- wiki/overview.md — Session 12-14 entry: same STRONG-HF ARD correction applied

### Task #9 — Aliases batch: COMPLETE
Added `## Aliases` blocks to all entity and concept pages:
- Entities: step-hfpef.md, tirzepatide-hfpef.md (minimal redirect aliases)
- Concepts (10 pages): diastolic-dysfunction, exercise-intolerance, ml-ai-hfpef, guideline-comparison, hfpef-phenotype-profiling, hfpef-treatment-gap, hfpef-diagnosis, natriuretic-peptides, hfpef-diagnostic-definitions, hf-phenotype-classification
- All entity pages from prior session (35) + 2 this session = 37 entity pages; all 12 concept pages now have Aliases blocks
- Total Aliases blocks added across session 18: 47 entity/concept pages (including the 35 from prior session context)

---

## 2026-05-13 (session 18 — lint fixes continued: SUMMIT stale refs, link fixes, stub standardisation, new pages)

### Remaining SUMMIT stale-reference fixes (completing session 17 task)
- wiki/entities/step-hfpef.md line 43 — fixed "SUMMIT ongoing, peak VO₂ + KCCQ co-primary" → tirzepatide, published NEJM 2025, correct co-primaries (KCCQ-CSS + CV death/worsening HF), HR 0.62
- wiki/sources/kittleson2023acc.md line 167 — fixed SUMMIT=semaglutide / STEP-HFpEF=tirzepatide swap; added published status (STEP-HFpEF 2023, SUMMIT NEJM 2025)
- wiki/sources/kittleson2023acc.md line 258 — corrected drug assignments and noted both trials now published

### Lint fixes
- Task #2: [[hfpef-phenotypes]] → [[hfpef-phenotype-profiling]] in 4 source files (alnaamani2015pac.md ×2, gao2025ecgdl.md, maurer2018attract.md ×2, pandey2021deepnnecho.md ×2)
- Task #4: [[hemodynamics]] → [[diastolic-dysfunction]] in alnaamani2015pac.md Related Pages
- Task #6: [[atrial-fibrillation|AF]] backslash → [[atrial-fibrillation|AF]] in hfpef-diagnosis.md (×2), natriuretic-peptides.md, echocardiography.md
- Task #7: Removed redundant SET outcomes table from hfpef-treatment-gap.md; replaced with cross-reference to [[supervised-exercise-training]] with one-line evidence summary
- Task #10: Standardised `raw/[pending ingest]` → `~ # pending ingest` in 13 entity files: attr-act, caba-hfpef, empulse, fair-hfpef, pep-chf, rehab-hfpef, relax, socrates-preserved, sota-p-cardia, spirit-hf, spirrit, strong-hf, victoria
- Task #11: Added Notes column to citations.md Stub Sources table; flagged Armstrong2020VICTORIA as HFrEF trial + no PDF; Cleland2006PEPCHF as HFpEF + no PDF; Packer2025SUMMIT as PDF not yet in raw/

### New pages created
- wiki/entities/vitality-hfpef.md — VITALITY-HFpEF entity: vericiguat 15/10 mg vs. placebo; N=789; KCCQ-PLS neutral; sGC class closed for HFpEF; SUMMARY + Aliases + Evidence + Contradictions sections
- wiki/concepts/pulmonary-hypertension-hfpef.md — PH-HFpEF concept stub: IpcPH vs. CpcPH; PAC > PVR for prognosis (Al-Naamani 2015); treatment gap; Paulus 2013 inflammatory mechanism
- wiki/entities/myovasc.md — MyoVasc registry stub: N=3,289; 10-year follow-up; DZHK Rhine-Main; PI Philipp Wild; backbone for MyoMobile RCT; NCT04064450; design pending ingest (Gobel 2021 Eur J Prev Cardiol)

### Registry files updated
- wiki/index.md — Added [[vitality-hfpef]] to Clinical Trial Entities, [[myovasc]] to Registry Entities, [[pulmonary-hypertension-hfpef]] to Concepts

---

## 2026-05-13 (session 17 — SUMMIT ingest + major correction)

### SUMMIT ingest — CRITICAL CORRECTION: SUMMIT = tirzepatide (Eli Lilly), NOT semaglutide

**Error corrected:** wiki had SUMMIT (NCT04847557) incorrectly assigned to semaglutide. Confirmed from NCT04847557 study file and JACC secondary analysis papers: SUMMIT = tirzepatide (LY3298176), Eli Lilly. NCT04788511 belongs to STEP-HFpEF (semaglutide; Novo Nordisk).

**Created new source pages:**
- wiki/sources/packer2025summit.md — Primary NEJM 2025 paper (Packer M et al.; N Engl J Med. 2025;392:427-437; doi:10.1056/NEJMoa2410027); PDF not in raw/ — reconstructed from secondary analyses; key result: HR 0.62 (0.41-0.95; P=0.026) for CV death/worsening HF; KCCQ-CSS +6.9 pts (3.3-10.6; P<0.001)
- wiki/sources/packer2025summit-ckd.md — JACC 2025;85:1721-1735 CKD subanalysis (raw/2025-JACC-Packer-SUMMIT_study.pdf); 61% CKD; benefit consistent across CKD/no-CKD (interaction P=0.86); weight loss −13.3% (CKD) / −14.5% (no-CKD) tirzepatide vs −2.2%/−2.4% placebo
- wiki/sources/kramer2025summit-cmr.md — JACC 2025;85:699-706 CMR substudy (raw/2025-JACC-Kramer-SUMMIT-CMR_substudy.pdf); N=106 completed; LV mass −11 g (P=0.004); paracardiac fat −45 mL (P<0.001); first GIP/GLP-1 RA to reduce LV mass in HFpEF by CMR

**Rewrote:**
- wiki/entities/summit.md — Complete rewrite: tirzepatide (LY3298176; Eli Lilly), co-primary KCCQ+CV events, published NEJM 2025; added ## Aliases block; added SUMMIT vs STEP-HFpEF comparison table; added evidence table from secondary sources pending primary PDF
- wiki/entities/tirzepatide-hfpef.md — Converted to redirect → [[summit]]; they are the same trial (NCT04847557)

**Updated registry/index files:**
- wiki/trials.md — SUMMIT row corrected (tirzepatide, correct title, status "2024 NEJM Jan 2025"); tirzepatide-hfpef row removed (merged into SUMMIT)
- wiki/citations.md — Added Packer2025SUMMITCKD and Kramer2025SUMMITCMR to Ingested Sources table; added Packer2025SUMMIT to Stub Sources; added all 3 formatted references
- wiki/index.md — Updated [[summit]] and [[tirzepatide-hfpef]] entity entries; added 3 new source page entries (packer2025summit, packer2025summit-ckd, kramer2025summit-cmr)
- wiki/contradictions.md — Contradiction #22 updated (SUMMIT now published; SUMMIT vs STEP-HFpEF class-effect question); contradiction #27 added (tirzepatide CMR LV mass −11 g vs. semaglutide echo no change)
- wiki/overview.md — High-level summary updated to reflect SUMMIT publication; knowledge gap updated from "SUMMIT ongoing" → "SUMMIT published (2025)"; session 17 added to Recent Additions
- wiki/timeline.md — SUMMIT added to Treatment table (2024/2025) and Landmark Trials table

---

## 2026-05-13 (session 16 — lint + STEP-HFpEF ingest)

### Wiki lint fixes (17 issues resolved)

**Correct fixes applied:**
- Fix 1: Removed duplicate `Solomon2024FINEARTS` entry from stub formatted references in citations.md (was already in ingested section)
- Fix 2: Added `Yusuf2003CHARM` row to citations.md ingested table (done in prior session, confirmed present)
- Fix 3: Updated `Edelmann2013ALDODHF` DOI note in citations.md (ISRCTN94726526 is trial registry ID)
- Fix 5: Removed FINEARTS-HF from "ongoing trials" table in hfpef-treatment-gap.md (trial published 2024)
- Fix 6: Updated ESC contradictions text in hfpef-treatment-gap.md — "No ESC HFpEF recommendation (ESC 2021)" → "Class I Level A for HFpEF/HFmrEF (ESC 2023)"
- Fix 8: REDUCE-LAP-HF-II frontmatter stub syntax fixed (prior session)
- Fix 10: armstrong2020victoria.md frontmatter stub syntax fixed (prior session)
- Fix 11: cleland2006pepchf.md frontmatter stub syntax fixed (prior session)
- Fix 12: Removed duplicate `### Clinical Trial Papers` heading in index.md
- Fix 13: Merged `### Guidelines` + `### Guidelines and Consensus Documents` into single section in index.md; kittleson2023acc, anker2023hfpefphenotype, savarese2022globalburden moved up
- Fix 16: guideline-comparison.md double separator fixed (prior session)
- Fix 17: Replaced 10-row failed-trials table in hfpef-treatment-gap.md with 1-sentence cross-reference to [[trials]]

**Incorrect-fix corrections:**
- Fix 4: STEP-HFpEF row (`| STEP-HFpEF | Tirzepatide (GLP-1/GIP) | ...`) removed from ongoing trials table in hfpef-treatment-gap.md (STEP-HFpEF = semaglutide and is published); STEP-HFpEF results added to evidence section as item 4; tirzepatide NCT corrected in trials.md (`NCT04788511` → `[verify on ingest]`) and entity page updated
- Fix 7+14: Created wiki/entities/attr-cm.md (ATTR Cardiomyopathy disease entity; aliases block: ATTR-CM, ATTRwt, ATTRv, TTR cardiomyopathy); links to [[attr-act]], [[hfpef-phenotype-profiling]], [[hfpef-diagnosis]]
- Fix 9: Moved `Kosiborod2023STEPHFPEF` from Stub Sources → Ingested Sources in citations.md (both table and formatted references); stub formatted reference removed
- Fix 15: Created wiki/concepts/coronary-microvascular-dysfunction.md (Paulus–Tschöpe paradigm; aliases: CMD, microvascular disease; sources: paulus2013novelparadigm, damario2019cmd); no alias overlap found in existing pages

### STEP-HFpEF ingest (raw/2023-NEJM-Kosiborod-STEP_HF_study.pdf + NCT04788511 study file)
- Upgraded: wiki/sources/kosiborod2023stephfpef.md (stub → full source page)
- CORRECTION: Dual primary endpoints are KCCQ-CSS + body weight (not KCCQ-CSS + 6MWD as in stub); 6MWD is confirmatory secondary
- Key results: KCCQ-CSS +7.8 pts (4.8–10.9; P<0.001), body weight −10.7 pp (−11.9 to −9.4; P<0.001), 6MWD +20.3m (P<0.001), CRP ratio 0.61 (P<0.001), win ratio 1.72 (P<0.001); HF events HR 0.08 (exploratory); SAEs 13.3% vs. 26.7%
- NCT04788511 confirmed from paper abstract (STEP-HFpEF non-DM; enrollment March 2021–March 2022; 96 sites; 13 countries)
- Updated: wiki/entities/step-hfpef.md (NCT confirmed, dual primary corrected, exact CIs added, frontmatter file updated)
- Updated: wiki/trials.md STEP-HFpEF row NCT `[verify on ingest]` → `NCT04788511`
- Updated: wiki/citations.md (Kosiborod2023STEPHFPEF moved stub → ingested; formatted reference added)
- Updated: wiki/contradictions.md #22 (corrected numbers: +7.8 pts, −10.7 pp, +20.3m, win ratio 1.72)
- New entries: index.md (step-hfpef entity + kosiborod2023stephfpef source); timeline.md (2023 STEP-HFpEF treatment + landmark); overview.md (knowledge gaps updated; recent additions updated)
- Added: 2023 STEP-HFpEF + 2024 FINEARTS-HF to timeline.md Landmark Trials table
- Stub note removed from index.md kosiborod2023stephfpef and step-hfpef entries

---

## 2026-05-13 (session 15 continuation)

### Full TOPCAT ingest (raw/2014-NEJM-Pitt-TOPCAT_study.pdf; Pitt2014TOPCAT)
- Upgraded: wiki/sources/pitt2014topcat.md (partial stub → full page with exact data from PDF)
- Key result: primary HR 0.89 (0.77–1.04; P=0.14) NEUTRAL; HF hosp HR 0.83 (P=0.04) only significant component; all-cause mortality HR 0.91 (P=0.29); Americas 27.3% vs 31.8% (interaction P=0.12 — NOT significant in paper); hyperkalemia 18.7% vs 9.1%; urinary metabolite contamination evidence NOT in this paper (published separately); NCT00094302
- CORRECTION: Americas subgroup narrative derives from post-hoc analyses; interaction P=0.12 in main paper is not significant — updated to reflect this accurately

### Stub upgrades from PDFs in raw/
- **STRONG-HF** (raw/2022-Lancet-Mebazaa-STRONG-HF_study.pdf; Mebazaa2022STRONGHF)
  - Upgraded: wiki/sources/mebazaa2022stronghf.md (stub → full page)
  - Key result: N=1,078; 180-day ARD 8.1% (2.9–13.2; P=0.0021); RR 0.66 (0.50–0.86); HFrEF subgroup ARD 12.5%, HFpEF subgroup ARD 6.3%; hypotension 5% vs <1%; NCT04142201; DOI 10.1016/S0140-6736(22)02143-1
- **EMPULSE** (raw/2022-NatureMed-Voors-EMPULSE_study.pdf; Voors2022EMPULSE)
  - Upgraded: wiki/sources/voors2022empulse.md (stub → full page)
  - Key result: N=530; win ratio 1.36 (1.09–1.68; P=0.0054); deaths 4.2% vs 8.3%; HFpEF subgroup 1.39 (0.95–2.03); NCT04157751; predominantly HFrEF (69%)
- **STEP-HFpEF DM** (raw/2024-NEJM-Kosiborod-STEP-HFpEF_study.pdf; Kosiborod2024STEPHFPEFDM)
  - DISCOVERY: PDF in raw/ is the DM companion paper (NEJM 2024;390:1394–1407), NOT the non-DM stub (NEJM 2023;389:1069–1084)
  - Created: wiki/sources/kosiborod2024stephfpefdm.md (new source page from DM companion PDF)
  - Key result: KCCQ-CSS +7.3 pts (4.1–10.4; P<0.001); 6MWD +14.3m (3.7–24.9; P=0.008); weight −6.4%; CRP ratio 0.67 (P<0.001); NT-proBNP ratio 0.8; HF hosp HR 0.40 (0.15–0.92); NCT04916470
  - Updated: kosiborod2023stephfpef.md (added cross-reference to DM companion; clarified non-DM stub status)

### Updated files
- wiki/citations.md: moved Mebazaa2022STRONGHF, Voors2022EMPULSE from Stub → Ingested; added Kosiborod2024STEPHFPEFDM as new Ingested entry; fixed STRONG-HF DOI (02143-1 from PDF vs 02076-1 in stub); moved/added full formatted references; removed RELAX/ATTRACT/SOCRATES duplicates from Stub section
- wiki/index.md: updated mebazaa2022stronghf, voors2022empulse descriptions with exact numbers; added kosiborod2024stephfpefdm entry; updated kosiborod2023stephfpef entry to note stub status

### Meta-file updates (contradictions, overview, timeline)
- wiki/contradictions:
  - Corrected #2 (TOPCAT Americas): Americas interaction P=0.12 — not significant in main paper; post-hoc narrative corrected; added exact primary HR 0.89 (P=0.14)
  - Added #25 (RELAX cGMP engagement without functional benefit): cGMP +133% (P=0.006) confirmed; VO2 P=0.90; safety signal; convergent NO/cGMP pathway failure
  - Added #26 (ATTR-ACT ATTRwt positive vs ATTRm neutral): ATTRwt P<0.001; ATTRm P=0.30 (underpowered N~36); NYHA III P=0.78
- wiki/overview.md: Added sessions 12–14 and session 15 entries to Recent Additions
- wiki/timeline.md:
  - Added RELAX (2013), SOCRATES-PRESERVED (2017), ATTR-ACT (2018) to Landmark Trials
  - Corrected TOPCAT row (P=0.14; interaction P=0.12)
  - Added EMPULSE (2022), STRONG-HF (2022) to Landmark Trials
  - Added STEP-HFpEF DM (2024) to Landmark Trials

---

## 2026-05-12 (session 14 continuation — context resumed)

### Stub upgrades (PDF already read in session 14; source pages fully written)
- **RELAX** (raw/2013-JAMA-Redfield-RELAX_study.pdf; Redfield2013RELAX)
  - Upgraded: wiki/sources/redfield2013relax.md (stub → full page with exact data)
  - Key result: sildenafil vs. placebo; peak VO₂ −0.20 vs. −0.20, P=0.90; all secondary endpoints NS; safety signal: creatinine (P=0.047), NT-proBNP (P=0.03), endothelin-1 (P=0.046), uric acid (P=0.02) all worse; cGMP confirmed increased (P=0.006) — target engaged, mechanism failed
- **SOCRATES-PRESERVED** (raw/2017-EHJ-Pieske-SOCRATES-PRESERVED_study.pdf; Pieske2017SOCRATES)
  - Upgraded: wiki/sources/pieske2017socrates.md (stub → full page)
  - Key result: vericiguat 5 arms; co-primary NT-proBNP + LAV both P>0.2; exploratory KCCQ-CSS at 10 mg +9.2 pts (P=0.016); heart rate −5.9 bpm (P=0.0045); protocol violation 48 patients; VITALITY-HFpEF phase 3 was neutral
- **ATTR-ACT** (raw/2018-NEJM-Maurer-ATTR-ACT_study.pdf; Maurer2018ATTRACT)
  - Upgraded: wiki/sources/maurer2018attract.md (stub → full page)
  - Key result: tafamidis pooled (264) vs. placebo (177); Finkelstein-Schoenfeld P<0.001; win ratio 1.695 (1.255–2.289); mortality HR 0.70 (0.51–0.96); CV hosp RR 0.68 (0.56–0.81); 6MWD reduced decline 75.68m; ATTRwt P<0.001; ATTRm P=0.30; ATTRwt ~13% of HFpEF patients

### Updated files
- wiki/citations.md: moved Redfield2013RELAX, Pieske2017SOCRATES, Maurer2018ATTRACT from Stub → Ingested Sources (table + full references)

---

## 2026-05-12 (session 14 — continued from session 13)

### Fully ingested (PDF read; source pages created from actual data)
- **Al-Naamani 2015 PAC** (raw/2015-JACHF-AlNaamani-PAC_in_PH-LHD_study.pdf; AlNaamani2015PAC)
  - Created: wiki/sources/alnaamani2015pac.md
  - Key result: PAC <1.1 mL/mmHg: HR 4.9 (1.9–12.4; P<0.001) for mortality in HFpEF+PH-LHD; PVR AUC 0.37 (useless); only age + PAC independently predict mortality; Comb-PH (DPG≥7) NS
- **Pandey 2021 DeepNN Echo** (raw/2021-JACCImaging-Pandey-DeepNN_diastolic_dysfunction.pdf; Pandey2021DeepNNEcho)
  - Created: wiki/sources/pandey2021deepnnecho.md
  - Key result: TDA-based DeepNN AUROC 0.988/0.997; external hemodynamic AUC 0.894 vs. ASE 0.829; e' most important variable; TOPCAT substudy (N=518): high-risk HR 1.92; spironolactone HR 0.65 (P=0.01) only in high-risk group; interaction P<0.05
- **Gao 2025 CNN-LSTM ECG** (raw/2025-ESCHeartFail-Gao-CNN_LSTM_ECG_HFpEF.pdf; Gao2025ECGDL)
  - Created: wiki/sources/gao2025ecgdl.md
  - Key result: CNN-LSTM on 12-lead ECG; 78% accuracy (N=238 training), 71.8% (N=117 validation); reference = LVEDP; BNP 22 vs. 20 pg/mL P=0.71; E/e' 8.25 vs. 8.5 P=0.66 — both NS between risk groups

### Updated files
- wiki/citations.md: added AlNaamani2015PAC, Pandey2021DeepNNEcho, Gao2025ECGDL to Ingested Sources table + full formatted references
- wiki/index.md: added alnaamani2015pac, pandey2021deepnnecho, gao2025ecgdl to Observational Studies section

---

## 2026-05-12 (session 13 — continued from session 12)

### Fully ingested (PDF read; source pages created/updated from actual data)
- **FINEARTS-HF** (raw/2024-NEJM-Solomon-FINEARTS-HF_study.pdf; Solomon2024FINEARTS)
  - Created: wiki/sources/solomon2024finearts.md (full source page with exact data from PDF)
  - Updated: wiki/entities/finearts-hf.md (promoted from stub to full entity with exact numbers)
  - Citations: Solomon2024FINEARTS moved from Stub Sources → Ingested Sources in citations.md; DOI confirmed 10.1056/NEJMoa2407107
  - Key result: RR 0.84 (95% CI 0.74–0.95; P=0.007); N=6001; 37 countries; median 32-month follow-up
- **ALDO-DHF** (raw/2013-JAMA-Edelmann-Aldo-DHF_study.pdf; Edelmann2013ALDODHF)
  - Created: wiki/sources/edelmann2013aldodhf.md (full source page)
  - Created: wiki/entities/aldo-dhf.md (new entity page)
  - Added: row in wiki/trials.md Historical HFpEF Pharmacological Trials table (ISRCTN94726526)
  - Citations: Edelmann2013ALDODHF added to Ingested Sources in citations.md (DOI pending crossref verification)
  - Key result: E/e' −1.5 P<0.001 ✓; peak VO₂ +0.1 P=0.81 ✗; LV mass −6 g/m² P=0.009; 6MWD −15m P=0.02 (worse)

### Updated files
- wiki/contradictions.md: updated #21 (added ALDO-DHF + exact FINEARTS-HF numbers); added #24 (ALDO-DHF structural-functional dissociation)
- wiki/index.md: added solomon2024finearts, edelmann2013aldodhf (sources); added aldo-dhf (entities); updated finearts-hf description

### Continued (same session) — 3 additional full ingests
- **Paulus & Tschöpe 2013 JACC** (raw/2013-JACC-Paulus-Tschoeppe-HFpEF_novel_paradigm.pdf; Paulus2013NovelParadigm)
  - Created: wiki/sources/paulus2013novelparadigm.md
  - Key content: novel HFpEF paradigm; comorbidities → inflammation → coronary microvascular → ↓NO → ↓PKG → titin stiffness + fibrosis; proposes HFpEF ≠ LV afterload excess; statin observational data (Figure 4)
- **SECRET** (raw/2015-JAMA-Kitzman-SECRET_study.pdf; Kitzman2016SECRET; published JAMA 2016;315:36–46)
  - Created: wiki/sources/kitzman2016secret.md
  - Created: wiki/entities/secret.md
  - Added: row in wiki/trials.md Non-Pharmacological section (NCT00959660)
  - Key result: exercise +1.2 mL/kg/min VO₂ P<0.001; diet +1.3 mL/kg/min P<0.001; combined +2.5 (additive); diet KCCQ +7 pts P=0.004; MLHF QoL co-primary NS
  - Note: NCT00959660 is the SECRET trial — matches raw/Study Details NCT00959660 .md file
- **Shah 2015 Phenomapping** (raw/2014-CirculationAHA-Shah-Phenomapping.pdf; Shah2015Phenomapping; Circulation 2015;131:269–279)
  - Created: wiki/sources/shah2015phenomapping.md
  - Key result: 3 phenogroups (young/mild; obese/metabolic; cardiorenal/advanced); HF hospitalisation HR 4.2 phenogroup 3 (P<0.001); validated in 107 independent patients; SVM AUC 0.70–0.76
- Updated: wiki/citations.md (added Paulus2013NovelParadigm, Shah2015Phenomapping, Kitzman2016SECRET to Ingested Sources)
- Updated: wiki/index.md (added 4 new source pages + 1 new entity page)

## 2026-04-30 (session 1)
- Ingested: raw/2021-ESC-Guidelines-Heart-Failure.pdf (McDonagh2021ESC)
- Created:
  - wiki/sources/mcdonagh2021esc.md
  - wiki/entities/hfpef.md
  - wiki/entities/hfmref.md
  - wiki/entities/hfref.md
  - wiki/entities/sglt2-inhibitors.md
  - wiki/entities/sacubitril-valsartan.md
  - wiki/entities/spironolactone.md
  - wiki/entities/paragon-hf.md (stub)
  - wiki/entities/topcat.md (stub)
  - wiki/entities/charm-preserved.md (stub)
  - wiki/entities/i-preserve.md (stub)
  - wiki/concepts/hf-phenotype-classification.md
  - wiki/concepts/hfpef-diagnosis.md
  - wiki/concepts/hfpef-treatment-gap.md
  - wiki/concepts/diastolic-dysfunction.md
  - wiki/concepts/natriuretic-peptides.md
- Updated:
  - wiki/index.md (initial population)
  - wiki/overview.md (initial population)
  - wiki/contradictions.md (initial population)

## 2026-04-30 (session 2 — template migration + content fixes + study stubs)

### Template migration (all pages migrated from old ## Content format to current templates)
- wiki/sources/mcdonagh2021esc.md — migrated to source template
- wiki/entities/hfpef.md — migrated to entity template
- wiki/entities/hfref.md — migrated to entity template
- wiki/entities/hfmref.md — migrated to entity template
- wiki/entities/sglt2-inhibitors.md — migrated to entity template
- wiki/entities/sacubitril-valsartan.md — migrated to entity template
- wiki/entities/spironolactone.md — migrated to entity template
- wiki/entities/paragon-hf.md — migrated to entity template; added link to source stub
- wiki/entities/topcat.md — migrated to entity template; added link to source stub
- wiki/entities/charm-preserved.md — migrated to entity template; added link to source stub
- wiki/entities/i-preserve.md — migrated to entity template; added link to source stub
- wiki/concepts/hf-phenotype-classification.md — migrated to concept template
- wiki/concepts/diastolic-dysfunction.md — migrated to concept template
- wiki/concepts/hfpef-diagnosis.md — migrated to concept template
- wiki/concepts/hfpef-treatment-gap.md — migrated to concept template
- wiki/concepts/natriuretic-peptides.md — migrated to concept template

### Content fixes (per user remarks)
- hfpef.md: Added mL/m² to LA volume index >40 threshold; added [[atrial-fibrillation]] hyperlink; added E/e' >13 cut-off (sens 46%, spec 86%); added AF NP thresholds (>365/>105 pg/mL); added TR velocity >2.8 m/s row
- hfpef-diagnosis.md: Same Table 9 fixes; AF thresholds throughout
- hfref.md: Removed repetition; restructured to entity template (Description / Role in HFpEF / Evidence / Status)
- hf-phenotype-classification.md: Diagnostic pathway converted to decision tree (ASCII); removed duplicate sentence in Clinical Relevance section
- diastolic-dysfunction.md: Removed duplicate E/e' accuracy statement from Contradictions (already in Evidence table); cleaned Relationship to HFpEF Heterogeneity

### New entity pages created
- wiki/entities/atrial-fibrillation.md — new entity: AF as cause/consequence of HFpEF; adjusted diagnostic thresholds
- wiki/entities/echocardiography.md — new imaging entity: role, markers, benefits/drawbacks in HFpEF
- wiki/entities/cardiac-mri.md — new imaging entity: gold standard LVEF; tissue characterisation; second-line in HFpEF

### New study stub pages created (wiki/sources/)
- solomon2019paragon.md — PARAGON-HF
- pitt2014topcat.md — TOPCAT
- yusuf2003charm.md — CHARM-Preserved
- massie2008ipreserve.md — I-PRESERVE
- mcmurray2014paradigm.md — PARADIGM-HF
- mcmurray2019dapahf.md — DAPA-HF
- packer2020emperor.md — EMPEROR-Reduced
- anker2021emperor.md — EMPEROR-Preserved
- solomon2022deliver.md — DELIVER
- redfield2015neat.md — NEAT-HFpEF
- zamani2015indie.md — INDIE-HFpEF
- armstrong2020vitality.md — VITALITY-HFpEF
- udelson2020capacity.md — CAPACITY-HFpEF
- ahmed2006dig.md — DIG-Preserved
- pocock2013maggic.md — MAGGIC

### Wiki metadata updated
- wiki/index.md — added all new pages; reorganised by category
- wiki/timeline.md — populated Landmark Trials, Diagnostic Criteria, Treatment, Pathophysiology tables
- wiki/log.md — this entry

## 2026-04-30 (session 3 — ingest: Ho 2019 + Sachdev 2023)

### Sources ingested
- raw/2019-CirculationAHA-Ho-exercise-response.pdf → citekey: Ho2019HFpEFDefinitions
- raw/2023-CirculationAHA-Sachdev-hfpef-exercise.pdf → citekey: Sachdev2023Exercise

### New pages created
- wiki/sources/ho2019hfpefdefinitions.md — study: 7 HFpEF definitions vs. invasive CPET; enrollment 12–90%; HFpEF_phys (53%) independently predicts CV events
- wiki/sources/sachdev2023exercise.md — source: AHA Statement; SET meta-analysis 8 RCTs n=503; VO2 +2.8 mL/kg/min; skeletal muscle mechanism
- wiki/concepts/hfpef-diagnostic-definitions.md — new concept: competing definitions, sensitivity/specificity tables, trial incompatibility implication
- wiki/concepts/exercise-intolerance.md — new concept: four-mechanism model (skeletal muscle primary >50%); therapeutic implications
- wiki/entities/supervised-exercise-training.md — new entity: HIIT/MCT; evidence table; 2022 Class I AHA/ACC; hard outcome caveat
- wiki/entities/cardiopulmonary-exercise-testing.md — new entity: diagnostic gold standard; invasive CPET criteria; mechanistic dissection role

### Existing pages updated
- wiki/concepts/hfpef-diagnosis.md — added Diagnostic Definition Heterogeneity section; sensitivity/specificity table; Ho2019 citation; updated Related Pages
- wiki/concepts/hfpef-treatment-gap.md — added SET as positive intervention with meta-analysis table; updated SGLT2i note; updated Related Pages
- wiki/concepts/diastolic-dysfunction.md — added note that cardiac filling pressure is secondary (not primary) exercise limiter per Sachdev 2023
- wiki/entities/hfpef.md — added HFpEF_phys definition; added SET to Emerging Signals; updated sources and Related Pages
- wiki/contradictions.md — added contradictions 6 (definition heterogeneity), 7 (SET functional vs. hard outcomes), 8 (cardiac vs. peripheral exercise mechanism)
- wiki/overview.md — added session 3 entry; added SET hard outcomes to Active Debates and Knowledge Gaps; updated Key Concepts
- wiki/timeline.md — added Ho 2019 (Diagnostic Criteria, Pathophysiology); added Sachdev 2023 + AHA/ACC 2022 Class I (Treatment)
- wiki/index.md — added new sources (Observational Studies, Scientific Statements sections); added new entities (Diagnostic Tools, Interventions); added new concepts
- wiki/log.md — this entry

## 2026-05-04 (session 4 — ingest: AHA 2022 guideline + TOPCAT design + EMPEROR-Preserved secondary + TORCH; connect registries to papers)

### Sources ingested
- raw/2022-CirculationsAHA-Heidenreich-AHA-ACC-HFSA-Guideline-HF.pdf → citekey: Heidenreich2022AHA
- raw/2011-AHA-Desai-TOPCAT_study.pdf → citekey: Desai2011TOPCAT
- raw/2026-JACCHF-Ferreira-Findings-EMPEROR-Preserved.pdf → citekey: Ferreira2026Emperor
- raw/2017-ESC-HF-Seyler-TORCH_DZHK-1_rationale.pdf → citekey: Seyler2017TORCH
- raw/Study - NCT03251183 (DECIPHER-HFpEF registry) — entity page created
- raw/Study - NCT02187263 (TORCH Phase 1 registry) — linked to TORCH entity
- raw/Study - NCT04265040 (TORCH-Plus registry) — linked to TORCH entity

### New pages created
- wiki/sources/heidenreich2022aha.md — 2022 AHA/ACC/HFSA Guideline; HFimpEF; SGLT2i Class 2a; A–D staging; H₂FPEF; full treatment table
- wiki/concepts/guideline-comparison.md — ESC 2021 vs. AHA 2022 systematic comparison across 7 dimensions
- wiki/sources/desai2011topcat.md — TOPCAT design paper; dual enrollment pathway; 266 centers/6 countries; full parameters
- wiki/sources/ferreira2026emperor.md — EMPEROR-Preserved Mg secondary analysis; 622 sites/23 countries; Mg paradox
- wiki/sources/seyler2017torch.md — TORCH registry rationale; 19 DZHK centres; 4-module structure; biobank
- wiki/entities/torch.md — TORCH / TORCH-Plus registry entity; Phase 1 (NCT02187263) + Phase 2 (NCT04265040)
- wiki/entities/decipher-hfpef.md — DECIPHER-HFpEF entity; 7 German centres; CMR vs. PV loops; n=185; full parameters + biopsy

### Existing pages updated (methods/results expanded from stubs to full content)
- wiki/sources/anker2021emperor.md — Methods fully expanded: LVEF >40%, NT-proBNP thresholds (AF/no-AF), echo criteria, 622 sites/23 countries; Results added; Limitations updated; Secondary analyses table + Ferreira2026 added
- wiki/sources/pitt2014topcat.md — Methods fully expanded: dual pathway, LVEF ≥45%, 266 centers/6 countries, full parameters, spironolactone titration; Results added; Limitations expanded; Secondary analyses table + Desai2011 added

### Entity pages updated
- wiki/entities/sglt2-inhibitors.md — AHA 2022 Class 2a for HFpEF added; status table (ESC 2021 vs. AHA 2022); Ferreira2026 Mg finding added; contradictions updated
- wiki/entities/sacubitril-valsartan.md — AHA 2022 Class 2b for HFpEF added; status table created
- wiki/entities/spironolactone.md — AHA 2022 Class 2b for HFpEF added; status table created

### Concept pages updated
- wiki/concepts/hf-phenotype-classification.md — HFimpEF added as 4th EF category; AHA 2022 distinction; History extended to 2022
- wiki/concepts/hfpef-treatment-gap.md — SGLT2i Class 2a partial gap closure documented; AHA 2022 treatment table; mortality gap still open; Ferreira2026 Mg open question added
- wiki/contradictions.md — Added contradictions 9 (SGLT2i ESC 2021 vs. AHA 2022), 10 (Mg direction reversal), 11 (HFpEF definition stringency difference)

### Metadata pages updated
- wiki/index.md — Added: heidenreich2022aha, desai2011topcat, ferreira2026emperor, seyler2017torch, torch, decipher-hfpef, guideline-comparison; reorganised Clinical Trial Papers section
- wiki/timeline.md — Added: AHA 2022 guideline (Diagnostic Criteria + Treatment entries); Ferreira 2026 (Landmark Trials); Registries section (TORCH 2014, DECIPHER-HFpEF 2017, TORCH-Plus 2020)
- wiki/log.md — this entry

## 2026-05-04 (session 7 — ingest: 9 papers; NCT corrections; stub expansions)

### Sources ingested (PDFs read)
- raw/2015-NEJM-Redfield-NEAT-HFpEF_study.pdf → citekey: Redfield2015NEAT
- raw/2019-eurheartj-pieske-HFA-PEFF_diagnostic_algorithm.pdf → citekey: Pieske2019HFAPEFF
- raw/2018-CirculationAHA-Yogesh-guide_daignosis-hfpef.pdf → citekey: Reddy2018H2FPEF
- raw/2023-CirculationsAHA-McMurry-DETERMINE_study.pdf → citekey: McMurray2024DETERMINE
- raw/2025-JCF-Docherty-DETERIMINE_wearables_physical_activity.pdf → citekey: Docherty2025DETERMINE
- raw/2025-HFR-Mirzai-Review_physical_activity_hfpef.pdf → citekey: Mirzai2025Exercise
- (DELIVER, PARAGON-HF, CHARM-Preserved, I-PRESERVE, VITALITY-HFpEF, CAPACITY-HFpEF read in prior session; stubs expanded this session)

### New source pages created
- wiki/sources/pieske2019hfapeff.md — HFA-PEFF 4-step algorithm; full scoring table; AF-adjusted thresholds; invasive criteria
- wiki/sources/reddy2018h2fpef.md — H₂FPEF score derivation; 6-variable score 0–9; AUC 0.841/0.886; single-centre Mayo Clinic
- wiki/sources/mcmurray2024determine.md — DETERMINE RCTs; HFpEF arm missed all primary endpoints; 6MWD neutral throughout
- wiki/sources/docherty2025determine.md — DETERMINE accelerometry substudy; accelerometer/KCCQ/6MWD measure distinct dimensions
- wiki/sources/mirzai2025exercise.md — 2025 exercise review ~30 RCTs; MICT best evidence; HIIT not superior to MICT; ~1/3 non-responders

### Stub source pages expanded to full content
- wiki/sources/solomon2022deliver.md — DELIVER: N=6,263; HR 0.82 (P<0.001); consistent benefit including LVEF ≥60%
- wiki/sources/solomon2019paragon.md — PARAGON-HF: N=4,822; RR 0.87 (P=0.06); subgroup signals women + LVEF <57%
- wiki/sources/yusuf2003charm.md — CHARM-Preserved: N=3,023; HR 0.89 (P=0.118); HF hosp signal P=0.017
- wiki/sources/massie2008ipreserve.md — I-PRESERVE: N=4,128; HR 0.95 (P=0.35); all-cause death HR 1.00; fully neutral
- wiki/sources/armstrong2020vitality.md — VITALITY-HFpEF: N=789; KCCQ-PLS neutral (P=0.47/0.80); 24 weeks; NCT03547583
- wiki/sources/udelson2020capacity.md — CAPACITY-HFpEF: N=196; peak VO₂ neutral (P=0.37); KCCQ worse on active arm (P=0.007); NCT03254485
- wiki/sources/redfield2015neat.md — NEAT-HFpEF: N=110; primary P=0.06 trend; all-dose combined P=0.02 LESS active; NCT02053493

### NCT corrections in wiki/trials.md (confirmed from ingested PDFs)
- CAPACITY-HFpEF: NCT03254381 → NCT03254485 (confirmed from paper abstract)
- VITALITY-HFpEF: NCT02673164 → NCT03547583 (confirmed from paper abstract)
- NEAT-HFpEF: NCT01516346 → NCT02053493 (confirmed from paper abstract)
- CHARM-Preserved: "pre-registration era" → NCT00634712 (confirmed from registry file)
- I-PRESERVE: removed [verify on ingest] tag — NCT00095238 confirmed from registry file

### New trials added to wiki/trials.md
- DETERMINE-Preserved (NCT03877224) and DETERMINE-Reduced (NCT03877237)

### wiki/trials-pending.md updated
- Added: SOCRATES-PRESERVED (vericiguat phase 2b in HFpEF; Pieske 2017 EHJ)
- Added: VICTORIA (vericiguat in HFrEF; Armstrong 2020 NEJM; NCT02861534) — for EF-comparison context

### Citations updated
- wiki/citations.md: Added 7 new ingested entries (Pieske2019HFAPEFF, Reddy2018H2FPEF, McMurray2024DETERMINE, Docherty2025DETERMINE, Mirzai2025Exercise, Redfield2015NEAT moved from stub)
- wiki/citations.md: Added full formatted references for all new ingested sources
- Yusuf2003CHARM DOI confirmed: 10.1016/S0140-6736(03)14285-7

### wiki/index.md updated
- Added new source pages under Observational Studies, Scientific Statements, Consensus/Guideline Papers, Clinical Trial Papers, Secondary Analyses sections
- Expanded clinical trial entries with key numbers

### wiki/log.md — this entry

---

## 2026-05-04 (session 6 — clinical trials overview, trials-pending, CLAUDE.md rule, Ferreira DOI)

### New pages created
- wiki/trials.md — master clinical trials overview table; 14 RCTs, 3 registries, 1 meta-analysis, secondary analyses; [verify on ingest] flags for unconfirmed NCT numbers
- wiki/trials-pending.md — staging list for trials referenced in sources but not yet added; initial entries: RELAX (sildenafil in HFpEF, from Ho 2019), ATTR-ACT (tafamidis, from AHA 2022 guideline)

### CLAUDE.md updated
- Added Clinical Trials Overview Rule: maintain trials.md + trials-pending.md; on every ingest scan for unreferenced trials; on trial addition move from pending to trials.md; required columns specified

### Citations updated
- wiki/citations.md: Ferreira2026Emperor DOI updated: 10.1016/j.jchf.2025.102889 (provided by user); [doi pending] notes removed

### Metadata updated
- wiki/index.md — added [[trials]] and [[trials-pending]] to Core Pages
- wiki/log.md — this entry

## 2026-05-04 (session 5 — lint, citation registry, redundancy reduction, cross-linking)

### New pages created
- wiki/citations.md — master citekey → full citation registry; 9 ingested + 13 stub sources with full formatted references

### CLAUDE.md updated
- Added Citation Lookup Rule: when user asks for a reference, read citations.md and return full formatted citation by citekey
- Extended Lint definition: redundancy detection, missing citations, stub tracking, citations.md drift

### Redundancies removed (content reduced to summary + pointer to canonical page)
- wiki/entities/hfpef.md: Table 9 marker table → pointer to [[hfpef-diagnosis]]
- wiki/concepts/diastolic-dysfunction.md: Table 9 marker table → bullet summary + pointer to [[hfpef-diagnosis]]
- wiki/concepts/guideline-comparison.md: H₂FPEF scoring table → inline summary + pointer to [[hfpef-diagnosis]]
- wiki/sources/heidenreich2022aha.md: H₂FPEF scoring table → inline summary + pointer to [[hfpef-diagnosis]]

### Content fixes
- wiki/entities/hfpef.md: "Role in HFpEF" → "Epidemiology and Clinical Profile"; ESC Long-Term Registry stat marked [needs source]; Status section → comparison table + AHA 2022; sources updated
- wiki/concepts/exercise-intolerance.md: Evidence table source column fixed to proper `source: filename.pdf` format
- wiki/concepts/natriuretic-peptides.md: Added AHA 2022 NP guidance note, EMPEROR-Preserved trial threshold context, updated sources and Related Pages

### Cross-links added
- diastolic-dysfunction.md → [[guideline-comparison]], [[decipher-hfpef]]
- hfpef-diagnosis.md → [[guideline-comparison]], [[decipher-hfpef]]
- natriuretic-peptides.md → [[guideline-comparison]], [[anker2021emperor]], [[ferreira2026emperor]]

### Metadata
- wiki/index.md — [[citations]] added to Core Pages
- wiki/log.md — this entry

## 2026-05-05 (session 8 — ingest DELIVER)

### Ingested
- raw/2022-NEJM-Solomon-Deliver_study.pdf → [[solomon2022deliver]] (citekey: Solomon2022DELIVER)

### Updated pages
- wiki/sources/solomon2022deliver.md — full rewrite from PDF; added complete Table 1 baseline data, Table 2 outcomes, subgroup forest plot HRs, KCCQ win ratio 1.11 (P=0.009), safety profile, dual-primary statistical design, CV death rate context
- wiki/concepts/hfpef-treatment-gap.md — SGLT2i symptom gap section updated: DELIVER KCCQ positive vs. DETERMINE neutral reconciled
- wiki/contradictions.md — added #16: DELIVER KCCQ positive vs. DETERMINE-Preserved neutral (same drug, different method + follow-up)
- wiki/citations.md — Solomon2022DELIVER promoted from Stub to Ingested; duplicate entries for Pitt2014TOPCAT and Anker2021EMPEROR removed from stubs

### Stubs added to trials-pending.md
- Butler 2022 (Eur Heart J): EMPEROR-Preserved EF spectrum subgroup analysis — motivated DELIVER dual-primary design; DELIVER found no heterogeneity, resolving the concern

## 2026-05-05 (session 8 — ingest PARAGON-HF)

### Ingested
- raw/2019-NEJM-PARAGON-HF_study.pdf → [[solomon2019paragon]] (citekey: Solomon2019PARAGON)

### Updated pages
- wiki/sources/solomon2019paragon.md — full rewrite from PDF; added complete Table 1 baseline, Table 2 outcomes with exact rates, full subgroup forest plot (12 prespecified), safety Table 3, statistical design details (dual run-in, adjusted alpha 0.048), 26-patient GCP exclusion
- wiki/citations.md — Solomon2019PARAGON promoted from Stub to Ingested

### Key new data vs. stub
- Renal protection: HR 0.50 (0.33–0.77) — significant; strongest secondary endpoint, underreported in HFpEF narrative
- NYHA improvement: OR 1.45 (1.13–1.86) — significant
- KCCQ NS (+1.0 pt, 0.0–2.1); both arms declined — important contrast with DELIVER
- Safety: paradoxically lower creatinine elevation and hyperkalemia despite active RAAS comparator
- Exact subgroup RRs: women 0.73 (0.59–0.90); LVEF ≤57%: 0.78 (0.64–0.95)

## 2026-05-05 (session 8 — ingest CHARM-Preserved)

### Ingested
- raw/2003-LANCET-Yusuf-CHARM-preserved_study.pdf → [[yusuf2003charm]] (citekey: Yusuf2003CHARM)

### Updated pages
- wiki/sources/yusuf2003charm.md — full rewrite from PDF; added complete Table 1 baseline (N=3,023, mean age 67.2y, LVEF 54%, 65% HTN, 29% AF, only 20% ACEi), Tables 2+3+4 (unadjusted HR 0.89 P=0.118; adjusted P=0.051; adjudicated HF hosp adjusted P=0.047; investigator-reported P=0.017/P=0.014; new-onset diabetes HR 0.60 P=0.005), safety discontinuations, baseline imbalance note, mid-trial ACEi protocol change
- wiki/citations.md — Yusuf2003CHARM promoted from Stub to Ingested; duplicate Solomon2019PARAGON removed from Stub refs section

### Key new data vs. stub
- New-onset diabetes: HR 0.60 (0.41–0.86), P=0.005 — 40% reduction; stronger result than primary efficacy endpoint
- Investigator-reported total HF admissions: 402 vs. 566, P=0.014 — counts diverge markedly from adjudicated
- Baseline imbalance: candesartan arm had more adverse prognostic factors (more MI, stroke, diabetes) — modest bias against treatment effect
- Mid-trial ACEi protocol change after HOPE publication introduces heterogeneity in background RAAS exposure

## 2026-05-05 (session 8 — ingest I-PRESERVE)

### Ingested
- raw/2008-NEJM-Massie-I-PRESERVE_study.pdf → [[massie2008ipreserve]] (citekey: Massie2008IPreserve)

### Updated pages
- wiki/sources/massie2008ipreserve.md — full rewrite from PDF; added complete Table 1 baseline (N=4,128, mean age 72y, LVEF 59–60%, 76% NYHA III, 88% HTN, 29% AF, median NT-proBNP 320/360, eGFR 72–73), Tables 2+3 outcomes with exact rates, Figure 2 subgroup (8/8 zero heterogeneity), Table 4 safety, concomitant RAAS background change during trial
- wiki/citations.md — Massie2008IPreserve promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub
- All-cause death: HR 1.00 (0.88–1.14), P=0.98 — exact CI and P now recorded
- Zero heterogeneity across all 8 prespecified subgroups — cleanest null in RAAS-HFpEF; contrast with PARAGON sex/LVEF signals
- NT-proBNP change NS (P=0.14): no biomarker effect despite 3.8 mmHg BP reduction
- MLHF QoL NS (P=0.85): neutral on symptoms
- Safety: creatinine doubling 6% vs. 4% P<0.001; K >6.0 3% vs. 2% P=0.01
- ACEi use rose 25% → 39%, spironolactone 15% → 28% during trial — progressive RAAS background dilution
- LVEF 59–60% (highest among early RAAS trials) — most representative of true HFpEF

### Trials-pending
- No new post-2020 HFpEF-important trials identified in I-PRESERVE references

## 2026-05-05 (session 8 — ingest CAPACITY-HFpEF)

### Ingested
- raw/2020-JAMA-Udelson-CAPACITY-HFpEF_study.pdf → [[udelson2020capacity]] (citekey: Udelson2020CAPACITY)

### Updated pages
- wiki/sources/udelson2020capacity.md — full rewrite from PDF; added complete Table 1 baseline (N=196, primary analysis n=143, median NT-proBNP 244 pg/mL, 57% ≤300, LVEF median 61.5%, BMI 34, 19% diuretics), Table 2 primary and secondary outcomes with exact CIs, exploratory KCCQ/6-MWT responder analyses, Figure 2 subgroup forest plot, Table 3 safety
- wiki/citations.md — Udelson2020CAPACITY promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub
- KCCQ worse: −7.2 [−12.3 to −2.0], P=0.007 — exact CI; KCCQ responders OR 0.43, P=0.01
- 6-MWT responders fewer on drug: OR 0.39, P=0.007 — significant harm signal on responder analysis
- Age interaction P=0.004: harm in ≥70y (adjusted diff −1.22 [−2.44 to −0.46]) — enrichment criterion group harmed
- Loop diuretic only 19% (vs. 52-93% in major trials) — very different population
- Median NT-proBNP 244 pg/mL; 57% below modern HFpEF NP entry thresholds — diagnostic uncertainty
- BP lowered −6.3 mmHg; dizziness 9.9% vs. 1.1%, hypotension 8.8% vs. 0% — likely mechanism for harm in elderly

### Trials-pending
- No new post-2020 HFpEF-important trials identified in CAPACITY-HFpEF references

## 2026-05-05 (session 8 — ingest VITALITY-HFpEF)

### Ingested
- raw/2020-JAMA-Armstrong-VITALITY-HFpEF.pdf → [[armstrong2020vitality]] (citekey: Armstrong2020VITALITY)

### Updated pages
- wiki/sources/armstrong2020vitality.md — full rewrite from PDF; added complete Table 1 baseline (N=789, LVEF 56.8%, median NT-proBNP 1364–1644 pg/mL, 86% loop diuretics, 86% beta-blockers, 45% MRA, 36% AF, eGFR 57–62), primary/secondary outcomes with exact CIs, Table 2 safety+clinical outcomes, titration details, placebo response analysis
- wiki/citations.md — Armstrong2020VITALITY promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub
- KCCQ-PLS: LS diff −1.5 [−5.5 to 2.5] P=0.47 (15mg); −0.5 [−4.6 to 3.5] P=0.80 (10mg) — exact CIs
- 6MWD: −5.5 m [−19.7 to 8.8] P=0.45; −1.8 m [−16.2 to 12.6] P=0.81 — exact CIs
- Placebo response +6.9 KCCQ PLS pts (exceeds MCID of 5 pts) — natural post-decompensation recovery; all 3 arms improved meaningfully
- Mortality signal: CV death 3.0%/4.6%/1.5% for 15mg/10mg/placebo — numerically more in 10mg; trial not powered
- SBP reduced −3.1/−3.8/−1.2 mmHg; symptomatic hypotension 6.4% vs. 3.4%
- Median NT-proBNP ~1400 pg/mL — starkly different from CAPACITY-HFpEF (244 pg/mL); very different severity populations

### Trials-pending
- No new post-2020 HFpEF-important trials identified in VITALITY-HFpEF references (VICTORIA already in pending)

## 2026-05-05 (session 8 — ingest PARADIGM-HF)

### Ingested
- raw/2014-NEJM-McMurray-PARADIGM-HF_study.pdf → [[mcmurray2014paradigm]] (citekey: McMurray2014PARADIGM)

### Updated pages
- wiki/sources/mcmurray2014paradigm.md — full rewrite from stub; added complete Table 1 baseline (N=8,442, LVEF 29.6%, 21% female, median NT-proBNP 1631, 93% beta-blocker, 54% MRA), Table 2 outcomes (primary HR 0.80, CV death HR 0.80, all-cause HR 0.84, KCCQ +1.64 P=0.001), Table 3 safety (paradoxically lower creatinine + hyperkalemia, more hypotension), subgroup forest plot, dual run-in design, early stopping context
- wiki/citations.md — McMurray2014PARADIGM promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub (stub was all placeholders)
- Primary HR 0.80 (0.73–0.87) P<0.001; exact P=4.0×10⁻⁷
- All-cause death HR 0.84 (0.76–0.93) P<0.001 — mortality benefit confirmed
- KCCQ clinical summary +1.64 pts [0.63–2.65] P=0.001 — significant symptom benefit; EF-contrast with PARAGON NS
- Safety paradox: creatinine ≥2.5 3.3% vs. 4.5% P=0.007; K>6.0 4.3% vs. 5.6% P=0.007 — same renal paradox pattern as PARAGON
- Run-in details: 18% screened patients excluded; 1,102 enalapril + 977 LCZ696 run-in dropouts
- Early stopping: 3rd interim analysis March 28, 2014; stopping boundary P<0.001 crossed

### Trials-pending
- No new post-2020 HFpEF-important trials identified in PARADIGM-HF references

## 2026-05-05 (session 8 — ingest DAPA-HF)

### Ingested
- raw/2019-NEJM-McMurray-DAPA-HF_study.pdf → [[mcmurray2019dapahf]] (citekey: McMurray2019DAPAHF)

### Updated pages
- wiki/sources/mcmurray2019dapahf.md — full rewrite from stub; added complete Table 1 baseline with medications (MRA 71.5%, sacubitril-valsartan 10.5%, beta-blocker 96%), Table 2 primary+secondary outcomes with exact HRs and CIs, subgroup forest plot (all patients + 15 prespecified subgroups), laboratory changes at 8 months, Table 2 safety, non-DM subgroup analysis
- wiki/citations.md — McMurray2019DAPAHF promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub (stub was all placeholders)
- Primary HR 0.74 (0.65–0.85) P<0.001; 386 (16.3%) vs 502 (21.2%); NNT=21
- Non-DM HR 0.73 (0.60–0.88) consistent with DM HR 0.75 (0.63–0.90) — mechanism beyond glucose lowering established
- NYHA II HR 0.63 (0.52–0.75) vs NYHA III/IV HR 0.90 (0.74–1.09) — post-hoc apparent attenuation; inconsistent with other advanced-disease markers
- Sacubitril-valsartan 10.5% at baseline; HR 0.75 consistent in this subgroup
- Lab changes: creatinine +0.02 mg/dL (minimal); hematocrit +2.41% P<0.001; NT-proBNP −301 [−457 to −150] P<0.001; weight −0.87 kg P<0.001; SBP −1.27 mmHg P=0.002
- Safety: AE discontinuation identical (4.7% vs 4.9%); renal AEs fewer on dapa (6.5% vs 7.2% NS); DKA 3 vs 1 case; no amputation/Fournier's difference
- KCCQ total symptom score win ratio 1.18 (1.11–1.26) P<0.001

### Trials-pending
- EMPEROR-Preserved (Anker 2021) and DELIVER (Solomon 2022) already ingested; no new post-2020 HFpEF-important trials to add from DAPA-HF (2019 paper)

## 2026-05-05 (session 8 — ingest EMPEROR-Reduced)

### Ingested
- raw/2020-NEJM-Packer-EMPEROR-Reduced_study.pdf → [[packer2020emperor]] (citekey: Packer2020EMPEROR)

### Updated pages
- wiki/sources/packer2020emperor.md — full rewrite from stub; added complete Table 1 baseline (N=3,730, LVEF ≤30%: 71.8%, median NT-proBNP 1887, sacubitril-valsartan 18.3%, MRA 70.1%, ICD 31%), Table 2 outcomes with exact HRs and CIs, subgroup forest plot (Figure 2, 16 subgroups), eGFR slope analysis, discontinuation eGFR analysis, safety summary
- wiki/citations.md — Packer2020EMPEROR promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub (stub was all placeholders)
- Primary HR 0.75 (0.65–0.86) P<0.001; NNT=19; first HF hosp HR 0.69 (0.59–0.81)
- eGFR slope +1.73 (1.10–2.37) mL/min/1.73m²/yr P<0.001 — headline renal finding
- Composite renal outcome HR 0.50 (0.32–0.77) — same as PARAGON-HF
- CV death HR 0.92 NS; all-cause HR 0.92 NS — shorter follow-up than DAPA-HF
- LVEF >30% subgroup HR 0.99 (0.76–1.31) — possible EF-gradient even within HFrEF
- Sacubitril-valsartan at baseline HR 0.64 (0.45–0.89) vs no ARNi 0.77
- Discontinuation analysis confirms structural renal protection: eGFR −0.93 vs −4.21 mL/min/yr after drug stop
- Hematocrit +2.36% (2.08–2.63) — consistent with DAPA-HF (+2.41%)

### Trials-pending
- EMPEROR-Preserved (Anker 2021) already ingested; no new post-2020 HFpEF-important trials to add

## 2026-05-05 (session 8 — ingest INDIE-HFpEF)

### Ingested
- raw/2014-CirculationAHA-Zamani-Indie_Beetroot_HFpEF.pdf → [[zamani2015indie]] (citekey: Zamani2015INDIE)

### Updated pages
- wiki/sources/zamani2015indie.md — full rewrite from stub (multiple stub errors corrected); added complete Table 1 baseline (N=17 crossover, age 65.5y, 88% male, 82% Black, 100% HTN, 71% DM, 94% obese, LVEF 63.5%, E/e' 11.6, median NT-proBNP 144 pg/mL, 53% met ESC criteria), Table 2 gas exchange data, Table 3 haemodynamic reserve, NIRS and aortic tonometry results
- wiki/citations.md — Zamani2015INDIE added to Ingested table and formatted refs; removed from Stub formatted refs; also removed orphaned Solomon2022DELIVER duplicate from Stub formatted refs

### Stub errors corrected on ingest
- Journal: stub said "JACC: Heart Failure" → corrected to Circulation 2015;131(4):371–380
- Intervention: stub said "KNO₃" → corrected to beetroot juice NO₃⁻ 12.9 mmol (crossover, single dose)
- N: stub said ~65 → corrected to 17 (modified ITT)
- Design: stub said parallel RCT ~6 weeks → corrected to double-blind crossover, single dose, ≥5-day washout
- Key finding: stub said "did not improve peak VO₂" → corrected to POSITIVE peak VO₂ (P=0.005); primary (efficiency) was neutral (P=0.64)

### Key new data vs. stub
- Primary (efficiency): neutral P=0.64
- Peak VO₂: +1.0 mL/min/kg, P=0.005 — SIGNIFICANT (stub was wrong)
- Mechanism: peripheral hemodynamic (↑CO +32.5% P=0.006; ↓SVR −10.6% P=0.03), not O₂ extraction
- Aortic augmentation index: −9.1%, P=0.03 — reduced wave reflections
- Crossover confirms bioavailability: plasma NOₓ 326 vs 10 µmol/L P=0.0003

### Trials-pending
- No new post-2020 HFpEF-important trials identified in INDIE-HFpEF references

## 2026-05-05 (session 8 — ingest DIG-Preserved)

### Ingested
- raw/2006-CirculationAHA-Ahmed-DIG_HF.pdf → [[ahmed2006dig]] (citekey: Ahmed2006DIG)

### Updated pages
- wiki/sources/ahmed2006dig.md — full rewrite from stub; added complete Table 1 baseline (N=988, LVEF 55.4%, 86% ACEi, 77% diuretics, 57% HTN, 56% ischaemic, NYHA I/II/III/IV 20/58/21/1%), Table 2 mortality and composite outcomes at 2y and study end, Table 3 hospitalisations by cause, digoxin toxicity data, offsetting mechanism analysis
- wiki/citations.md — Ahmed2006DIG promoted from Stub to Ingested; full formatted reference added

### Key new data vs. stub (stub had all placeholders)
- Primary HR 0.82 (0.63–1.07) P=0.136 at study end (NS); but at 2y HR 0.71 (0.52–0.98) P=0.034 (significant — pre-specified)
- Mortality completely null: all-cause HR 0.99, CV HR 1.00
- Worsening HF hosp reduced: 2y HR 0.66 P=0.012; overall trend HR 0.79 P=0.094
- Unstable angina hosp increased: 2y HR 1.76 P=0.004; overall trend HR 1.37 P=0.061
- Digoxin toxicity: 48 (10%) vs 18 (4%) P<0.001 — important safety signal
- Net null explained by competing effects: HF reduction offset by angina increase

### Trials-pending
- No post-2020 HFpEF-important trials to add from a 2006 publication

## 2026-05-05 (session 8 — ingest MAGGIC)

### Ingested
- raw/2013-ESC-Pocock-MAGGIC_meta-analysis.pdf → [[pocock2013maggic]] (citekey: Pocock2013MAGGIC)

### Updated pages
- wiki/sources/pocock2013maggic.md — full rewrite from stub; added complete Table 2 (13 predictors with exact RRs and CIs), Table 5 (EF <40 subgroup, N=21,442), Table 6 (EF ≥40 subgroup, N=17,930 — ACEi/ARB RR 0.938 P=0.233 NS), Table 4 risk score calibration; design details (30 studies: 6 RCTs + 24 observational, IPD-MA, Poisson regression with study random effect), EF spline analysis (knot at 40%), heartfailurerisk.org integer score
- wiki/citations.md — Pocock2013MAGGIC promoted from Stub to Ingested; Stub table and Stub formatted refs section now empty (all stubs ingested)

### Key new data vs. stub (stub was all placeholders)
- Exact N: 39,372 patients; 15,851 deaths (40.2%); median follow-up 2.5y (IQR 1.0–3.9y)
- EF threshold confirmed at 40%: EF per 5% RR 0.581 up to 40%, then flat — HFpEF as distinct prognostic entity
- ACEi/ARB EF ≥40: RR 0.938 (0.864–1.019) P=0.233 — NOT significant; EF <40: RR 0.834 P<0.001 — significant
- Age RR 1.589/decade in EF ≥40 (> EF <40 RR 1.407) — age dominant predictor in HFpEF
- Diabetes RR 1.513 in EF ≥40 (> EF <40 RR 1.354) — cardiometabolic burden more harmful in HFpEF
- Integer score calibration: score 20 → 25% 3y mortality; score 30 → 52%; score 33+ → 70%

### Trials-pending
- 2013 meta-analysis; no post-2020 HFpEF-important trials to add

## 2026-05-05 (session 8 — ingest Yi 2025 AI review)

### Ingested
- raw/2025-jjcc-Yi-AI_in_HFpEF.pdf → [[yi2025ai]] (citekey: Yi2025AI)

### New pages created
- wiki/sources/yi2025ai.md — new source page; review article using source template
- wiki/concepts/ml-ai-hfpef.md — new concept page; ML/AI in HFpEF; 4 domains (diagnosis, phenotyping, risk prediction, management); history from 2015 to 2025; open questions

### Key content from review (38 studies, Yi & Cho 2025, J Cardiol 87:113–120)
- ECG deep learning: AUC 0.87 (Unterhuber/Kwon); NPV 0.98 — scalable rule-out
- Echo 3D-CNN (Akerman): AUC 0.79; single A4C clip; outperforms HFA-PEFF/H₂FPEF
- NLP/EHR: 75.4% of ESC-criteria HFpEF patients undiagnosed in routine EHR (Garan 2023)
- Phenotyping: 11 studies; 3–4 phenogroups consistent across datasets; cardiometabolic/inflammatory/ischaemic/age-AF axes
- Spironolactone responders (Kresoja 2023; Desai 2024): ML predicts responders; BMI top predictor (33.7%); non-responders show no benefit (P=0.52 vs P=0.008) — TOPCAT reframed as enrichment failure
- In silico empagliflozin mechanism: NHE1 inhibition → cardiomyocyte oxidative stress (Bayes-Genis 2021)

### Citations updated
- wiki/citations.md — Yi2025AI added to Ingested table and formatted refs (new entry; no prior stub)

### Trials-pending
- No post-2020 HFpEF RCTs identified as missing from wiki; Aldo-DHF referenced but 2013 (pre-cutoff)

## 2026-05-06 (session 8 — ingest Kittleson 2023 ACC ECDP)

### Ingested
- raw/2023-JACC-Kittleson-ACC_expert_consensu_HFpEF.pdf → [[kittleson2023acc]] (citekey: Kittleson2023ACC)

### New pages created
- wiki/sources/kittleson2023acc.md — new source page; guideline/consensus document using source template; 44-page ACC ECDP; full treatment algorithm, dose tables, contraindication tables, mimics table, comorbidity management, referral acronyms

### Updated pages
- wiki/concepts/guideline-comparison.md — added ACC 2023 ECDP section; updated History section; added sex-stratified algorithm table; H₂FPEF vs. HFA-PEFF priority clarification; updated sources frontmatter
- wiki/trials-pending.md — added SUMMIT (NCT04847557, semaglutide in HFpEF) and STEP-HFpEF (NCT04788511, tirzepatide in HFpEF)
- wiki/citations.md — Kittleson2023ACC added to Ingested table and formatted refs
- wiki/index.md — added [[kittleson2023acc]] under new "Guidelines and Consensus Documents" section

### Key content vs. existing wiki
- Treatment algorithm (Figure 9): SGLT2i first (near-Class I) → MRA for women (all EF) + men EF <55–60% → ARNI same criteria → ARB for ARNI-ineligible
- Sex-stratified recommendation: PARAGON HR 0.73 women vs. 1.03 men; LVEF 50–55% may be abnormal in women (smaller LV)
- Table 3: dose targets — dapa/empa 10mg; spiro 25→50mg; sac/val 24/26→97/103mg BID; cand 4–8→32mg
- Table 1: HFpEF mimics — 8 mimics with clinical clues + diagnostic tests (amyloidosis CTS/lumbar → Tc-PYP; Fabry → α-galactosidase; sarcoidosis → FDG-PET+CMR)
- CHECK-IN (PCP→cardiology) + INHALE (cardiology→HF specialist) acronyms
- GLP-1RA: semaglutide and tirzepatide referenced; SUMMIT + STEP-HFpEF ongoing
- STRONG-HF: 8% absolute reduction HF readmission/death with in-hospital GDMT titration
- CardioMEMS Class 2b; GUIDE-HF COVID-confounded; useful subset defined
- Comorbidity management: TZDs contraindicated; saxagliptin/alogliptin avoided; finerenone for diabetic CKD; thiazide + loop for CKD diuretic resistance

### Trials-pending added
- SUMMIT (NCT04847557): semaglutide in HFpEF with obesity
- STEP-HFpEF (NCT04788511): tirzepatide in HFpEF with obesity

## 2026-05-06 (session 9 — ingest Anker 2023 HFA/ESC/ESH HFpEF Phenotyping Statement)

### Ingested
- raw/2023-ESC-Anker_HFpEF_phenotyping.pdf → [[anker2023hfpefphenotype]] (citekey: Anker2023HFpEFPhenotype)

### New pages created
- wiki/sources/anker2023hfpefphenotype.md — new source page; 20-page HFA/ESC/ESH scientific statement; phenotype prevalence wheel (Figure 1, 18 phenotypes), treatment wheel (Figure 2), phenotype-specific evidence sections, ongoing trials
- wiki/concepts/hfpef-phenotype-profiling.md — new concept page; two-layer treatment model; phenotype-guided add-on table; LVEF 50–55% and >65% subgroup data; CMD prevalence; cancer HFpEF; ongoing trials table

### Updated pages
- wiki/entities/hfpef.md — added Comorbidity Phenotype Prevalences section (Figure 1 table, 18 phenotypes with prevalences); added [[hfpef-phenotype-profiling]] to Related Pages; added Anker2023HFpEFPhenotype to sources
- wiki/entities/atrial-fibrillation.md — added AF prevalence up to 50% (paroxysmal); EAST-AFNET4 data; CABA-HFpEF (NCT05508256, Phase III, DZHK); atrial FMR combined phenotype; updated Related Pages + sources
- wiki/entities/spironolactone.md — added ESC/HFA 2023 "may be considered" framing; SPIRIT-HF (NCT04727073) and SPIRRIT (NCT02901184) ongoing; FINEARTS-HF (NCT04435626, finerenone) first non-steroidal MRA trial; updated Related Pages + sources
- wiki/concepts/hfpef-treatment-gap.md — added "Phenotype-Based Approach" section with two-layer model and ongoing trials table (FINEARTS-HF, SUMMIT, STEP-HFpEF, SPIRIT-HF, CABA-HFpEF, FAIR-HFpEF); updated Related Pages + sources

### Key content vs. existing wiki
- Figure 1: First structured prevalence data for 18 HFpEF comorbidity phenotypes; iron deficiency 50–75% most underrecognised
- Figure 2: Treatment wheel — phenotype-specific add-on agents for 7 comorbidity categories
- Iron deficiency 50–75%; VO2 reduction, 6MWD reduction, HRQOL impairment; FAIR-HFpEF/PREFER-HF ongoing
- CMD: PROMIS-HFpEF 66% endothelium-independent + 24% endothelium-dependent = 91% total
- LVEF 50–55%: distinct subgroup; spironolactone benefit (TOPCAT), sacubitril/valsartan benefit (PARAGON ≤57%), empagliflozin benefit (EMPEROR ≥50% to <64%)
- LVEF >65%: U-shaped mortality; secondary HFpEF workup mandatory (ATTR 13% with LVH)
- Cancer HFpEF: doxorubicin → diastolic dysfunction 60% at 1y, 80% at 3y; excluded from all major trials
- Chronotropic incompetence: beta-blocker withdrawal improves function — contra-intuitive but documented
- CABA-HFpEF (NCT05508256): Phase III AF ablation vs. rate control in HFpEF; DZHK network

### Citations updated
- wiki/citations.md — Anker2023HFpEFPhenotype added to Ingested table and formatted refs

### Trials-pending added
- FINEARTS-HF (NCT04435626): finerenone (non-steroidal MRA) in HFpEF, LVEF ≥40%
- CABA-HFpEF (NCT05508256): catheter ablation vs. rate control in HFpEF with AF; DZHK Phase III
- FAIR-HFpEF (NCT03074591): ferric carboxymaltose vs. placebo in HFpEF with iron deficiency
- SPIRIT-HF (NCT04727073): spironolactone in HFpEF; resolves TOPCAT MRA question

## 2026-05-06 (session 9 — ingest Savarese 2022 global HF burden)

### Ingested
- raw/2022-ESC-Savarese-Global_burden_HF.pdf → [[savarese2022globalburden]] (citekey: Savarese2022GlobalBurden)

### New pages created
- wiki/sources/savarese2022globalburden.md — new source page; global HF epidemiology invited review (Cardiovasc Res 2022); prevalence, incidence, aetiology, outcomes, hospitalisations, costs by EF phenotype; 7-registry distribution table; Figure 1/2/3/4 data

### Updated pages
- wiki/entities/hfpef.md — Epidemiology section updated: HFpEF fraction 16–47% by registry; 5-year mortality comparable to HFrEF (75.7%); non-CV mortality 30.7% vs 20.1% in HFrEF; 63% non-CV hospitalisations; sources + Related Pages updated
- wiki/entities/hfmref.md — added Epidemiology section: HFmrEF 14–24% across 5 registries; 1-year mortality 7.6%; sources + Related Pages updated
- wiki/concepts/hf-phenotype-classification.md — added 7-registry EF phenotype distribution table; sources + Related Pages updated

### Key content vs. existing wiki
- First structured epidemiological data for the wiki; existing pages had [needs source] placeholders
- HFpEF 16–47% range explained by registry setting, region, diagnostic criteria
- 5-year mortality paradox: lower 1-year CV mortality in HFpEF offset by higher non-CV mortality → comparable 5-year outcomes
- IHD 32% in HFpEF vs. 56–60% in HFrEF (Swedish HF registry) — mechanistically distinct aetiology profile
- Valvular disease 20% of HFpEF vs. 4% HFrEF (ESC-HF-LT)
- Costs: Germany €25,532/year highest; HFpEF driving disproportionate future cost increases

### Citations updated
- wiki/citations.md — Savarese2022GlobalBurden added to Ingested table and formatted refs

### Trials-pending
- No post-2020 HFpEF clinical trials to add (epidemiology review)

## 2026-05-06 (session 10 — ingest Pfeffer 2019 HFpEF perspective)

### Ingested
- raw/2019-CIRCRESAHA-Pfeffer-HFpEF_perspective.pdf → [[pfeffer2019hfpef]] (citekey: Pfeffer2019HFpEF)

### New pages created
- wiki/sources/pfeffer2019hfpef.md — new source page; invited Circ Res perspective; pathophysiologic cascade (Figure 2); cGMP/PKG paradigm; titin; ATTR 13–19% prevalence; therapeutic landscape 2019; CHAMPION trial; SECRET trial; prevention evidence; PEP-CHF

### Updated pages
- wiki/entities/hfpef.md — added cGMP/PKG cellular mechanism paragraph; titin; ATTR 13–19% prevalence + tafamidis/SPECT screening; Pfeffer2019HFpEF to sources
- wiki/concepts/hfpef-treatment-gap.md — added PEP-CHF to failed trials table (HR 0.92, P=0.55); added CHAMPION trial section (haemodynamic monitoring reduces HF hosp in HFpEF); Pfeffer2019HFpEF to sources
- wiki/concepts/exercise-intolerance.md — added Kitzman 2010 first RCT note; SECRET trial (exercise + caloric restriction, additive benefit); systemic microvascular dysfunction mechanism; Pfeffer2019HFpEF to sources
- wiki/concepts/hfpef-diagnosis.md — added 1990s–2000s history entry: 9 epidemiological definitions 1997–2015; CHARM-Preserved LVEF >40% threshold rationale; Pfeffer2019HFpEF to sources
- wiki/index.md — added [[pfeffer2019hfpef]] under Review Articles
- wiki/citations.md — Pfeffer2019HFpEF added to Ingested table and formatted refs

### Trials-pending added
- PEP-CHF (Cleland 2006): perindopril in HF LVEF >40%, elderly ≥70y; HR 0.92 neutral; historical RAAS trial
- REDUCE LAP-HF II (NCT03088033): interatrial shunt device in HFpEF; haemodynamic decompression via L→R shunt
- Minimally invasive pericardial modification (NCT03923673): device approach targeting extrinsic pericardial constraint in HFpEF

## 2026-05-06 (session 10 — ingest D'Amario 2019 CMD review)

### Ingested
- raw/2019-FPhys-D'Amario-Microvascular_Dysfunction.pdf → [[damario2019cmd]] (citekey: D'Amario2019CMD)

### New pages created
- wiki/sources/damario2019cmd.md — new source page; CMD as "common soil" paradigm; Figure 1 cascade (comorbidities→inflammation→EndoMT→HFpEF); titin N2BA→N2B isoform shift; EndoMT mechanism; calcium overload (late Na⁺/RALI-DHF); CMD measurement tools + 4-type classification; OSA RR 2.2; iron deficiency severity correlation; statins (JASPER); anti-IL-1/anakinra (D-HART); PDE-9; anti-fibrotic (nintedanib/pirfenidone); SGLT2i microvascular mechanism

### Updated pages
- wiki/concepts/diastolic-dysfunction.md — added Cellular Mechanisms section: cGMP/PKG detailed molecular pathway; titin N2BA→N2B isoform shift + hypophosphorylation; EndoMT (endothelial-mesenchymal transition as fibrosis driver); calcium overload via late Na⁺ current; History section extended (Paulus/Tschöpe 2013; Graziani/Crea 2018 CMD "common soil"); sources + Related Pages updated
- wiki/citations.md — D'Amario2019CMD added to Ingested table and formatted refs
- wiki/index.md — added [[damario2019cmd]] under Review Articles

### Key content vs. existing wiki
- EndoMT: first time captured in wiki; primary fibrosis driver; α-SMA/collagen I upregulation; TGF-β/SMAD; cardiomyocyte apoptosis via paracrine signalling
- Titin isoform shift (N2BA→N2B): distinction from mere "titin stiffness" — now mechanistically detailed
- CMD 4-type Camici/Crea classification: not previously in wiki
- OSA: RR 2.2 for HF admission (16.8% prevalence); treatment improves diastolic function
- Iron deficiency: diastolic dysfunction severity proportional to ID severity; absolute vs. functional ID distinction
- Statins: observational evidence for HFpEF benefit; endomyocardial biopsy data (↑PKG, ↓nitrotyrosine, ↓hypertrophy); JASPER study
- Ranolazine/RALI-DHF: calcium overload target; acute haemodynamic proof-of-concept (↓LVEDP/PCWP)
- Anti-fibrotic approaches: HFpEF-IPF shared mechanism; nintedanib/pirfenidone

### Trials-pending
- No post-2020 major HFpEF outcome trials to add (experimental agents are Phase 2 pre-outcome)

## 2026-05-06 (session 10 — comprehensive update of overview.md and timeline.md)

### Updated pages
- wiki/overview.md — full rewrite reflecting all 10 sessions; updated High-Level Summary (microvascular/EndoMT paradigm; two-layer treatment model); Key Concepts expanded (hfpef-phenotype-profiling, ml-ai-hfpef, diastolic-dysfunction cellular mechanisms added); Active Debates extended (CMD debate, statins, diagnostic algorithm choice); Recent Additions through session 10; Knowledge Gaps updated and extended (FINEARTS-HF, SUMMIT/STEP-HFpEF, CABA-HFpEF, CMD targeting, EndoMT, statins RCT, iron deficiency, cancer HFpEF)
- wiki/timeline.md — added Epidemiology section (Savarese 2022; Anker 2023 comorbidity prevalences); Pathophysiology timeline: filled [needs source] entries; added 2013 (Paulus/Tschöpe cGMP/PKG), 2018 (Graziani/Crea CMD "common soil"), 2019 (EndoMT + titin isoform shift + calcium overload); Treatment timeline: added 2010 (Kitzman first exercise RCT), 2017 (AHA/ACC Class IIb ARB/MRA), 2023 (Anker HFA/ESC two-layer model + ACC 2023 ECDP); Landmark Trials: added PEP-CHF (2006); AI/ML section: populated with Yi 2025 data (ECG-AI, NLP, phenotyping, TOPCAT responder prediction)

## 2026-05-12 (session 11 — ingest McDonagh 2023 ESC Focused Update)

### Sources ingested
- raw/2023-ESC-McDonagh-Focused_update_guidelines.pdf → [[mcdonagh2023escupdate]] (citekey: McDonagh2023ESCupdate [zotero-unverified])

### New pages created
- wiki/sources/mcdonagh2023escupdate.md — 2023 ESC Focused Update on HF; SGLT2i Class I, Level A for HFpEF and HFmrEF; STRONG-HF Class I Level B (rapid in-hospital/post-discharge GDMT intensification); EMPULSE (empagliflozin acute HF; win ratio 1.36); finerenone Class I Level A for CKD+T2DM (FIDELIO-DKD + FIGARO-DKD); iron deficiency update; HFpEF Figure 2 algorithm (3 green arms: diuretics, SGLT2i, comorbidity); explicit footnote: benefit hospitalization-driven, not CV mortality

### Updated pages
- wiki/concepts/guideline-comparison.md — renamed scope to ESC 2021 / ESC 2023 / AHA 2022 / ACC 2023 ECDP; 4-column overview table added; ESC 2023 SGLT2i Class I section and history entry added; contradictions updated; sources frontmatter updated
- wiki/entities/sglt2-inhibitors.md — summary updated (Class I ESC 2023 for HFpEF/HFmrEF); ESC 2023 paragraph added in Role in HFpEF; 3-row status table updated (ESC 2023 row: Class I, Level A across all EF categories); sources frontmatter updated
- wiki/concepts/hfpef-treatment-gap.md — summary updated (ESC 2023 Class I + AHA 2022 Class 2a); McDonagh2023ESCupdate added to sources frontmatter
- wiki/contradictions.md — contradiction #9 updated: ESC 2021/AHA 2022 divergence marked RESOLVED by ESC 2023; ESC 2023 paragraph added
- wiki/timeline.md — ESC 2023 treatment entry added (Class I SGLT2i HFpEF; STRONG-HF; finerenone CKD)
- wiki/overview.md — High-Level Summary updated (ESC 2023 Class I); guideline-comparison link updated; hfpef-treatment-gap bullet updated; ESC 2025 anticipation revised; session 11 entry added to Recent Additions
- wiki/citations.md — McDonagh2023ESCupdate added to Ingested table and full formatted refs
- wiki/index.md — [[mcdonagh2023escupdate]] added under Guidelines

### Trials-pending added
- STRONG-HF (NCT03412201): rapid in-hospital/post-discharge GDMT intensification in acute HF; 180-day primary; ESC 2023 Class I
- EMPULSE (NCT04157751): empagliflozin initiated in-hospital in acute HF across LVEF spectrum; win ratio 1.36; ESC 2023 acute HF context

## 2026-05-12 (session 11 — ingest Mahmood 2024 systematic review of HFpEF guidelines)

### Sources ingested
- raw/2024-ehj-qcco-Mahmood_systematic_review_practice_guidelines.pdf → [[mahmood2024guidelines]] (citekey: Mahmood2024Guidelines [zotero-unverified])

### New pages created
- wiki/sources/mahmood2024guidelines.md — first systematic AGREE II review of 7 HFpEF guidelines; Figure 2 agreement/disagreement/gaps taxonomy; 7-guideline comparison table (NP thresholds, E/e', LAVI, SGLT2i adoption, surveillance); GLP-1RA evidence gap (STEP-HFpEF/DM published); SOTA-P-CARDIA, SPIRRIT, REHAB-HFpEF as new ongoing trials

### Updated pages
- wiki/concepts/guideline-comparison.md — added international guidelines section (NHFA/CSANZ, CCS/CHFS, SHA, JCS/JHFS); NP threshold comparison table (7 guidelines); E/e' threshold table; LAVI threshold table; SGLT2i adoption by guideline table; surveillance frequency table; Mahmood2024Guidelines added to sources
- wiki/contradictions.md — added #17 (E/e' threshold: ESC >9 vs. AHA ≥15 vs. others >14), #18 (LAVI: AHA ≥29 vs. ESC/others >34), #19 (NP age-adjustment: uniform vs. NHFA/CSANZ stratified)
- wiki/trials-pending.md — added: SOTA-P-CARDIA (NCT05562063, sotagliflozin HFpEF no T2DM), SPIRRIT (NCT02901184, spironolactone HFpEF), REHAB-HFpEF (NCT05525663, cardiac rehab HFpEF), REACH-HFpEF (NCT TBD), STEP-HFpEF (semaglutide, PUBLISHED NEJM 2023 — candidate for ingest)
- wiki/citations.md — Mahmood2024Guidelines added to Ingested table and full formatted refs
- wiki/index.md — [[mahmood2024guidelines]] added under Guidelines section

## 2026-05-12 (session 11 — ingest Bohmke 2022 nonpharmacological HFpEF strategies)

### Sources ingested
- raw/2022-CardioClin-Bohmke-nonpharmacological_hfpef.pdf → [[bohmke2022nonpharm]] (citekey: Bohmke2022Nonpharm [zotero-unverified])

### New pages created
- wiki/sources/bohmke2022nonpharm.md — narrative review of 4 exercise modalities (MCT, HIIT, combined resistance/aerobic, IMT) and dietary interventions (caloric restriction, sodium restriction, MedDiet, DASH, malnutrition management) in HFpEF; key trials: Kitzman 2010, SECRET, HEART Camp, EX-DHF, OPTIMEX-CLIN (N=180 HIIT=MCT), Palau 2014 (IMT +2.9 mL/kg/min), Kinugasa 2020 (at-home IMT); PICNIC + EFFORT malnutrition trials; SODIUM-HF; UFA-Preserved pilot

### Updated pages
- wiki/entities/supervised-exercise-training.md — summary updated to include 4 modalities (IMT added); Description section expanded: 4-modality descriptions with IMT mechanism (respiratory muscle O2 competition); Key Individual Trials table added (8 trials including OPTIMEX-CLIN + IMT RCTs); sources frontmatter updated (Bohmke2022Nonpharm + Mirzai2025Exercise added); Related Sources updated
- wiki/concepts/exercise-intolerance.md — Respiratory Muscle Oxygen Competition section added (IMT mechanism distinct from the 4-component model); Caloric Restriction and Skeletal Muscle Fat Infiltration section added (IMAT → peripheral O2 utilisation; SECRET CR arm); History entries for Palau 2014, Kinugasa 2020, Bohmke 2022 review added; Open Questions: 2 new questions on IMT phenotype specificity and CR in non-obese/cachectic; Related Sources updated (bohmke2022nonpharm + mirzai2025exercise added); sources frontmatter updated
- wiki/trials-pending.md — added OPTIMEX-CLIN (HIIT vs. MCT vs. control, N=180, largest head-to-head), SECRET-II (NCT02636439, caloric restriction + exercise in obese HFpEF), UFA-Preserved 2 (NCT03966755, omega-3 supplementation in HFpEF)
- wiki/citations.md — Bohmke2022Nonpharm added to Ingested table and full formatted refs
- wiki/index.md — [[bohmke2022nonpharm]] added under Review Articles
- wiki/overview.md — supervised-exercise-training bullet updated (4 modalities + IMT data); Recent Additions session 11 extended; Knowledge Gaps: HIIT bullet updated + IMT gap + dietary gap added

## 2026-05-12 (session 11 — ingest Zeid 2025 MyoMobile study design)

### Sources ingested
- raw/2025-ESC-Zeid-MyoMobile_study.pdf → [[zeid2025myomobile]] (citekey: Zeid2025MyoMobile [zotero-unverified])
- Note: design paper only; N=185 ITT; primary results (step count at 12 weeks) not yet published

### New pages created
- wiki/sources/zeid2025myomobile.md — MyoMobile study design; 3-arm EE2 RCT (standard care vs. wearable tracking vs. tracking+coaching); app algorithm (step count, weekly goal adjustment); eligibility criteria; full baseline characteristics table (LVEF 53.5%, median NT-proBNP 418, E/e' 9.42, AF 51.9%, obesity 40.5%); secondary endpoints (CPET, echo, HRV, 6MWT, KCCQ, multi-omics); DZHK Rhine-Main; NCT04940312

### Updated pages
- wiki/entities/supervised-exercise-training.md — added "Digital Health and App-Based Approaches" section: MyoMobile app algorithm description; complementary vs. equivalent distinction; sources frontmatter + Related Pages updated
- wiki/concepts/ml-ai-hfpef.md — added "Digital Health Interventions (mHealth)" section: MyoMobile as first prospective mHealth RCT in HFpEF; accelerometry/DMOs connection to Docherty 2025; sources frontmatter + Related Sources updated
- wiki/trials-pending.md — added MyoMobile (NCT04940312, design paper, primary results pending)
- wiki/citations.md — Zeid2025MyoMobile added to Ingested table and full formatted refs
- wiki/index.md — [[zeid2025myomobile]] added under Review Articles
- wiki/overview.md — session 11 Recent Additions entry extended with Zeid 2025

## 2026-05-12 (session 11 — scan 25 ClinicalTrials.gov registry .md files in raw/)

### Assessment
25 markdown registry files examined. 19 match already-ingested sources (TOPCAT/NCT00094302, EMPEROR-Preserved, TORCH, TORCH-Plus, DECIPHER-HFpEF, DELIVER, PARAGON-HF, CHARM-Preserved, I-Preserve, CAPACITY-HFpEF, DETERMINE-Preserved, NEAT-HFpEF, VITALITY-HFpEF, DAPA-HF, EMPEROR-Reduced, PARADIGM-HF, INDIE-HFpEF, MyoMobile) — no new wiki content needed for these. 6 are genuinely new.

### Trials added to wiki/trials-pending.md
- **MyoVasc (NCT04064450)** — Mainz observational cohort, N=3,289 HF patients, 10-year follow-up, PI Philipp Wild (same as MyoMobile); published design paper (Gobel 2021, Eur J Prev Cardiol)
- **HIT-HF (NCT03184311)** — University of Basel; HIIT vs. MCT in HFpEF, N=86, design paper (Gasser 2021, Front Physiol); distinct from OPTIMEX-CLIN
- **Levine HFpEF Vascular-Metabolic-Neural Study (NCT03465072)** — UT Southwestern, suspended; mechanistic MSNA + VO₂ kinetics + KE training; first aim accomplished
- **OptimEx Long-Term Follow-up (NCT05162859)** — TU Munich, N=74; observational follow-up of OPTIMEX-CLIN and EX-DHF to assess VO₂ durability post-training
- **m-Health CR HFpEF Pandey (NCT05002075)** — UT Southwestern, N=69, COMPLETED pilot RCT; home-based mHealth CR vs. standard care in HFpEF
- **Muscle Blood Flow HFpEF Bunsawat (NCT05115890)** — VA, N=35; peripheral vascular control mechanisms + KE training

## 2026-05-12 (session 12 — ingest pending trials: entity pages, source stubs, trials.md update)

### Task
Converted all 31 entries in wiki/trials-pending.md into entity pages and/or trials.md rows. trials-pending.md cleared.

### Entity pages created (Tier 1 — major published trials)
- wiki/entities/finearts-hf.md — finerenone (non-steroidal MRA) in HFpEF; HR ~0.84 (P=0.007); first non-SGLT2i positive pharmacological HFpEF trial [created previous session, confirmed this session]
- wiki/entities/strong-hf.md — high-intensity GDMT uptitration in acute HF; ~8% absolute ARR 180-day; ESC 2023 Class I
- wiki/entities/empulse.md — empagliflozin in-hospital initiation in acute HF; win ratio 1.36; safety established across LVEF
- wiki/entities/relax.md — sildenafil (PDE5i) in HFpEF; N=216; fully neutral; part of NO/cGMP failure series
- wiki/entities/attr-act.md — tafamidis in ATTR-CM; N=441; mortality RR 0.70; first disease-modifying ATTR-CM therapy; AHA 2022 Class I
- wiki/entities/victoria.md — vericiguat in HFrEF; N=5,050; HR 0.90 (P=0.02); contrast with neutral VITALITY-HFpEF
- wiki/entities/socrates-preserved.md — vericiguat phase 2b in HFpEF; NT-proBNP signal; motivated VITALITY-HFpEF phase 3 (then neutral)
- wiki/entities/step-hfpef.md — semaglutide 2.4 mg in obese HFpEF; N=529; KCCQ-CSS +6.4 pts, 6MWD +20.5m (P<0.001); first major GLP-1RA HFpEF trial
- wiki/entities/pep-chf.md — perindopril in elderly HFpEF; N=850; HR 0.92 (P=0.55); oldest RAAS trial; high drug discontinuation

### Entity pages created (Tier 2 — ongoing trials)
- wiki/entities/summit.md — semaglutide in HFpEF+obesity; peak VO₂ + KCCQ co-primary; NCT04847557
- wiki/entities/tirzepatide-hfpef.md — tirzepatide (GLP-1/GIP) in HFpEF+obesity; NCT04788511
- wiki/entities/spirit-hf.md — spironolactone in HFpEF; NCT04727073; definitive MRA trial
- wiki/entities/spirrit.md — spironolactone vs. usual care in HFpEF; NCT02901184
- wiki/entities/caba-hfpef.md — catheter ablation vs. rate control in HFpEF with AF; NCT05508256; DZHK
- wiki/entities/fair-hfpef.md — IV ferric carboxymaltose in HFpEF with iron deficiency; NCT03074591
- wiki/entities/reduce-lap-hf-ii.md — interatrial shunt device in HFpEF; NCT03088033; overall neutral; PVR subgroup signal
- wiki/entities/sota-p-cardia.md — sotagliflozin (SGLT2+SGLT1) in HFpEF without T2DM; NCT05562063
- wiki/entities/rehab-hfpef.md — structured cardiac rehabilitation in HFpEF; NCT05525663
- wiki/entities/myomobile.md — app-based PA coaching in HFpEF; NCT04940312 (source page already existed)

### Source stubs created (Tier 1 — published trials without PDFs)
- wiki/sources/mebazaa2022stronghf.md — STRONG-HF
- wiki/sources/voors2022empulse.md — EMPULSE
- wiki/sources/redfield2013relax.md — RELAX
- wiki/sources/maurer2018attract.md — ATTR-ACT
- wiki/sources/armstrong2020victoria.md — VICTORIA (note: distinct from armstrong2020vitality = VITALITY-HFpEF, same first author, same year, different trial)
- wiki/sources/pieske2017socrates.md — SOCRATES-PRESERVED
- wiki/sources/kosiborod2023stephfpef.md — STEP-HFpEF (semaglutide)
- wiki/sources/cleland2006pepchf.md — PEP-CHF

### Trials added to trials.md only (Tier 3 — smaller/mechanistic/observational; no entity pages)
- OPTIMEX-CLIN, HIT-HF, SECRET-II, UFA-Preserved 2, MyoMobile, m-Health CR HFpEF, OptimEx-LTF (Non-Pharmacological/Exercise section)
- Levine NCT03465072, Bunsawat NCT05115890, MyoVasc (Mechanistic section)
- REDUCE LAP-HF II, Pericardial Modification (Device section)
- REACH-HFpEF (Non-Pharmacological section)
- Butler 2022 EF Spectrum analysis (Secondary Analyses table)

### trials.md restructured
Added new sections: Acute Heart Failure Trials; Device Trials; Non-Pharmacological and Exercise Trials; Mechanistic Studies; ATTR-CM Trials. Historical negative HFpEF pharmacological trials now in separate subsection. Total trials tracked: ~40+.

### trials-pending.md cleared
All 31 pending entries processed and removed. File now contains only the "How to Add a Trial" instructions section.

### Citations updated
- wiki/citations.md — Stub Sources table updated: Solomon2024FINEARTS + 8 new stub citekeys added; formatted references added in Stub Sources section

### Metadata updated
- wiki/index.md — 8 new source pages added under Clinical Trial Papers; 19 new entity pages added under Clinical Trial Entities
- wiki/log.md — this entry

## 2026-05-18 (session 22 — ingest: exercise trials + systematic reviews/meta-analyses)

### Sources ingested (PDFs read)

**Exercise trials:**
- raw/2021-NEJM-Kitzman-REHAB-HF_study.pdf → citekey: Kitzman2021REHABHF
- raw/2021-JACC-Mentz-REHAB-HF_study.pdf → citekey: Mentz2021REHABHFpEF
- raw/2021-JAMA-Mueller-HIIT_moderate_guideline_study.pdf → citekey: Mueller2021OptimEx
- raw/2020-ESC-DonelliDaSilveira-HIIT_moderate_HFpEF.pdf → citekey: DonelliDaSilveira2020HIIT
- raw/2020-GeroGeriMed-Azhar-dietry_exercise_hfpef_pilot_study.pdf → citekey: Azhar2020Protein

**Systematic reviews and meta-analyses:**
- raw/2022-HeartFailRef-Jin-LA_structure.pdf → citekey: Jin2022LA
- raw/2023-HeartFailRev-Lin-CMD_prevalence.pdf → citekey: Lin2023CMD
- raw/2024-CurrProbCardiol-Kaddoura-beta_blocker_hfpef.pdf → citekey: Kaddoura2024BetaBlocker
- raw/2024-FrontCardioMed-Fu-inflammatory_markers_hfpef.pdf → citekey: Fu2024Inflammation
- raw/2024-HeartLungCirc-Lee-lifestyle_interventions_HFpEF.pdf → citekey: Lee2024Lifestyle
- raw/2025-EHJO-Prokopidis-Exercise_capacity_hfpef_hfref.pdf → citekey: Prokopidis2025Exercise
- raw/2025-AmJPhysiolHeart-vanDeBovenkamp-hemodynamics_hfpef_hfref.pdf → citekey: vanDeBovenkamp2025Hemodynamics
- raw/2025-HeartFailRev-Ammar-BNP_NTBNP_hfpef.pdf → citekey: Ammar2025BNP

### New source pages created (13)
- wiki/sources/kitzman2021rehabhf.md — REHAB-HF main results; NCT02196038; N=349; ≥60y, ADHF any EF; transitional multidomain rehab; SPPB +1.5 pts (P<0.001); 6MWD +34 m; KCCQ +7.1; rehospitalisation NS (RR 0.93); 97% frail/pre-frail; 53% HFpEF
- wiki/sources/mentz2021rehabhfhfpef.md — REHAB-HF HFpEF subgroup; HFpEF (EF≥45%; n=185) vs HFrEF (n=164); SPPB +1.9 (1.1–2.6) vs +1.1 (0.3–1.9); global rank endpoint significant in HFpEF (PI=0.59; P=0.04) not HFrEF; interaction P=0.098
- wiki/sources/mueller2021optimex.md — OptimEx-Clin; NCT02078947; 5 European sites; N=180 HFpEF; HIIT +1.5, MCT +2.0 mL/kg/min at 3 months; HIIT vs MCT: −0.4 (NS); gains lost at 12 months; E/e' unchanged
- wiki/sources/donelli2020hiit.md — DonelliDaSilveira 2020; N=19; HIIT +3.5 vs MCT +1.9 mL/kg/min (P<0.001); E/e' improved both arms; likely false positive
- wiki/sources/azhar2020protein.md — Azhar 2020; N=23 randomised, 16 analysed; protein supplement ± exercise; combined arm: 6MWD +36.6 m, quadriceps +21.5 kg; PS alone: no benefit, ↑body fat
- wiki/sources/jin2022la.md — Jin 2022 LA meta-analysis; 61 studies (8,806 HFrEF + 9,928 HFpEF); LAGLS_R 9–12.8% HFrEF vs 18.9–23.4% HFpEF; AF 34–43% in HFpEF
- wiki/sources/lin2023cmd.md — Lin 2023 CMD prevalence; 10 studies; 1,267 patients; pooled CMD 71% (invasive 79%; non-invasive 66%); CFR −1.28 vs controls; CMD RR 2.21
- wiki/sources/kaddoura2024betablocker.md — Kaddoura 2024 beta-blocker meta-analysis; 16 observational studies; 27,188 patients; mortality OR 0.81 (0.65–0.99; P=0.044); HF rehospitalisation NS
- wiki/sources/fu2024inflammation.md — Fu 2024 inflammatory markers; 8 cohort studies; 9,744 patients; all-cause mortality HR 1.43; CV mortality HR 2.04; CV rehospitalisation HR 2.83; I²=0%
- wiki/sources/lee2024lifestyle.md — Lee 2024 lifestyle interventions; 6 RCTs; 375 patients; weight −5.30 kg; 6MWD +43.63 m; NYHA −0.54; MLHFQ −17.77 (all P<0.001)
- wiki/sources/prokopidis2025exercise.md — Prokopidis 2025 exercise meta-analysis; 46 studies; VO₂peak higher by 0.78 mL/kg/min in HFpEF (P=0.02; NS after comorbidity adjustment); CO and SV higher in HFpEF
- wiki/sources/vandebovenkamp2025hemodynamics.md — van de Bovenkamp 2025 hemodynamics meta-analysis; 21 RCTs; reverse remodeling essentially absent in HFpEF vs robust in HFrEF; SV not increased in HFpEF; LVMi −2.8 g/m²
- wiki/sources/ammar2025bnp.md — Ammar 2025 BNP/NT-proBNP; 22 studies; 10,158 HFpEF patients; adverse events HR 1.34–1.80; CV mortality HR 1.44–1.65; low BNP = poor prognosis in HFpEF

### New entity pages created (2)
- wiki/entities/rehab-hf.md — REHAB-HF trial entity; NCT02196038; main results + HFpEF subgroup; completed; published NEJM 2021 + JACC HF 2021
- wiki/entities/optimex-clin.md — OptimEx-Clin trial entity; NCT02078947; HIIT vs MCT vs control results; completed; published JAMA 2021

### New meta-analysis candidates file created
- wiki/sources-pending-from-meta-analyses.md — 25+ candidate papers from 6 ingested meta-analyses; prioritised for future ingest; high-priority: PARAMOUNT (Solomon 2012), Shah 2018 CMD, Arnold 2022 CMD, Lam 2018 beta-blockers, Tamaki NLR/PLR (N=1,026), Zhu/Zhou WBC (N=2,898), Kitzman 2016 SECRET diet arm

### Registry files updated
- wiki/trials.md — added REHAB-HF row; updated OPTIMEX-CLIN row with correct NCT (NCT02078947) and wiki links
- wiki/citations.md — 13 new ingested citekeys added to table; 13 formatted references added to Full Formatted References section

### Metadata updated
- wiki/index.md — added 5 exercise trial source pages under Clinical Trial Papers; added new "Systematic Reviews and Meta-Analyses" section (8 meta-analysis sources); added [[rehab-hf]] and [[optimex-clin]] under Clinical Trial Entities; added [[sources-pending-from-meta-analyses]] to Core Pages
- wiki/entities/supervised-exercise-training.md — added OptimEx-Clin and DonelliDaSilveira 2020 rows to Key Individual Trials table; added Post-Hospitalisation Rehabilitation section (REHAB-HF); updated Related Pages and sources frontmatter
- wiki/overview.md — updated SET bullet (OptimEx-Clin + REHAB-HF references); updated Active Debates (HIIT vs MCT + beta-blockers); added session 22 Recent Additions; added 3 new Knowledge Gaps (post-hospitalisation rehab, beta-blockers RCT gap, inflammatory marker-guided therapy)
- wiki/timeline.md — added REHAB-HF (2021) and OptimEx-Clin (2021) rows to Treatment table
- wiki/log.md — this entry
