config-page
# Wiki Index

## Core Pages
- [[overview]] — high-level summary, active debates, knowledge gaps
- [[timeline]] — chronological evolution of HFpEF understanding
- [[contradictions]] — tensions between sources and pages
- [[citations]] — master citekey → full citation registry; read this when asked for a reference
- [[citations-doi-review]] — DOI verification tracking log; 0 open as of 2026-09-17 lint pass (9 stale null-DOI entries found and synced from citations.md during that pass)
- [[tags-overview]] — canonical tag list with page counts and links; jump here instead of scanning individual pages for a topic
- [[trials]] — master clinical trials overview table (all trials in wiki: title, abbreviation, intervention, condition, NCT, dates)
- [[trials-pending]] — trials referenced in sources but not yet added; review before deciding to ingest
- [[sources-pending-from-meta-analyses]] — candidate primary studies from meta-analyses for future ingest; prioritised by evidence potential
- [[sources-missing]] — standalone papers referenced in wiki prose with no source page yet; review before ingest (2026-07-14)
- [[candidate-pages-review]] — concept/entity/mechanism pages surfaced by mining all sources/concepts/entities; awaiting approval before creation (2026-07-14)
- [[queries/index]] — answered questions saved as canonical query pages

---

## Quick Lookup by Type

Jump straight to the relevant subsection instead of scanning the full Sources/Entities/Concepts lists below.

**Entities by `entity_type`** (80 pages, see `### Clinical Trial Entities` etc. below; entity subsections group loosely by this field):

| entity_type | Count |
|---|---|
| trial | 45 |
| drug | 12 |
| score | 5 |
| comorbidity | 3 |
| imaging-tool | 3 |
| phenotype | 3 |
| registry | 3 |
| guideline | 1 |
| disease | 1 |
| diagnostic-tool | 1 |
| study | 1 |
| treatment-approach | 1 |
| intervention | 1 |

**Concepts by theme** (56 pages, see `## Concepts` subheadings below):

| Theme | Count |
|---|---|
| Core Pathophysiology & Mechanisms | 16 |
| Phenotypes & Comorbidity-Specific HFpEF | 14 |
| Diagnostic Framework & Classification | 7 |
| Exercise Physiology & Intolerance | 7 |
| Treatment & Care Delivery | 7 |
| Biomarkers | 3 |
| AI / Machine Learning | 1 |
| Vascular | 1 |

**Sources by category** — see `## Sources` subheadings below (Guidelines and Consensus Documents, Registry Papers, Observational Studies, Scientific Statements, Clinical Trial Papers, Review Articles, Systematic Reviews and Meta-Analyses, Secondary Analyses, Trial Design Papers).

For topic/keyword lookup across all page types, see [[tags-overview]].

---

## Sources

### Guidelines and Consensus Documents
- [[mcdonagh2021esc]] — 2021 ESC Guidelines for diagnosis and treatment of HF; foundational source; adds SGLT2i as fourth HFrEF pillar
- [[mcdonagh2023escupdate]] — 2023 ESC Focused Update; upgrades SGLT2i to Class I, Level A for HFpEF and HFmrEF; STRONG-HF pre/post-discharge intensive care Class I; finerenone Class I for CKD+T2DM
- [[mahmood2024guidelines]] — Mahmood 2024 (EHJ QCCO): first systematic review of 7 HFpEF guidelines (AGREE II); agreement/disagreement/gaps taxonomy (Figure 2); diagnostic threshold divergences: E/e', LAVI, NP; SGLT2i in 5/7 guidelines post-2021
- [[sauer2026pharmacological]] — Sauer 2026 (ESC Heart Fail): comprehensive pharmacological landscape review; four-society guideline table (ESC/AHA-ACC-HFSA/JCS-JHFS/iCARDIO); SGLT2i Class I across all; finerenone first non-SGLT2i Class I (ESC/iCARDIO); combination therapy paradigm (SGLT2i+nsMRA HR 0.69); emerging trials table (BALANCED-HF, EASi-HF, REDEFINE-HF, CONFIRMATION-HF); no beta blocker recommendation in any society
- [[heidenreich2022aha]] — 2022 AHA/ACC/HFSA Guideline; adds HFimpEF; SGLT2i Class 2a for HFpEF; MRA/ARNI Class 2b for HFpEF; A–D staging
- [[kittleson2023acc]] — ACC 2023 ECDP: operational HFpEF management supplement to AHA 2022; Figure 9 treatment algorithm; sex-stratified ARNI/MRA; HFpEF mimics Table 1; CHECK-IN/INHALE referral acronyms; GLP-1RA + SUMMIT/STEP-HFpEF flagged
- [[anker2023hfpefphenotype]] — HFA/ESC/ESH 2023 Scientific Statement: phenotype profiling for HFpEF; Figure 1 prevalence wheel (18 comorbidities); Figure 2 treatment wheel; SGLT2i universal + phenotype-guided add-on; CABA-HFpEF, FINEARTS-HF, FAIR-HFpEF, SPIRIT-HF flagged
- [[lam2011hfpef]] — Lam 2011 (Eur J Heart Fail 13:18–28): HFpEF epidemiology and natural history review; HFpEF ~50% of all HF; prevalence rising 1%/year; annual mortality ~20–29% (similar to HFrEF); clinical profile: older, female, hypertensive, obese; no proven treatment at time of publication; foundational "why this matters" evidence
- [[savarese2022globalburden]] — Savarese 2022 (Cardiovasc Res): global HF epidemiology invited review; >64 million worldwide; HFpEF 16–47% by registry; 5-year mortality ~50–75%; HFpEF prevalence rising; 7-registry distribution table; costs up to €25,532/year
- [[kittleson2024accaha]] — Kittleson 2024 (JACC): 2024 update to 2020 ACC/AHA HF Performance & Quality Measures; 3 new PMs: PM-2 first HFpEF-specific performance measure (BP control: SBP<130+DBP<80 mmHg), PM-3 SGLT2i for HFrEF; 6 new QMs including QM-1 (SGLT2i for HFmrEF/HFpEF), QM-2 (SDOH screening), QM-6 (amyloid screen); formalises SGLT2i and BP control as US performance standards
- [[pieske2019hfapeff]] — Pieske 2019 (Eur Heart J): HFA-PEFF 4-step diagnostic algorithm (P–E–F1–F2); composite score ≥5=HFpEF; AF-adjusted NP thresholds; canonical ESC/HFA diagnostic reference

### Registry Papers
- [[seyler2017torch]] — TORCH registry rationale (Seyler 2017): 19 DZHK German centres; non-ischemic CMP; 2,300 patients; deep molecular phenotyping; obligatory echo/ECG/labs; biobank; modules: clinical, genomics, inflammation, biomarker

### Observational Studies
- [[ho2019hfpefdefinitions]] — Ho 2019 (Circulation): invasive CPET reference; 7 definitions enroll 12–90% of same cohort; HFpEF_phys (53%) independently predicts CV events
- [[borlaug2010exercise]] — Borlaug 2010 (Circ Heart Fail): invasive supine exercise hemodynamics (n=55); 58% exertional HFpEF with normal resting hemodynamics; exercise PCWP ≥25 mmHg; PASP ≥45 mmHg screen (AUC 0.99); all noninvasive markers AUC <0.70
- [[landsteiner2025hemodynamics]] — Landsteiner 2025 (Circ Res): HC-HFpEF concept (n=872, MGH); 23–28% exercise-unmasked; PCWP/CO slope >2 as upright threshold; trial NT-proBNP criteria exclude 67–71% of HC-HFpEF; 4 hemodynamic profile taxonomy
- [[reddy2018h2fpef]] — Reddy 2018 (Circulation): H₂FPEF score derivation; 6 variables (BMI, ≥2 antihypertensives, AF, PASP>35, age>60, E/e'>9); AUC 0.841; validated against invasive CPET
- [[alnaamani2015pac]] — Al-Naamani 2015 (JACC HF): PAC <1.1 mL/mmHg → HR 4.9 for mortality in HFpEF+PH-LHD; outperforms PVR (AUC 0.37), DPG, TPG; only age and PAC independently predict mortality
- [[pandey2021deepnnecho]] — Pandey 2021 (JACC CI): CNN/TDA-based DeepNN for LVDD phenotyping (9 echo variables); AUROC 0.988/0.997; e' most important; TOPCAT substudy: spironolactone benefit only in high-risk phenogroup (HR 0.65; P=0.01)
- [[gao2025ecgdl]] — Gao 2025 (ESC HF): CNN-LSTM 12-lead ECG model for HFpEF risk; 78% accuracy (Cohort A), 71.8% (Cohort B); LVEDP reference; BNP + E/e' did not differ between risk groups
- [[reddy2024afhfpef]] — Reddy 2024: AF-HFpEF bidirectional relationship; 83% occult HFpEF in symptomatic AF by exercise RHC; ~82% occult AF in HFpEF at 1 year; exercise RHC the only reliable HFpEF diagnostic in AF
- [[beale2018sex]] — Beale 2018 (JACC HF): sex-specific HFpEF physiology; women higher LVEF, smaller LV volumes, greater interstitial fibrosis; sex-biology context for PARAGON-HF and PARAGLIDE-HF
- [[beale2019sex]] — Beale 2019 (JACC HF): sex differences in HFpEF outcomes and physiology; women's higher LVEF biology underpins sex subgroup signals in ARNI trials
- [[duca2018genderdiff]] — Duca 2018 (Sci Rep): N=260 invasive hemodynamics/CMR cohort; men die more of cardiac causes (16.5% vs 6.1%), women die more of non-cardiac causes (10.5% vs 2.5%) — "men die of HFpEF, women die with HFpEF"
- [[lau2022arterialstiffness]] — Lau 2022 (J Card Fail): N=190 invasive CPET cohort; women have ~6mmHg higher augmentation pressure, >10% higher augmentation index than men; arterial stiffness associates with abnormal exercise diastolic reserve more strongly in women
- [[coppi2025genderdiff]] — Coppi 2025 (J Cardiovasc Dev Dis) review: SERCA2a/estrogen-receptor mechanism detail; sex-specific echo/CMR diagnostic reference ranges (LA strain, GLS, ECV); SGLT2i/GLP-1RA sex-subgroup trial data (non-significant trend favouring women)
- [[bozkurt2020sex]] — Bozkurt 2020 (JACC): sex and gender differences across the HF spectrum; women higher LVEF explains ARNI sex-treatment interaction
- [[lange2024cmr]] — Lange 2024 (Int J Cardiovasc Imaging): cross-sectional CMR n=54 HF (22 HFpEF, 17 HFmrEF, 15 HFrEF) + 19 controls; HFpEF vs controls: LA reservoir strain 28.9 vs 35.9% (P=0.008), LV GLS −15.0 vs −19.2% (P=0.001), native T1 1012 vs 988 ms (P=0.003); LACI elevated (P=0.004)
- [[akerman2025ai]] — Akerman 2025 (Nat Commun): EchoGo HF v2 (Ultromics) external validation in 240 cases + 256 controls; AUROC 0.797 vs H₂FPEF 0.788 (P=0.001); 9.1% AI intermediate vs 61.7% H₂FPEF; AI-positive HR 2.56 for composite outcome; high sensitivity vs high specificity diagnostic trade-off
- [[haykowsky2011exercise]] — Haykowsky 2011 (JACC): exercise physiology; n=48 HFpEF vs 25 HCs; peak VO₂ −30%; A-VO₂ Diff reserve strongest independent predictor of peak VO₂ (β=0.66; P=0.0002); implicates peripheral noncardiac factors
- [[reddy2017artstiff]] — Reddy 2017 (JACC; Borlaug lab): invasive exercise arterial stiffness; n=98 HFpEF vs 22 controls; no resting difference; exercise unmasks higher arterial elastance + lower TACI (both P<0.001); correlated with higher PCWP (r=−0.42) and lower CO (r=−0.66); inorganic nitrite reduces wave reflections and PCWP −8 mmHg at exercise
- [[shah2018promis]] — PROMIS-HFpEF (Shah 2018, Eur Heart J): 75% CMD prevalence (151/202) in guideline-defined HFpEF; multinational 5-centre; CMD correlates with UACR, NT-proBNP, impaired RV function; CRP NOT associated with CMD
- [[arnold2022diamond]] — DIAMOND-HFpEF (Arnold 2022, JACC CI): CMR-based; 70% MVD (MPR<2.0) in HFpEF vs 48% controls; MPR independently predicts death/HF hosp (HR 0.69, P=0.03); NO correlation between MPR and ECV/fibrosis — CMD and fibrosis are independent prognostic mechanisms
- [[tamaki2023nlrplr]] — Tamaki 2023 (JAHA; PURSUIT-HFpEF; n=1,026): NLR+PLR combined HR 2.66 for cardiac death; serial NLR+PLR HR 2.71; CRP not independently associated; largest NLR/PLR study in ADHF-HFpEF
- [[boralkar2019nlr]] — Boralkar 2019 (Am J Cardiol; Stanford; n=443): NLR on admission HR 1.18 (P=0.04); NLR trajectory HR 1.26 (P=0.001); both incremental to GWTG-HF risk score; NLR trajectory improves AUC at 1-, 2-, 3-year follow-up
- [[zhuzhou2021leukocyte]] — Zhu and Zhou 2021 (BMC Cardiovasc Disord; TOPCAT substudy; n=2,898): U-shaped leukocyte-mortality relationship; Q1 (lowest) HR 1.44 and Q4 (highest) HR 1.90 vs Q2 reference; women-predominant effect
- [[joseph2016qrs]] — Joseph 2016 (JACC HF; TOPCAT post-hoc; N=3,445): QRS ≥120 ms in 17.9%; HR 1.27 for primary composite (P=0.009); HFH HR 1.38 (P=0.003); continuous QRS risk from ~100 ms; no spironolactone interaction by QRS; broader-EF comparison
- [[suzuki2018sdb]] — Suzuki 2018 (ESC HF; Fukushima; N=221 HF): severe SDB (AHI >30/h) predicts higher PWV in HFpEF (β=0.234; P=0.005) but NOT HFrEF (P=0.068); first evidence of differential SDB-arterial stiffness relationship by EF subtype
- [[kasahara2018chart2]] — Kasahara 2018 (Heart Vessels; CHART-2 registry; N=4,301 HF): BNP prognostic across EF subtypes; median BNP HFpEF 85.3 vs. HFrEF 208 pg/mL; HR per log₂ BNP similar across groups (interaction P=0.300); CART cut-offs: 30/100/300 pg/mL; Tohoku Japan 6.3y follow-up
- [[zamani2023pericardialfat]] — Zamani 2023 (Circulation research letter; NCT04068844; N=28 obese HFpEF): epicardial fat r=0.88 with LV eccentricity index (P<0.001); paracardial fat r=0.91 (P<0.001); BMI and subcutaneous/visceral fat NOT correlated; 13/28 had abnormal eccentricity >1.0
- [[sung2023fqrs]] — Sung 2023 (JAHA; N=960 HFpEF; Taiwan; 657-day median follow-up): fQRS prevalence 31.6%; anterior/lateral fQRS HR 1.90 for HFH (P<0.001); associated with myocardial perfusion defects and coronary slow flow; prognostic marker beyond standard echo parameters
- [[leahy2025heartlung]] — Leahy 2025 (JACC HF; NCT04068844; N=55 obese HFpEF): dynamic hyperinflation in 62% at 20W and 85% at peak; DH group PCWP 23±8 vs. 16±6 mmHg at 20W (P=0.005); ΔEELV correlates with ΔPCWP (r²=0.167 at peak; P=0.002); EFL severity NOT associated with PCWP; reframes elevated exercise PCWP as partly ventilatory in obese HFpEF
- [[ortegahernandez2024statins]] — Ortega-Hernández 2024 (J Clin Med; RICA registry; N=2,788 HFpEF): statin use (40.2%); 1-year mortality 14.7% vs. 20.9% (non-statin); adjusted HR 0.74 (P=0.002); benefit restricted to patients without IHD (HR 0.69; P<0.001); IHD subgroup NS; aldosterone antagonists and digoxin associated with worse outcomes (HR 1.34 each)
- [[gonzalez2024sglt2trends]] — González 2024 (BMC Cardiovasc Disord 2024;24:285): US MarketScan claims, Jan 2020–Jun 2023; HFpEF SGLT2i overall 0.5%→9.9%; with T2DM ~20%; without T2DM ~1.2% — 17-fold gap; implementation gap persists despite Class I ESC 2023; canagliflozin collapsed after CANVAS; dapagliflozin + empagliflozin dominate; clinician T2DM-drug mental model lingers

### Scientific Statements
- [[sachdev2023exercise]] — Sachdev 2023 AHA Statement: SET meta-analysis (8 RCTs, n=503); VO2 +2.8 mL/kg/min; skeletal muscle as primary exercise intolerance mechanism
- [[borlaug2023statement]] — Borlaug 2023 JACC Scientific Statement: comprehensive HFpEF state-of-the-field; 5-phenotype Venn model; epidemiology (1-in-10 lifetime risk); SGLT2i first-line; 24 knowledge gaps; disease progression spectrum (LA→PH→RV)
- [[mirzai2025exercise]] — Mirzai 2025 (Heart Fail Rev): state-of-the-art review ~30 exercise RCTs 2004–2024; MICT best evidence; HIIT not superior to MICT; ~1/3 non-responders; no hard outcomes

### Clinical Trial Papers
- [[cleland2021homage]] — HOMAGE: spironolactone vs. usual care in Stage B pre-HF (N=527); primary endpoint (galectin-3 × PIIINP interaction) neutral (P=0.947); PIIINP mean diff −0.15 µg/L (P=0.323); secondary echo/BP/NT-proBNP signals favourable but exploratory
- [[anker2021emperor]] — EMPEROR-Preserved: empagliflozin in HFpEF (LVEF >40%); 5,988 patients, 622 sites/23 countries; first positive major HFpEF trial; methods fully expanded
- [[pitt2014topcat]] — TOPCAT: spironolactone vs. placebo in HFpEF; 3,445 patients, 266 centers/6 countries; neutral overall; Americas subgroup positive; methods expanded
- [[ferreira2026emperor]] — EMPEROR-Preserved secondary analysis (Ferreira 2026): serum Mg predicts outcomes; empagliflozin raises Mg; higher Mg → more benefit; opposite to HFrEF direction
- [[solomon2019paragon]] — PARAGON-HF: sacubitril/valsartan vs. valsartan; LVEF ≥45%, N=4,822; RR 0.87 (P=0.06); subgroup signal LVEF <57% + women; FDA label extension
- [[yusuf2003charm]] — CHARM-Preserved: candesartan vs. placebo; LVEF >40%, N=3,023; HR 0.89 (P=0.118); HF hosp signal (P=0.017); NCT00634712
- [[massie2008ipreserve]] — I-PRESERVE: irbesartan vs. placebo; LVEF ≥45%, N=4,128; HR 0.95 (P=0.35); fully neutral; most definitive RAAS null trial
- [[solomon2022deliver]] — DELIVER: dapagliflozin vs. placebo; LVEF >40%, N=6,263; HR 0.82 (P<0.001); consistent benefit ≥60% LVEF
- [[redfield2015neat]] — NEAT-HFpEF: isosorbide mononitrate; LVEF ≥50%, N=110; primary P=0.06; patients significantly LESS active on all doses (P=0.02)
- [[armstrong2020vitality]] — VITALITY-HFpEF: vericiguat vs. placebo; LVEF ≥45%, N=789; KCCQ-PLS neutral (P=0.47/0.80)
- [[udelson2020capacity]] — CAPACITY-HFpEF: praliciguat vs. placebo; LVEF ≥40%, N=196; peak VO₂ neutral; KCCQ worse in active arm (P=0.007)
- [[mcmurray2024determine]] — DETERMINE: dapagliflozin HFpEF+HFrEF; N=817 (504 HFpEF); HFpEF arm missed all primary endpoints; 6MWD neutral across all arms
- [[mcmurray2014paradigm]] — PARADIGM-HF: sacubitril/valsartan vs. enalapril in HFrEF; superior on mortality + hospitalization
- [[mcmurray2019dapahf]] — DAPA-HF: dapagliflozin in HFrEF; 26% reduction in primary composite; established SGLT2i as 4th pillar
- [[packer2020emperor]] — EMPEROR-Reduced: empagliflozin in HFrEF; 25% reduction; renal protection
- [[zamani2015indie]] — INDIE-HFpEF: inorganic nitrate; neutral; negative NO pathway trial
- [[ahmed2006dig]] — DIG-Preserved: digoxin in HF LVEF ≥45%; neutral
- [[pocock2013maggic]] — MAGGIC: individual patient meta-analysis; HFpEF mortality lower than HFrEF but confounded by comorbidity
- [[mebazaa2022stronghf]] — STRONG-HF (Mebazaa 2022): high-intensity NT-proBNP-guided GDMT uptitration; N=1,078; 180-day ARD 8.1% (RR 0.66, P=0.0021); HFpEF subgroup directionally consistent; ESC 2023 Class I; NCT04142201
- [[voors2022empulse]] — EMPULSE (Voors 2022): empagliflozin in-hospital acute HF; N=530; win ratio 1.36 (1.09–1.68; P=0.0054); HFpEF subgroup win ratio 1.39 (0.95–2.03); renal safety confirmed; NCT04157751
- [[albulushi2025sglt2fibrosis]] — Albulushi 2025 (Eur J Med Res 30:592): N=100 HFpEF+T2DM; dapagliflozin 10 mg vs. placebo 12 months; serial CMR; ΔECV −3.5% vs. −0.8% (P<0.001); ΔLVMI −8.2 vs. −2.1 g/m² (P=0.002); Δ6MWT +45 vs. +10m (P=0.01); ΔNT-proBNP −210 vs. −50 pg/mL (P=0.008); HHF 4% vs. 12% (P=0.03); first serial CMR evidence for SGLT2i antifibrotic mechanism in HFpEF
- [[maier2013ralidhf]] — RALI-DHF (JACC Heart Fail 2013): N=20 HFpEF; ranolazine (late I_Na inhibitor) crossover; exercise LVEDP −4.7 mmHg (P=0.001); Ca²⁺/Na⁺ pathway proof-of-concept; no Phase 3 RCT followed
- [[vantassell2018dhart2]] — D-HART2 results (Circ Heart Fail 2018): N=31 HFpEF; anakinra 24 weeks; hs-CRP AUC ratio 0.40 (P=0.001) — target engaged; peak VO₂ NS (P=0.54) — critical null: inflammation suppression ≠ functional improvement
- [[fudim2024rebalance]] — REBALANCE-HF (JAMA Cardiol 2024): N=80 HFpEF; splanchnic nerve ablation vs. sham; exercise PCWP −5.4 mmHg (P=0.003); KCCQ +12.5 pts; NCT04592445; first sham-controlled RCT for neural preload reduction in HFpEF
- [[zeid2026myomobile]] — MyoMobile primary results (JACC Heart Fail 2026;14(5):102845): N=185 HFpEF; app-based PA coaching significantly increased step count vs. control; KCCQ and 6MWT improved; first positive digital health RCT in HFpEF
- [[redfield2013relax]] — RELAX: sildenafil (PDE5i) vs. placebo in HFpEF; N=216; fully neutral; part of NO/cGMP pathway failure series
- [[maurer2018attract]] — ATTR-ACT: tafamidis in ATTR cardiomyopathy; N=441; mortality RR 0.70; first disease-modifying ATTR-CM therapy; AHA 2022 Class I
- [[armstrong2020victoria]] — VICTORIA: vericiguat in HFrEF; N=5,050; HR 0.90 (P=0.02); contrast with neutral VITALITY-HFpEF (same drug)
- [[pieske2017socrates]] — SOCRATES-PRESERVED: vericiguat phase 2b in HFpEF; NT-proBNP signal at 10 mg; motivated VITALITY-HFpEF phase 3 (then neutral)
- [[kosiborod2023stephfpef]] — STEP-HFpEF (non-DM, 2023): semaglutide 2.4 mg; obese HFpEF without T2DM; KCCQ-CSS +7.8 pts, body weight −10.7 pp, 6MWD +20.3m (all P<0.001); win ratio 1.72; N=529; NCT04788511
- [[packer2025summit]] — SUMMIT primary (NEJM 2025): tirzepatide in obese HFpEF; N=731; HR 0.62 (P=0.026) for CV death/worsening HF; KCCQ-CSS +6.9 pts; first GLP-1RA trial with event endpoint
- [[packer2025summit-ckd]] — SUMMIT CKD subanalysis (JACC 2025;85:1721): 61% CKD; benefit consistent across CKD/no-CKD (interaction P=0.86); weight loss −13.3% (CKD) and −14.5% (no-CKD) tirzepatide
- [[kramer2025summit-cmr]] — SUMMIT CMR substudy (JACC 2025;85:699): N=106; LV mass −11 g (P=0.004); paracardiac fat −45 mL (P<0.001); first GIP/GLP-1 RA to reduce LV mass in HFpEF by CMR
- [[kosiborod2024stephfpefdm]] — STEP-HFpEF DM (2024): semaglutide in obese HFpEF with T2DM; N=616; KCCQ-CSS +7.3 pts, 6MWD +14.3m, weight −6.4%, CRP ratio 0.67; HF hosp HR 0.40 (nominal); NCT04916470
- [[cleland2006pepchf]] — PEP-CHF: perindopril in elderly HFpEF (LVEF >40%); N=850; HR 0.92 (P=0.55); oldest RAAS trial in HFpEF
- [[solomon2012paramount]] — PARAMOUNT (Phase 2): LCZ696 (ARNi precursor) vs. valsartan in HFpEF; N=301; NT-proBNP −23% at 12 weeks (P=0.005); LA volume improvement at 36 weeks; Phase 2 mechanistic bridge to PARAGON-HF
- [[solomon2024finearts]] — FINEARTS-HF: finerenone vs. placebo in HFmrEF/HFpEF; N=6001; RR 0.84 (95% CI 0.74–0.95; P=0.007) for total WHF events + CV death; first non-steroidal MRA positive trial in HFpEF
- [[vaduganathan2025finegltsecondary]] — FINEARTS-HF SGLT2i-use subgroup (Vaduganathan 2025, Circulation): finerenone benefit consistent regardless of baseline SGLT2i use (RR 0.83 vs. 0.85; P-interaction=0.76); ARR nearly doubled in SGLT2i-treated subgroup
- [[edelmann2013aldodhf]] — ALDO-DHF: spironolactone 25 mg in ambulatory HFpEF; N=422; E/e' improved (P<0.001), LV mass reduced (P=0.009); peak VO₂ and symptoms unchanged; structural-functional dissociation
- [[paulus2013novelparadigm]] — Paulus & Tschöpe 2013 (JACC): foundational HFpEF mechanistic paradigm; comorbidities → systemic inflammation → coronary microvascular endothelial inflammation → ↓NO → ↓cGMP → ↓PKG → titin stiffness + fibrosis → diastolic dysfunction
- [[shah2015phenomapping]] — Shah 2015 (Circulation): first ML phenomapping of HFpEF; N=397+107 validation; 3 phenogroups: young/mild, obese/metabolic, cardiorenal/advanced; HF hospitalisation HR 4.2 for phenogroup 3; validated prospectively
- [[kitzman2016secret]] — SECRET (Kitzman 2016): 2×2 factorial RCT; N=100 obese HFpEF; both caloric restriction and aerobic exercise improved peak VO₂ (+1.2–1.3 mL/kg/min; P<0.001); effects additive; diet improved KCCQ (P=0.004)
- [[edelmann2025exdhf]] — Ex-DHF (Nat Med 2025): n=322 HFpEF, 12-month combined endurance+resistance training; primary Packer composite NOT MET (tau-b=−0.073; P=0.17); VO₂ +1.3 mL/kg/min (P=0.003); NYHA OR 5.89 (P<0.001); adherence ~53%; ISRCTN86879094
- [[mentz2023paraglide]] — PARAGLIDE-HF design (JCF 2023): n=467, LVEF >40%, WHF event; 52% women, 22% Black; median NT-proBNP 2,009 pg/mL; NCT03988634; rationale for post-WHF Sac/Val RCT
- [[abraham2011champion]] — CHAMPION primary results (Lancet 2011): n=550; NYHA III HF (any EF); CardioMEMS PA pressure monitoring; 28% HF hospitalisation reduction (HR 0.72, P=0.0002) at 6 months; foundational RCT for device-based haemodynamic monitoring
- [[adamson2014champion]] — CHAMPION HFpEF subgroup (Circ Heart Fail 2014): n=119 HFpEF (LVEF ≥40%); ~46% HF hospitalisation reduction with PA pressure monitoring; first evidence of meaningful HF hospitalisation reduction specifically in HFpEF
- [[abraham2016champion]] — CHAMPION complete follow-up (Lancet 2016): n=550; CardioMEMS PA pressure monitoring; randomised phase 33% HF admission reduction (HR 0.67, P<0.0001); open-access 48% reduction (HR 0.52, P<0.0001)
- [[pandey2025humain]] — HuMAIN Phase 2A (Circ Heart Fail 2025): HU6 (mitochondrial uncoupler small molecule; **not** Humacyte bioartificial kidney) in HFpEF + obesity; NCT05284617; fat-selective catabolism mechanism
- [[sharif2024locomotor]] — Sharif 2024 (JCF): pilot RCT n=22 HFpEF; 12.5-week resistance training; VO₂peak 17.1→19.4 mL/kg/min; fat-selective improvement; lean mass increased; supports skeletal muscle mechanism
- [[obaya2024aerobic]] — Obaya 2024 (Physiol Res Int): RCT n=40 HFpEF; lower-limb aerobic cycling superior to upper-limb arm ergometry (21.51 vs 19.26 mL/kg/min; P<0.001); LVEF unchanged both arms
- [[borlaug2024inable]] — INABLE-Training (Mayo Clin Proc 2024): N=73, inorganic nitrite 40 mg TID vs. placebo + exercise training; exercise improved VO₂ +0.79, KCCQ, 6MWD; nitrite added no benefit (P=0.77); fifth NO/cGMP negative trial in HFpEF; 75% NYHA III, 63% rural population
- [[brubaker2023secret2]] — SECRET-II (Circ Heart Fail 2023): N=88, CR+AT vs. RT+CR+AT, 20 weeks; both improved VO₂ ~5–7% and KCCQ ~15–20 pts; resistance training added leg strength and muscle quality but NOT additional VO₂ and did NOT prevent skeletal muscle mass loss
- [[alonso2022heartcamp]] — HEART Camp HFpEF subgroup (J Card Fail 2022): N=59 HFpEF; behavioral coaching; adherence 42% vs. 14% at 12 mo, 56% vs. 0% at 18 mo; 6MWT +63 m vs. +13 m (P=0.048); KCCQ all domains improved; HFrEF subgroup: no benefit — HFpEF-specific adherence responsiveness
- [[kitzman2021rehabhf]] — REHAB-HF main results (Kitzman 2021, NEJM): transitional progressive multidomain rehab in 349 acute HF patients (any EF; ≥60y; 97% frail); SPPB +1.5 pts (P<0.001); 6MWD +34 m; 60-day rehospitalisation NS; NCT02196038
- [[mentz2021rehabhfhfpef]] — REHAB-HF HFpEF subgroup (Mentz 2021, JACC HF): HFpEF arm SPPB +1.9 vs. HFrEF +1.1; global rank endpoint significant in HFpEF (P=0.04) not HFrEF (P=0.69); interaction P=0.098
- [[mueller2021optimex]] — OptimEx-Clin (Mueller 2021, JAMA): HIIT vs. MCT vs. guideline control in HFpEF (N=180, 5 European sites); HIIT = MCT at 3 and 12 months; neither met MCID; gains not sustained at 12 months; closes the HIIT superiority debate
- [[donelli2020hiit]] — DonelliDaSilveira 2020 (Eur J Prev Cardiol): N=19 single-centre RCT; HIIT +3.5 vs. MCT +1.9 mL/kg/min (P<0.001 between-group); likely false positive; contradicted by OptimEx-Clin (N=180)
- [[azhar2020protein]] — Azhar 2020 (Gerontol Geriatr Med): protein supplementation ± exercise pilot in HFpEF (N=16 analysed); combined arm: 6MWD +36.6 m, quadriceps strength +21.5 kg; PS alone: no functional benefit, increased body fat
- [[ponikowski2020affirm]] — AFFIRM-AHF (Ponikowski 2020; Lancet; N=1,132; HFrEF LVEF <50%): IV ferric carboxymaltose vs. placebo after acute HF + iron deficiency; primary composite HR RR 0.79 (P=0.059, NS overall); total HFH RR 0.74 (P=0.013); CV death NS; pre-COVID analysis positive (P=0.024); NOTE: HFrEF population — relevant context for FAIR-HFpEF
- [[rillig2021eastafnet4]] — EAST-AFNET4 HF subgroup (Rillig 2021; Circulation; N=798 HF): early rhythm control vs. usual care in AF+HF; primary composite HR 0.74 (95% CI 0.56–0.97; P=0.03); HFpEF subgroup N=442 (56.3%); no interaction by HF type (P=0.63); supports rhythm control benefit in HFpEF+AF
- [[lindenfeld2021guidehf]] — GUIDE-HF (Lindenfeld 2021; Lancet; N=1,000; all EF): CardioMEMS PA pressure-guided management; primary composite HR 0.88 (P=0.16, NS); pre-COVID HR 0.81 (P=0.049); HFpEF subgroup (LVEF >40%, N=469) HR 0.85 (P=0.28); COVID-19 confounded the trial
- [[vonhaehling2024fair]] — FAIR-HFpEF (von Haehling 2024; Eur Heart J; N=40, stopped early): first RCT of IV iron in HFpEF with iron deficiency; FCM vs. placebo; 6MWT difference +49 m at week 24 (P=0.029); +65 m vs. −8 m at week 32; SAEs fewer with FCM (5 vs. 19; rate ratio 0.27; P=0.043); underpowered but directionally positive
- [[babb2026ventilatorylimit]] — Babb 2026 (Respir Physiol Neurobiol; NCT04068844; N=42 obese HFpEF): NTG 400 μg SL vs. placebo crossover; NTG confirmed to lower PCWP and CO (both P<0.01) but did NOT change exercise capacity, breathing mechanics, or lung volumes; EELV R²=0.96 before vs. after NTG; paradigm-shifting: exercise is ventilatory-limited, not cardiac-limited, in obese HFpEF
- [[backhaus2021hfpefstress]] — HFpEF-Stress trial (Backhaus 2021, Circulation; NCT03260621; N=75/68 analysed): real-time exercise-stress CMR vs. invasive RHC; exercise LA long-axis strain AUC 0.93, best noninvasive discriminator tested, outperforming NT-proBNP/E-e'/H₂FPEF/HFA-PEFF
- [[rommel2016stiffmap]] — STIFFMAP (Rommel 2016, JACC; NCT02459626; N=36): CMR ECV vs. invasive pressure-volume-loop LV stiffness; ECV independently predicts stiffness constant β (r=0.75); splits HFpEF into fibrosis-dominant vs. relaxation-dominant subphenotypes
- [[capone2026hfpefpht]] — HFpEF-PHT (Capone 2026, Cardiovasc Res; NCT05055180; N=23 biopsy sub-cohort): LV endomyocardial-biopsy multi-omics; blocked proximal glycolysis, succinate accumulation, energy deprivation, EFEMP1-led ECM/fibrosis upregulation, all obesity-independent
- [[landsteiner2026multiorgan]] — Landsteiner 2026 multiorgan deficits (Circulation; N=820 iCPET + N=6,345 MESA): 7 exercise physiological deficits; ≥5 deficits HR 3.90 for CV hospitalisation/mortality; metabolomic signatures + TWAS gene prioritisation; largest invasive CPET HFpEF cohort to date
- [[stone2024relievehf]] — RELIEVE-HF (Stone 2024, Circulation; NCT03499236; N=508): sham-controlled interatrial shunt trial, any LVEF; safe, neutral overall; preserved-LVEF stratum harmed (all-cause death HR 3.24); reduced-LVEF stratum trended toward benefit
- [[ferreira2025sogaldipef]] — SOGALDI-PEF (Ferreira 2025, JACC Heart Fail; NCT05676684; N=108): dapagliflozin ± spironolactone crossover in HFmrEF/HFpEF; combination reduced NT-proBNP 11% more than monotherapy (P=0.035); greater eGFR decline/hyperkalemia trade-off

### Review Articles
- [[yi2025ai]] — Yi 2025 (J Cardiol): systematic review of 38 AI/ML studies in HFpEF; ECG-AI AUC 0.87; NLP identifies 75.4% undiagnosed; ML spironolactone responders reframe TOPCAT as enrichment failure
- [[pfeffer2019hfpef]] — Pfeffer 2019 (Circ Res): invited perspective by Pfeffer/Shah/Borlaug; pathophysiologic cascade (Figure 2); cGMP/PKG cellular mechanism; ATTR 13–19% in HFpEF; trial landscape review including PEP-CHF; CHAMPION trial; SECRET trial; prevention (SPRINT)
- [[damario2019cmd]] — D'Amario 2019 (Front. Physiol.): CMD as "common soil" for HFpEF; Figure 1 comorbidity→inflammation→EndoMT→HFpEF cascade; titin N2BA→N2B isoform shift; calcium overload; OSA RR 2.2; statins as emerging therapy; anti-IL-1; PDE-9 inhibition; anti-fibrotic approaches
- [[bohmke2022nonpharm]] — Bohmke 2022 (Cardiol Clin): narrative review of 4 exercise modalities (MCT, HIIT, combined resistance/aerobic, IMT) + dietary interventions (CR, sodium, MedDiet, DASH, malnutrition); IMT +2.9 mL/kg/min VO₂peak; OPTIMEX-CLIN HIIT=MCT; SECRET CR additive to exercise
- [[manabe2023sympathetic]] — Manabe 2023 (Front Cardiovasc Med): mini review; MSNA paradoxical increase in HFpEF during dynamic cycling; static exercise MSNA resembles controls; LBF/LVC reduced; functional sympatholysis gap identified as major knowledge gap
- [[khidihir2026finerenone]] — Khidihir & Kalra 2026 (Curr Atheroscler Rep): finerenone pharmacology and CKM-context review; FINE-HEART AF reduction (HR 0.83); SGLT2i co-administration hyperkalemia-neutral; retrospective finerenone-vs-spironolactone comparison; 3 new ongoing mechanistic trials (FINE-FOCUS, FINE-REMODEL, FINE-MECH)
- [[zeid2025myomobile]] — Zeid 2025 (EHJ Digital Health): MyoMobile study design; 3-arm EE2 RCT; N=185 HFpEF; step count primary endpoint; NCT04940312; DZHK Rhine-Main; baseline characteristics; **primary results published** [[zeid2026myomobile]]
- [[ipek2024cmr]] — Ipek 2024 (EHJ Cardiovasc Imaging): comprehensive CMR review in HFpEF; covers FT-CMR strain, LGE, ECV, T1/T2, perfusion (CFR), spectroscopy (31P-MRS, 1H-MRS), exercise CMR; LACI as HFpEF severity marker
- [[fayyaz2025pathophys]] — Fayyaz 2025 (Nat Rev Cardiol 22:90–104): systematic review of 56 human myocardial tissue studies in HFpEF; 8-pathway framework (fibrosis, hypertrophy, microvascular rarefaction, diastolic dysfunction [titin/SERCA2a/T-tubule], metabolic [ATP/NAD⁺ deficit], inflammation/ROS, cGMP-PKG impairment, ER stress/DNA damage); comorbidity-dependent heterogeneity explains monotherapy failure
- [[carbone2024inflammation]] — Carbone 2024 (JACC Heart Fail 12:1270–1273; editorial): inflammation-obesity-CRF triad in HFpEF; adipose-derived cytokines impair skeletal muscle mitochondria; GLP-1RA + SGLT2i reduce adipose-driven inflammation + improve CRF; explains why targeted IL-1 blockade (D-HART2) fails while GLP-1RA succeeds
- [[requenaibanez2022sglt2]] — Requena-Ibáñez 2022 (Cardiovasc Drugs Ther 2023;37:989–996): narrative review of SGLT2i mechanisms across HF EF spectrum; EAT/pericardial restraint reduction mechanism; fibrosis attenuation; EMPEROR-Preserved LVEF >60% attenuation signal; phenotype-based vs. EF-based patient selection argument; CMR to reduce EF measurement variability in trials
- [[morfino2022biomarkers]] — Morfino 2022 (J Cardiovasc Dev Dis 2022;9:256): comprehensive HFpEF biomarker review; six pathways (NP, fibrosis, inflammation, endothelial, adipokine, metabolic/renal); NPs AUC 0.80 (51 studies); hs-TnT sex differences (men HR 3.33, women HR 1.35); sST2 RV not LV geometry; Galectin-3 AUC 0.927 (cut-off 10.1 ng/mL); GDF-15 not AF-dependent — best prognostic in acute HFpEF panel; six-pathway biomarker map (Figure 1)
- [[achten2025screening]] — Achten 2025 (Heart Fail Rev 2025;30:1207–1213): HFpEF screening in obesity rationale; HFpEF onset one decade earlier in obese; 20% cardiac structural changes at 15y obesity, 95% at 25y; NT-proBNP sensitivity 77%→67% at BMI >35 (downward adjustment needed); height²-indexing for echo volumes; HFpEF-ABA score; stepwise HFpEF-ABA→NP→echo algorithm; SGLT2i consistent across BMI; tirzepatide SUMMIT HR 0.62; open question: prospective prevalence of early HFpEF in asymptomatic obese
- [[upadhya2025echo]] — Upadhya 2025 (Heart Fail Rev 30:899–922; Duke): comprehensive echocardiography review in HFpEF; H₂FPEF sens 52.7%, HFA-PEFF 70%; LASr <18% as third criterion in ASE/EACVI 2016 → 99% classification; LA min LAV better reflects chronic LVFP; 6 HFpEF mimicker patterns (amyloid, HCM, Fabry, constrictive, stiff LA, precapillary PAH); 5 TTE phenotype signatures; LVEF U-shaped mortality (nadir 60–65%)
- [[hage2026ntprobnp]] — Hage 2026 (Int J Cardiol 458:134554; Karolinska/Roche): NT-proBNP glycosylation at Thr-71 causes standard Elecsys assay to underdetect true NP in HFpEF; NT-proBNP/tNT-proBNP ratio 0.27 (HFpEF) vs 0.32 (HFrEF; P=0.019) — HFpEF has more glycosylation; tNT-proBNP independently prognostic in HFpEF (HR 1.77; p=0.022) while standard NT-proBNP loses significance after eGFR adjustment; research-use-only assay
- [[attia2019ecgaf]] — Attia 2019 (Lancet): CNN ECG-AI for AF detection in patients in sinus rhythm; AUC 0.87; **NOT an HFpEF study** — methodological precursor to ECG-AI screening in HFpEF
- [[cowie2017sdb]] — Cowie 2017 (JACC HF): state-of-the-art review of SDB in HF; SDB prevalence 50–75% in HF; CSA vs. OSA mechanism dichotomy; SERVE-HF: ASV increased CV mortality in HFrEF+CSA (HR 1.28); CAT-HF stopped; treatment landscape: CPAP/BiPAP/ASV; clinical management algorithm
- [[horiuchi2022npguided]] — Horiuchi 2022 (Heart International): review; NP-guided therapy benefits HFrEF <75y (BATTLESCARRED, TIME-CHF) but NOT HFpEF; TIME-CHF HFpEF subgroup trended to worsen; GUIDE-IT neutral; meta-analyses show no benefit or trend to harm in HFpEF; challenges NT-proBNP titration paradigm in HFpEF
- [[wester2023sdb]] — Wester 2023 (Biomedicines; Regensburg/UT Southwestern): SDB 58–80% in HFpEF; three HFpEF phenotypes (older vascular ~45%, metabolic obese ~30%, younger NP-deficient ~25%); CaMKII pathway: intermittent hypoxia → ↑ROS → CaMKII oxidation → Na⁺/Ca²⁺ dysregulation → diastolic SR Ca²⁺ leak → atrial arrhythmias → HFpEF; treatment: PAP therapy, GLP-1RA, SGLT2i; ACE2 sex-specific pathway
- [[timoteo2024eat]] — Timóteo 2024 (Int J Cardiol): EAT in HFpEF review; two pathways: (1) pericardial restraint → ↑LVEDP; (2) paracrine dysfunction: TNF-α/IL-1β/IL-6/leptin → fibrosis/inflammation/microvascular dysfunction/AF; CT preferred for EAT volume measurement; treatment targets: statins, SGLT2i, GLP-1RA, pericardiotomy pilot
- [[ilonze2024disparities]] — Ilonze 2024 (Curr Cardiovasc Risk Rep; review): racial/ethnic disparities across HFpEF care continuum; Black patients: 7.4/1,000 PY first HFH (highest); 20–35% have low BNP despite elevated PCWP; ATTR V122I in 3.43% of Black Americans ≥60y; H2FPEF score underdiagnoses Black patients; SGLT2i + GLP-1RA underutilised in minority patients; SDOH framework
- [[giannitsi2019sixmwt]] — Giannitsi 2019 (Ther Adv Cardiovasc Dis 13:1–10): narrative review of 6MWT in HF; ATS/ERS-standardised protocol (≥30m corridor, 3m course marking, standardised encouragement phrasing); CPET rationale (cost/equipment/training/availability vs. patient cooperation); 6MWD-peak VO₂ correlations (r=0.28–0.81); prognostic thresholds (≤300m poor prognosis, <200m markedly increased mortality); intervention-response evidence (CRT, IV iron, sacubitril/valsartan, MitraClip); calls for HFpEF-specific MCID/prognostic validation
- [[bilbao2016mlhf]] — Bilbao 2016 (Health Qual Life Outcomes 14:23): MLHFQ factor-structure validation (N=2,565, 13 Spanish hospitals); confirms two-factor physical/emotional structure (21 items, 0–105 range: physical 8 items 0–40, emotional 5 items 0–25); also validates a third "social" subscale
- [[spertus2020kccq]] — Spertus 2020 (J Am Coll Cardiol 76:2379–2390): "Interpreting the KCCQ" state-of-the-art review; 23 items → 7 domains (symptom frequency/burden/stability, physical/social limitation, QoL, self-efficacy); TSS/CSS/OSS construction; 5/10/20-point MCID thresholds (anchor-based, Spertus 2005); FDA Clinical Outcome Assessment qualification (not a guideline endorsement)

### Systematic Reviews and Meta-Analyses
- [[masri2026attrcm]] — Masri 2026 (Prog Cardiovasc Dis pre-proof): ATTR-CM trials systematic review; covers tafamidis (ATTR-ACT), acoramidis (ATTRibute-CM), patisiran (APOLLO-B), vutrisiran (HELIOS-B; HR 0.72, P<0.001), eplontersen; multiple approved/approvable options; early treatment maximises benefit; ATTR-CM now fully tractable as HFpEF subphenotype
- [[jin2022la]] — Jin 2022 (Heart Fail Rev): 61 studies (8,806 HFrEF + 9,928 HFpEF); LA global longitudinal strain markedly worse in HFrEF (LAGLS_R 9–12.8%) vs. HFpEF (18.9–23.4%); AF 34–43% in HFpEF despite better LA function
- [[lin2023cmd]] — Lin 2023 (Heart Fail Rev): 10 studies, 1,267 patients; pooled CMD prevalence 71% in HFpEF (invasive 79%; non-invasive 66%); CFR lower by −1.28 vs. controls; CMD risk 2.21× higher in HFpEF than controls
- [[kaddoura2024betablocker]] — Kaddoura 2024 (Curr Probl Cardiol): 16 observational studies (27,188 patients); beta-blockers in HFpEF: all-cause mortality OR 0.81 (95% CI 0.65–0.99; P=0.044); HF rehospitalisation NS; predominantly observational evidence
- [[fu2024inflammation]] — Fu 2024 (Front Cardiovasc Med): 8 cohort studies (9,744 patients); inflammatory markers in HFpEF: all-cause mortality HR 1.43; CV mortality HR 2.04; CV rehospitalisation HR 2.83; I²=0% throughout
- [[lee2024lifestyle]] — Lee 2024 (Heart Lung Circ): 6 RCTs (375 patients); lifestyle interventions in HFpEF: body weight −5.30 kg (P=0.002); 6MWD +43.63 m (P<0.001); NYHA −0.54; MLHFQ −17.77 (P<0.001)
- [[prokopidis2025exercise]] — Prokopidis 2025 (Eur Heart J Open): 46 studies; exercise capacity HFpEF vs. HFrEF comparison; VO₂peak higher in HFpEF by 0.78 mL/kg/min (P=0.02; NS after comorbidity adjustment); CO and SV higher in HFpEF
- [[vandebovenkamp2025hemodynamics]] — van de Bovenkamp 2025 (Am J Physiol Heart Circ Physiol): 21 RCTs; pharmacological reverse remodeling in HFpEF essentially absent vs. robust in HFrEF; SV not increased; LV volumes unchanged; LVMi −2.8 g/m²
- [[ammar2025bnp]] — Ammar 2025 (Heart Fail Rev): 22 studies (10,158 patients); BNP/NT-proBNP in HFpEF: adverse events HR 1.34–1.80; CV mortality HR 1.44–1.65; low BNP = poor prognosis in HFpEF (inverse of HFrEF pattern)
- [[minisy2025sglt2]] — Minisy 2025 (BMC Cardiovasc Disord 25:765): 9 RCTs, >20,000 patients; CV death/HHF HR 0.83 (0.76–0.90; GRADE high); HHF alone HR 0.75 (GRADE high); mortality HR 0.92 (NS; GRADE low); KCCQ +1.8 pts; I²=62%; no publication bias; most comprehensive SGLT2i class-effect estimate in HFpEF
- [[beale2019iron]] — Beale 2019 (Open Heart; PROSPERO 42017069896): 15 studies, N=1,877 HFpEF; iron deficiency prevalence 59% (95% CI 52–65%); functional ID 34%; absolute ID 30%; ID associated with worse VO₂ max, 6MWT, QoL; no RCT evidence in HFpEF at time of publication; anticipated FAIR-HFpEF
- [[shi2022sst2]] — Shi 2022 (Front Cardiovasc Med): 16 studies, N=2,761 HFpEF; sST2 AUC <0.7 for HFpEF diagnosis (inferior to NT-proBNP); prognostic: log sST2 HR 2.76 for all-cause death (I²=0%; P=0.013); composite HR 6.52 (P<0.001); sST2 as outcome biomarker, not diagnostic
- [[alsadawi2022rhythmcontrol]] — Al-Sadawi 2022 (Heart Rhythm O²): 5 studies, N=16,825 HFpEF+AF; rhythm control vs. rate control: OR 0.735 for adverse outcomes (95% CI 0.665–0.813; P<0.001); I²=0%; 4/5 studies used catheter ablation; supports rhythm control in HFpEF+AF

### Secondary Analyses
- [[merrill2019topcat]] — TOPCAT sex differences secondary analysis (JACC Heart Fail 2019): N=3,445; women: higher LVEF (~63% vs. ~58%), less CAD, more hypertension; spironolactone sex×treatment interaction P=0.26 (NS); no sex-differential MRA response
- [[gori2021paragon]] — PARAGON-HF biomarker study (JACC Heart Fail 2021;9:627–635): N=1,260 HFpEF; hs-TnT >14 ng/L in 58.3%; HR 1.38 per doubling for primary composite; Sac/Val reduced hs-TnT by 9–10% vs. valsartan; threshold 17 ng/L for outcomes prediction; P interaction NS for TnT-modified Sac/Val benefit
- [[ferreira2023spironolactone]] — Spironolactone echocardiographic IPD meta-analysis (Eur J Heart Fail 2023;25:108–113): N=984 (HOMAGE+Aldo-DHF+TOPCAT Americas); LAVi −1.1 mL/m² (P=0.03); LVMi −3.6 g/m² (P=0.01); IVS −0.2 cm (P=0.01); E/e' −1.3 (P=0.02; heterogeneity P<0.01); LVEF +1.7% (P<0.01); mechanistic rationale for SPIRRIT-HFpEF and SPIRIT-HF
- [[petrie2024stephfpef]] — STEP-HFpEF program NT-proBNP analysis (JACC 2024;84:27–40): N=1,145 pooled; semaglutide reduced NT-proBNP ETR 0.82 (P=0.0002); weight-loss-independent (P interaction=0.58); KCCQ-CSS T3 (+11.9 pts vs. T1 +4.5 pts; P=0.02); win ratio T3 2.17 vs. T1 1.45 (P=0.04); direct HF disease-modifying mechanism
- [[turgeon2025finearts]] — Turgeon & Beavers 2025 (J Card Fail; 3-page editorial): Bayesian re-analysis of TOPCAT using FINEARTS-HF as strong prior; posterior HR 0.87 (0.79–0.94) for TOPCAT overall; P(HR<1) = 100%; P(HR<0.95) = 98%; restores spironolactone class confidence; $0.15/day vs. $3.61/day finerenone — cost equity argument
- [[docherty2025determine]] — Docherty 2025 (JCF): DETERMINE accelerometry substudy; accelerometer/KCCQ/6MWD measure distinct dimensions; weak cross-correlations
- [[pfeffer2022topcat]] — Pfeffer 2022 (Circulation): TOPCAT Americas post-hoc reanalysis; Americas HR 0.82 (0.69–0.98, P=0.04); canrenone undetectable in 30% Russian/Georgian patients; FDA advisory 8:4:1 vote; basis for spironolactone Class IIb Level B in HFpEF
- [[verma2024inflammation]] — Verma 2024: STEP-HFpEF inflammation sub-analysis; semaglutide benefit CRP-independent; confirms inflammation heterogeneity in HFpEF
- [[fudim2024paraglide]] — PARAGLIDE-HF symptomatic hypotension analysis (JCF 2024): Sac/Val 24.0% vs Val 15.5% (P=0.020); predictors: LVEF >60%, lower SBP, white race; clinically actionable safety signal
- [[nouhravesh2025paraglide]] — PARAGLIDE-HF initiation setting (JAHA 2025): no difference in-hospital vs out-of-hospital initiation (P-interaction=0.99); Sac/Val safe to initiate in either setting
- [[rambarat2025paraglide]] — PARAGLIDE-HF sex analysis (AHJ 2025): NT-proBNP benefit consistent by sex (P-interaction=0.908); women excess symptomatic hypotension (OR 2.29, P=0.012); higher LVEF + worse eGFR in women
- [[patel2024reducelaphf]] — REDUCE LAP-HF II echocardiographic substudy (JAMA Cardiol 2024): n=621; LV EDV −5.65 mL (P<0.001); LA EF +1.88 pp (P=0.02); RV EDV +9.58 mL (P<0.001); PVR subgroup interaction P=0.01 for RV changes; RV systolic function unchanged
- [[chaudhary2025worseninghf]] — REDUCE LAP-HF II expanded worsening-HF (WHF) definition analysis (JACC Heart Fail 2025;13(9):102571): n=621; 3-tier hierarchical WHF taxonomy (hospitalisation/urgent outpatient/nonurgent outpatient diuretic escalation); expanding definition raised incidence 17.4%→25.9% and turned nonsignificant responder-subgroup shunt effect significant (RR 0.56, P=0.009); level 1 alone predicted mortality (HR 3.54) at least as strongly as expanded "any WHF" (HR 2.60) — power gain without added mortality specificity
- [[litwin2024reducelaphf]] — REDUCE LAP-HF I/II 3-year/5-year follow-up (Am Heart J 2024;278:106–116): overall trial neutral through 3 years (win ratio 1.04, 95% CI 0.83–1.30); responder subgroup (PVR ≤1.74 WU, no CRM device) benefit durable/strengthening: win ratio 1.6, 44% HF-event reduction, KCCQ +10.1 pts
- [[doi2026reducelaphf]] — REDUCE LAP-HF II insights: HF duration/remodeling/hemodynamic severity (JACC Heart Fail 2026;103167): no significant effect on primary composite in overall population; HF diagnosis duration >3y associated with worse shunt outcomes (HR 1.72, P=0.001), interaction test NS
- [[berk2025patisiran]] — Patisiran post hoc APOLLO-B functional-capacity analysis (JACC Adv 2025;4(8):101876): MCID 6.9–7.8m 6MWT; ADL/KCCQ-OS treatment-response detail; explicit regulatory-status statement — patisiran NOT FDA-approved for cardiac ATTR-CM indication (approved Brazil; compassionate-use only in France, tafamidis 61mg failures) — resolves prior wiki contradiction

### Trial Design Papers
- [[vantassell2017dhart2]] — D-HART2 design (Clin Cardiol 2017): anakinra (IL-1 receptor antagonist) 24 weeks in HFpEF enriched for hs-CRP >2 mg/L; primary CRP AUC endpoint; rationale: Paulus–Tschöpe IL-1→diastolic dysfunction cascade
- [[desai2011topcat]] — TOPCAT design paper: eligibility, dual enrollment pathway (hospitalization/NP), 266 centers/6 countries, spironolactone titration schema, parameters collected
- [[lund2024spirrit]] — SPIRRIT-HFpEF design (Eur J Heart Fail 2024;26:2453–2463; NCT02901184): first registry-based RCT (RRCT) in chronic HF; SwedeHF + US TIN platforms; spironolactone/eplerenone vs. usual care; LVEF ≥40%; ~2,200 enrolled mid-2024; protocol amended to total recurrent events; design paper confirms RRCT concept validity

---

## Entities

### HF Phenotypes
- [[hfpef]] — Heart failure with preserved ejection fraction (LVEF ≥50%); central entity of this wiki
- [[hfmref]] — Heart failure with mildly reduced ejection fraction (LVEF 41–49%); renamed from 'mid-range' in 2021; heterogeneous
- [[hfref]] — Heart failure with reduced ejection fraction (LVEF ≤40%); four-pillar treatment with proven mortality benefit

### Pharmacological Entities
- [[sglt2-inhibitors]] — Dapagliflozin/empagliflozin; Class I for HFrEF; first proven HFpEF therapy (EMPEROR-Preserved, DELIVER — post-2021 cutoff)
- [[sacubitril-valsartan]] — ARNI; Class I for HFrEF; FDA-endorsed for LVEF below normal based on PARAGON-HF subgroup; no ESC HFpEF recommendation
- [[spironolactone]] — MRA; Class I for HFrEF; TOPCAT Americas subgroup positive in HFpEF; overall trial neutral
- [[balcinrenone]] — Selective MR modulator (distinct from sMRA and nsMRA); Phase 2 MIRACLE neutral on UACR endpoint (N=133, all 3 doses); Phase 3 BALANCED-HF (~N=4,800, dapagliflozin combination) ongoing; no regulatory approval
- [[vicadrostat]] — Aldosterone synthase inhibitor (CYP11B2 inhibitor); acts upstream of MR to suppress aldosterone synthesis; Phase 3 EASi-HF (~N=6,000, empagliflozin combination, EF ≥40%) ongoing; no regulatory approval
- [[semaglutide-hfpef]] — GLP-1RA; STEP-HFpEF/STEP-HFpEF DM; NT-proBNP reduction independent of weight loss; CRP reduction
- [[sgc-stimulators]] — Vericiguat + praliciguat drug class; SOCRATES-PRESERVED, VITALITY-HFpEF, CAPACITY-HFpEF all neutral/harmful in HFpEF
- [[statins]] — Mechanistic (D'Amario 2019 biopsy/PKG data) + observational (RICA registry HR 0.74) evidence; no dedicated RCT in HFpEF
- [[ranolazine]] — Late I_Na inhibitor; RALI-DHF proof-of-concept (exercise LVEDP −4.7 mmHg); no Phase 3 follow-up
- [[tolvaptan]] — V2-receptor antagonist/aquaretic; guideline recommendations vary (CCS/CHFS, JCS/JHFS formal; others discuss without recommending)
- [[acetazolamide]] — Carbonic-anhydrase-inhibitor diuretic adjunct; SHA sole formal recommendation; ESC notes need for further data

### Clinical Trial Entities
- [[paragon-hf]] — Sacubitril/valsartan vs. valsartan in HFpEF; missed primary endpoint; LVEF <57% subgroup signal; FDA label
- [[topcat]] — Spironolactone vs. placebo in HFpEF; neutral overall; Americas subgroup positive; enrollment controversy
- [[charm-preserved]] — Candesartan vs. placebo in HF LVEF >40%; missed primary endpoint; hospitalization trend
- [[i-preserve]] — Irbesartan vs. placebo in HFpEF; fully neutral; most definitively negative RAAS trial in HFpEF
- [[finearts-hf]] — Finerenone (non-steroidal MRA) in HFpEF/HFmrEF; LVEF ≥40%; N=6001; RR 0.84 (95% CI 0.74–0.95; P=0.007); first non-SGLT2i pharmacological positive trial in HFpEF
- [[aldo-dhf]] — Spironolactone 25 mg in ambulatory HFpEF; N=422; E/e' improved, LV mass reduced; exercise capacity + symptoms unchanged; structural-functional dissociation
- [[secret]] — 2×2 factorial RCT; N=100 obese HFpEF; caloric restriction + exercise both improve peak VO₂; additive; diet improves KCCQ +7 pts; MLHF QoL not met
- [[relax]] — Sildenafil (PDE5i) in HFpEF; N=216; fully neutral; part of NO/cGMP failure series
- [[attr-act]] — Tafamidis in ATTR cardiomyopathy; N=441; mortality RR 0.70; first disease-modifying therapy for critical HFpEF subphenotype
- [[pep-chf]] — Perindopril in elderly HFpEF; N=850; HR 0.92 neutral; oldest RAAS trial; high drug discontinuation
- [[victoria]] — Vericiguat in HFrEF; HR 0.90 positive; contrast with neutral VITALITY-HFpEF (same drug, HFpEF)
- [[socrates-preserved]] — Vericiguat phase 2b in HFpEF; NT-proBNP signal; motivated VITALITY-HFpEF (then neutral)
- [[vitality-hfpef]] — VITALITY-HFpEF: vericiguat 15 mg or 10 mg vs. placebo in HFpEF (LVEF ≥45%); N=789; KCCQ-PLS neutral (P=0.47/0.80); large placebo response; closes sGC stimulator class for HFpEF
- [[step-hfpef]] — Semaglutide 2.4 mg in obese HFpEF without T2DM; N=529; KCCQ-CSS +7.8 pts, body weight −10.7 pp, 6MWD +20.3m, win ratio 1.72 (all P<0.001); first published large GLP-1RA trial in HFpEF
- [[strong-hf]] — High-intensity GDMT uptitration in acute HF; ~8% absolute RRR 180-day events; ESC 2023 Class I
- [[empulse]] — Empagliflozin in-hospital initiation in acute HF; win ratio 1.36; safety established across LVEF
- [[summit]] — Tirzepatide (GLP-1/GIP dual agonist; Eli Lilly) in obese HFpEF; N=731; co-primary KCCQ-CSS + CV death/worsening HF; HR 0.62 (P=0.026); KCCQ +6.9 pts; first HFpEF trial showing event reduction with GLP-1RA class; published NEJM 2025; NCT04847557
- [[tirzepatide-hfpef]] — Redirect → [[summit]]; tirzepatide HFpEF = SUMMIT (NCT04847557; Eli Lilly); NCT04788511 belongs to STEP-HFpEF (semaglutide)
- [[spirit-hf]] — Spironolactone in HFpEF; NCT04727073; ongoing; aims to resolve TOPCAT contamination controversy
- [[spirrit]] — Spironolactone vs. usual care in HFpEF; NCT02901184; ongoing; MRA definitiveness trial
- [[caba-hfpef]] — Catheter ablation vs. rate control in HFpEF with AF; NCT05508256; DZHK; ongoing
- [[fair-hfpef]] — FAIR-HFpEF: IV ferric carboxymaltose vs. placebo in HFpEF with iron deficiency; NCT03074591; N=40 (stopped early); published Eur Heart J 2024; 6MWT +49m (P=0.029); SAEs fewer with FCM; underpowered — preliminary
- [[reduce-lap-hf-ii]] — Interatrial shunt device in HFpEF; NCT03088033; overall neutral; PVR subgroup signal
- [[sota-p-cardia]] — Sotagliflozin (SGLT2+SGLT1) in HFpEF without T2DM; NCT05562063; ongoing
- [[rehab-hfpef]] — Cardiac rehabilitation in HFpEF; NCT05525663; ongoing; addresses CR evidence gap
- [[myomobile]] — MyoMobile: app-based PA coaching in HFpEF; NCT04940312; DZHK Rhine-Main; N=185; PUBLISHED JACC Heart Fail 2026 — step count improved, secondary KCCQ + 6MWT; first positive digital health RCT in HFpEF
- [[paraglide-hf]] — PARAGLIDE-HF (NCT03988634): sacubitril/valsartan vs. valsartan in 467 post-WHF HFpEF patients (LVEF >40%); NT-proBNP ratio 0.85 (0.73–0.999); LVEF ≤60% subgroup drives benefit; 52% women, 22% Black; SH signal (24.0% vs 15.5%)
- [[rehab-hf]] — REHAB-HF (NCT02196038): transitional progressive multidomain rehabilitation in acute HF (any EF; ≥60y; N=349); SPPB improved; HFpEF subgroup benefits more than HFrEF on global rank endpoint; rehospitalisation not reduced
- [[optimex-clin]] — OptimEx-Clin (NCT02078947): HIIT vs. MCT vs. guideline control in HFpEF (5 sites; N=180); HIIT not superior to MCT; exercise gains not sustained at 12 months with telemedical supervision
- [[train-hfpef-ph]] — TRAIN-HFpEF-PH (NCT05464238): standardized low-intensity exercise + respiratory rehabilitation vs. standard care in HFpEF with invasively confirmed pulmonary hypertension; N=90 (target); design published 2023, ongoing
- [[rebalance-hf]] — REBALANCE-HF (NCT04592445): endovascular splanchnic nerve ablation vs. sham in HFpEF; exercise PCWP −5.4 mmHg (P=0.003); KCCQ improved; first sham-controlled RCT for neural preload reduction; JAMA Cardiol 2024
- [[emperor-preserved]] — Empagliflozin outcome trial; HR ~0.79 for CV death/HFH; first major positive HFpEF RCT
- [[deliver]] — Dapagliflozin outcome trial; co-pivotal with EMPEROR-Preserved establishing SGLT2i class effect across EF spectrum
- [[guide-hf]] — CardioMEMS haemodynamic-guided management; primary composite HR 0.88 (NS); pre-COVID sensitivity HR 0.81 (P=0.049)
- [[neat-hfpef]] — Isosorbide mononitrate crossover RCT; neutral/harm signal; part of NO/cGMP-pathway failure cluster
- [[indie-hfpef]] — Inorganic nitrate (KNO₃) RCT; neutral; companion trial to NEAT-HFpEF
- [[capacity-hfpef]] — Praliciguat RCT; neutral; published simultaneously with VITALITY-HFpEF
- [[ex-dhf]] — Combined endurance+resistance training RCT (N=322); Packer composite not met (P=0.17) despite VO2/NYHA benefit
- [[serve-hf]] — Adaptive servo-ventilation in HFrEF+CSA; increased all-cause (HR 1.13) and CV mortality (HR 1.34); ASV contraindication established
- [[soloist-whf]] — Sotagliflozin in T2DM + worsening HF; effect consistent across EF but underpowered for HFpEF; stopped early (COVID funding)
- [[diamond-hfpef]] — CMR+invasive coronary physiology study; MPR/ECV uncorrelated (r=−0.06); CMD and fibrosis as independent axes
- [[responder-hf]] — Ongoing atrial-shunt trial (NCT05233358); successor to REDUCE LAP-HF II, PVR-defined "responder" phenotype only
- [[homage-trial]] — Stage B (pre-HF) spironolactone RCT; contributed IPD to pooled echo remodeling analysis
- [[paramount-trial]] — LCZ696 (sacubitril/valsartan precursor) Phase 2 predecessor to PARAGON-HF; NT-proBNP + LA dimension improvement
- [[heart-camp]] — Behavioral exercise-adherence coaching RCT; HFpEF subgroup (N=59) secondary analysis
- [[hfpef-stress-trial]] — HFpEF-Stress (NCT03260621): real-time exercise-stress CMR vs. invasive RHC; N=75/68; exercise LA long-axis strain AUC 0.93, best noninvasive discriminator tested
- [[stiffmap]] — STIFFMAP (NCT02459626): CMR ECV vs. invasive pressure-volume loops; N=36; ECV independently predicts LV stiffness constant β (r=0.75); fibrosis-dominant vs. relaxation-dominant subphenotypes
- [[hfpef-pht]] — HFpEF-PHT (NCT05055180): Leipzig Heart Center LV endomyocardial-biopsy cohort; N=23 (19 HFpEF/4 NFO); multi-omics results in [[capone2026hfpefpht]]
- [[relieve-hf]] — RELIEVE-HF (NCT03499236): sham-controlled interatrial shunt, any LVEF; N=508; safe, neutral overall; preserved-LVEF stratum harmed (mortality HR 3.24), reduced-LVEF stratum trended toward benefit
- [[sogaldi-pef]] — SOGALDI-PEF (NCT05676684): dapagliflozin ± spironolactone crossover; N=108; combination reduced NT-proBNP 11% more than monotherapy; first dedicated SGLT2i+MRA combination RCT in HFpEF/HFmrEF

### Registry-Only Trial Entities (no results paper yet — see [[trials-pending]] Group B)
- [[excalibur-hfpef]] — EXCALIBUR-HFpEF (DRKS00039892): app-based exercise coaching vs. standard care; HFpEF LVEF >40%; N=200 target; recruiting since 2026-01-27; no data yet
- [[balanced-hf]] — BalanceD-HF (NCT06307652): balcinrenone/dapagliflozin vs. dapagliflozin; HF with impaired kidney function; N=3,850 (est.); AstraZeneca; recruiting; no data yet
- [[easi-hf]] — EASi-HF Preserved (NCT06424288): vicadrostat + empagliflozin vs. placebo + empagliflozin; HFpEF/HFmrEF LVEF ≥40%; N=6,000 (est.); Boehringer Ingelheim; recruiting; no data yet
- [[redefine-hf]] — REDEFINE-HF (NCT06008197): finerenone vs. placebo post-ADHF hospitalisation; HFpEF/HFmrEF LVEF ≥40%; N=5,200 (est.); recruiting; no data yet
- [[confirmation-hf]] — CONFIRMATION-HF (NCT06024746): finerenone + empagliflozin vs. usual care, open-label, hospitalized HF; **any-EF, not HFpEF-restricted**; N=1,500 (est.); recruiting; no data yet

### Registry-Only Trial Entities, Status Uncertain (see [[trials-pending]] Group C)
- [[mapped]] — MAPPED (NCT06316661): CMR stress-perfusion/ECV vs. controls across two HFpEF phenogroups; N=60 (est.); Istituto Auxologico Italiano, Milan; **registry status Unknown** (last known: Recruiting, 2024-03) — may never publish

### Registry Entities
- [[torch]] — DZHK TORCH registry: 19 German centres; 2,300 (Phase 1) + 4,340 (TORCH-Plus) non-ischemic CMP patients; deep molecular phenotyping
- [[decipher-hfpef]] — DECIPHER-HFpEF: 7 German centres; n=185; validates CMR vs. invasive PV loops in HFpEF; biopsy + biomarkers; NCT03251183
- [[myovasc]] — MyoVasc registry: N=3,289 HF patients + controls; 10-year follow-up; multi-omics; DZHK Rhine-Main; PI Philipp Wild; backbone for [[myomobile]] RCT; NCT04064450
- [[pursuit-hfpef]] — Osaka-area prospective ADHF-HFpEF registry (UMIN000021831); N=1,026; basis for NLR+PLR cardiac-death prediction finding

### Comorbidity Entities
- [[atrial-fibrillation]] — Most common sustained arrhythmia; both cause and consequence of HFpEF; requires adjusted diagnostic thresholds
- [[obesity-hfpef]] — Obesity (BMI ≥30) in HFpEF; 30–40% prevalence; pericardial restraint + adipose inflammation; targeted by semaglutide (STEP-HFpEF) + tirzepatide (SUMMIT HR 0.62)
- [[hypertension-hfpef]] — Arterial hypertension in HFpEF; 60–80% prevalence (most common comorbidity); RAAS blockade consistently neutral; SBP <130 mmHg target; phenotype-guided agents (indapamide, nebivolol, CCB)
- [[attr-cm]] — ATTR Cardiomyopathy (disease entity); TTR amyloid; 13–19% prevalence in HFpEF; tafamidis disease-modifying (AHA 2022 Class I); requires active exclusion in HFpEF workup
- [[patisiran-apollo-b]] — siRNA (TTR gene silencer); first cardiac-outcomes evidence in ATTR-CM via APOLLO-B trial

### Imaging Modalities
- [[echocardiography]] — Primary imaging modality for LVEF and diastolic function assessment in HFpEF
- [[cardiac-mri]] — Gold standard for LVEF; tissue characterisation; second-line in HFpEF workup
- [[technetium-pyrophosphate-scintigraphy]] — Non-invasive gold-standard diagnostic for ATTR-CM exclusion in HFpEF workup

### Diagnostic Tools
- [[cardiopulmonary-exercise-testing]] — Gold standard for invasive HFpEF confirmation; dissects cardiac vs. peripheral exercise intolerance mechanisms
- [[maggic-risk-score]] — Externally validated HF prognostic risk score; used as adjustment covariate in phenomapping analyses
- [[kansas-city-cardiomyopathy-questionnaire]] — Most-cited patient-reported outcome instrument in the wiki; primary/key-secondary endpoint across HFpEF trials
- [[six-minute-walk-test]] — Standard functional-capacity outcome measure; secondary endpoint across pharmacological and exercise trials
- [[minnesota-living-with-heart-failure-questionnaire]] — QoL instrument used in RAAS/PDE5i-era HFpEF trials (I-PRESERVE, RELAX)
- [[short-physical-performance-battery]] — Geriatric functional-assessment battery; REHAB-HF primary endpoint

### Interventions
- [[supervised-exercise-training]] — Most consistently positive HFpEF intervention; peak VO2 +2.8 mL/kg/min; Class I AHA/ACC 2022; hard outcomes unknown

---

## Concepts

### Diagnostic Framework & Classification
- [[hf-phenotype-classification]] — EF-based four-way classification of HF (HFrEF/HFmrEF/HFpEF/HFimpEF); AHA 2022 adds HFimpEF; rationale, caveats
- [[guideline-comparison]] — ESC 2021 vs. AHA 2022 on HFpEF: definition, EF taxonomy, staging, diagnostics, pharmacotherapy; key divergences explained
- [[hfpef-diagnosis]] — Diagnostic criteria, Table 9 markers, HFA-PEFF/H₂FPEF algorithms, invasive confirmation
- [[hfpef-diagnostic-definitions]] — Seven competing definitions enroll 12–90% of same cohort; sensitivity/specificity vs. invasive CPET reference; trial populations non-interchangeable
- [[noncardiac-dyspnea]] — Differential-diagnosis contrast class for exercise-unmasked HFpEF; basis for H₂FPEF score derivation
- [[hfpef-mimics-differential-diagnosis]] — HCM, cardiac sarcoidosis, constrictive pericarditis, Fabry disease, haemochromatosis, high-output HF as active-exclusion phenocopies
- [[hfpef-aba-score]] — 3-variable (BMI/Age/AF) pre-echo screening score; outperforms NT-proBNP alone for risk stratification

### Core Pathophysiology & Mechanisms
- [[diastolic-dysfunction]] — Impaired LV relaxation/stiffness → elevated filling pressures; core HFpEF mechanism; echocardiographic and invasive assessment
- [[coronary-microvascular-dysfunction]] — CMD; Paulus–Tschöpe paradigm: systemic inflammation → coronary microvascular endothelial inflammation → ↓NO/cGMP → titin stiffness + fibrosis; "common soil" hypothesis; NO/cGMP therapy failures paradox
- [[pericardial-restraint]] — Mechanical cardiac constraint from pericardium + paracardiac adipose tissue; limits biventricular filling at exercise; central obesity-HFpEF mechanism; pericardial fat modifiable (SUMMIT CMR: tirzepatide −43 mL)
- [[inflammation-hfpef]] — Systemic inflammation in HFpEF; NLR/PLR trajectories; IL-6, TNF-α pathways; NLR trajectory HR 1.26; DHART2 anti-IL-1β pilot
- [[hfpef-inflammatory-metabolic-paradigm]] — Extension of Paulus 2013 paradigm; HR 1.43 all-cause/HR 2.04 CV mortality/HR 2.83 rehospitalisation (I²=0%); inflammatory endotype (~30%)
- [[myocardial-fibrosis]] — Diffuse interstitial fibrosis; sST2 HR 2.76 (I²=0%); ECV independent from CMD (r=−0.06); hfpef-fibrosis-paradigm
- [[epicardial-adipose-tissue]] — EAT pathophysiology; pericardial restraint + paracrine inflammation; r=0.88 with LV eccentricity
- [[nitric-oxide-pathway]] — eNOS → cGMP-PKG → titin phosphorylation; systemic inflammation → NO deficit
- [[camkii]] — CaMKII oxidation by ROS (SDB/hypoxia) → Ca²⁺ dysregulation → AF substrate
- [[cardiac-output-reserve]] — Peak CO 6.3 vs 7.6 L/min; EDV vs ESV reserve patterns in HFpEF
- [[hemodynamics]] — PCWP 18→32 mmHg rest→exercise; haemodynamic reserve impairment; NP-guided therapy failure
- [[cardiac-remodelling]] — Concentric LV hypertrophy dominant; QRS as remodelling marker; reverse remodelling with ARNi/SGLT2i
- [[left-atrial-remodelling]] — LA dilation and dysfunction; PARAMOUNT LA volume −4.6 vs +0.37 mL; AF substrate
- [[microvascular-dysfunction]] — CMD 70% prevalence (DIAMOND-HFpEF); fQRS ECG surrogate; independent of fibrosis
- [[hfpef-fibrosis-paradigm]] — CMD and fibrosis as parallel independent prognostic axes (r=−0.06)
- [[titin]] — Sarcomeric stiffness mechanism; N2BA→N2B isoform shift + hypophosphorylation; dynamically modifiable target

### Biomarkers
- [[natriuretic-peptides]] — BNP/NT-proBNP; diagnostic thresholds including AF-adjusted values; limitations in obesity; NT-proBNP glycosylation at Thr-71 causes Elecsys assay to underestimate true NP concentration in obese/diabetic HFpEF (Hage 2026 tNT-proBNP)
- [[biomarkers-hfpef]] — Hub page; six categories (natriuretic peptides, inflammatory, fibrosis, leukocyte ratios, iron deficiency, metabolic/renal) plus structural/imaging-derived biomarkers; includes tNT-proBNP glycosylation problem; multi-biomarker panel evidence; open questions on obesity-adjusted thresholds
- [[ecg-biomarkers-hfpef]] — QRS ≥120 ms HR 1.27/1.38 (TOPCAT); fQRS HR 1.90 for HFH; ECG surrogates for CMD and remodelling

### Exercise Physiology & Intolerance
- [[exercise-intolerance]] — Dominant HFpEF symptom; primary mechanism is skeletal muscle myopathy (>50% of VO2 deficit); cardiac, pulmonary, vascular contributions secondary
- [[ventilatory-limitation]] — Ventilatory limitation in obese HFpEF; 62–85% dynamic hyperinflation; NTG doesn't improve exercise
- [[heart-lung-interactions]] — Dynamic hyperinflation → ↑PCWP; ΔEELV vs. ΔPCWP correlation (r²=0.167)
- [[peripheral-mechanisms-hfpef]] — A-VO₂ difference reserve β=0.66; peripheral skeletal muscle primary exercise limitation
- [[chronotropic-incompetence]] — ~30–50% prevalence exercise-limiting mechanism; beta-blocker withdrawal improves VO2; rate-adaptive pacing failed
- [[dynamic-hyperinflation]] — ΔEELV ≥150 mL from rest; 62% at 20W, 85% at peak exercise; raises exercise PCWP
- [[inspiratory-muscle-training]] — Respiratory-muscle-specific training; distinct from aerobic/resistance modalities; Palau 2014 VO2peak +2.9 mL/kg/min

### Phenotypes & Comorbidity-Specific HFpEF
- [[hfpef-phenotype-profiling]] — Two-layer treatment model: SGLT2i universal + phenotype-guided add-on; 18 comorbidity phenotypes with prevalences; Figure 2 treatment wheel; CMD, iron deficiency, cancer HFpEF; LVEF 50–55% subgroup
- [[pulmonary-hypertension-hfpef]] — PH in HFpEF; present in ~50–80%; IpcPH (passive) vs. CpcPH (reactive with vasculopathy); PAC outperforms PVR for prognosis; no proven pharmacological therapy for CpcPH in HFpEF
- [[hfpef-phenotypes]] — HFpEF phenotype framework; Shah 2014 phenomapping (4 clusters); Anker 2023 biomarker phenotyping; precision medicine rationale; phenotype-directed therapy
- [[obese-metabolic-hfpef]] — Obese-metabolic HFpEF phenotype (~30%); EAT, lipotoxicity, OSA; semaglutide KCCQ +7.8 pts/6MWD +20.3 m/weight −10.7% (STEP-HFpEF); SGLT2i universal
- [[hypertensive-fibrotic-hfpef]] — Hypertensive-fibrotic HFpEF phenotype (~50%); concentric LV hypertrophy; sST2 HR 2.76; BP control (SBP<130), SGLT2i, MRA; best prognosis among HFpEF subtypes
- [[atrial-fibrillation-hfpef]] — AF-dominant HFpEF phenotype (10–50%); loss of atrial kick; rhythm control OR 0.735/HR 0.74 vs. rate control; CABA-HFpEF ongoing
- [[iron-deficiency]] — Iron deficiency in HFpEF; 59% prevalence; FAIR-HFpEF 6MWT +49m; IV ferric carboxymaltose
- [[sleep-disordered-breathing]] — SDB in HFpEF; 50–80% prevalence; CaMKII pathway; SERVE-HF contraindication (HFrEF context); OSA treatment
- [[rhythm-control]] — Rhythm vs. rate control in AF+HFpEF; OR 0.735 (I²=0%) meta-analysis; EAST-AFNET4 HR 0.74
- [[sex-differences-hfpef]] — Female HFpEF predominance via 7 mechanisms (structure, vascular aging, menopause, comorbidity, obstetric history, immune biology, exercise hemodynamics); sex-differential arterial stiffness (Lau 2022); men die of HFpEF (RHF/SCD) vs. women die with HFpEF (Duca 2018)
- [[hfpef-disparities]] — Racial/ethnic disparities; Black women 7.4/1,000 PY; low BNP trap; ATTR V122I 3.43%
- [[pulmonary-arterial-pressure]] — IpcPH vs CpcPH; PCWP 32 mmHg at 20W; PA pressure monitoring
- [[magnesium-hfpef]] — Serum Mg quintile treatment-effect modifier in EMPEROR-Preserved; lower Mg associated with worse outcomes
- [[cancer-therapy-cardiotoxicity-hfpef]] — Anthracycline/taxane/trastuzumab/radiotherapy-induced HFpEF; iatrogenic phenotype with quantified per-agent incidence

### Treatment & Care Delivery
- [[hfpef-treatment-gap]] — Central problem: no proven disease-modifying therapy across full HFpEF population; failed trials catalogue; SET fills functional gap
- [[treatment-hfpef]] — Redirect stub → [[hfpef-treatment]]; resolves [[treatment-hfpef]] cross-references
- [[hfpef-treatment]] — Treatment evidence synthesis; SGLT2i Class 2a/1; statins HR 0.74 non-ischaemic; GLP-1 RA; phenotype-directed therapy
- [[hemodynamic-monitoring]] — CardioMEMS; CHAMPION 28% HFH reduction; GUIDE-HF pre-COVID HR 0.81
- [[acc-aha-hf-guidelines]] — 2022 AHA/ACC guidelines; PM-2 BP control; QM-1 SGLT2i for HFpEF
- [[acute-hf]] — ADHF in HFpEF; NLR trajectory HR 1.26; haemodynamic management
- [[worsening-heart-failure]] — WHF as trial construct: 3-tier hierarchical definition (hospitalisation/urgent outpatient/nonurgent outpatient); broadening increases event rate/power but not mortality specificity; underlies SOLOIST-WHF/PARAGLIDE-HF population definitions and FINEARTS-HF/DELIVER endpoint constructs

### AI / Machine Learning
- [[ml-ai-hfpef]] — AI/ML in HFpEF: 4 domains (diagnosis, phenotyping, risk prediction, management); spironolactone responder ML; ECG-AI as scalable screening

### Vascular
- [[arterial-stiffness]] — Exercise-divergent arterial stiffness; Ea/TACI uncoupling; inorganic nitrite reversal
