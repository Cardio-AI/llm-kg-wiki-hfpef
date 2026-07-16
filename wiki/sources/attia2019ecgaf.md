---
title: 'An artificial intelligence-enabled ECG algorithm for the identification of
  patients with atrial fibrillation during sinus rhythm: a retrospective analysis
  of outcome prediction'
citekey: attia2019ecgaf
year: 2019
authors: Attia ZI, Noseworthy PA, Lopez-Jimenez F, Asirvatham SJ, Deshmukh AJ, Gersh
  BJ, Carter RE, Yao X, Rabinstein AA, Erickson BJ, Kapa S, Friedman PA
journal: The Lancet
tags:
- ml-ai
- atrial-fibrillation
- diagnosis
created: 2026-05-15
last_updated: 2026-05-15
sources:
- citekey: attia2019ecgaf
  doi: 10.1016/S0140-6736(19)31721-0
page-type: source-summary-page
---
# An artificial intelligence-enabled ECG algorithm for the identification of patients with atrial fibrillation during sinus rhythm

> **NOT an HFpEF study.** A convolutional neural network trained on sinus-rhythm ECGs detects patients with paroxysmal atrial fibrillation (AUC 0.87 per ECG, 0.90 per patient), revealing the structural atrial "signature" of AF-prone patients — methodology foundational for ECG-AI applied to HFpEF.

**Full citation:**
Attia ZI, Noseworthy PA, Lopez-Jimenez F, Asirvatham SJ, Deshmukh AJ, Gersh BJ, Carter RE, Yao X, Rabinstein AA, Erickson BJ, Kapa S, Friedman PA. An artificial intelligence-enabled ECG algorithm for the identification of patients with atrial fibrillation during sinus rhythm: a retrospective analysis of outcome prediction. *Lancet.* 2019;394(10201):861–867. doi:[10.1016/S0140-6736(19)31721-0](https://doi.org/10.1016/S0140-6736(19)31721-0)

---

## Core Arguments

**Study type:** Retrospective development and validation; NOT an HFpEF study. Population: general patients at Mayo Clinic with ≥1 sinus-rhythm 12-lead ECG recorded 1993–2017.

**Training data:** 649,931 ECGs from 180,922 patients; validation on separate held-out set.

**Task:** Identify patients with known paroxysmal AF from their sinus-rhythm ECGs — detecting atrial structural remodelling (fibrosis, hypertrophy) that persists between AF episodes, not the arrhythmia itself.

**Key performance metrics:**
- AUC **0.87** per single sinus-rhythm ECG (sensitivity 79.0%, specificity 79.5%)
- AUC **0.90** when all available sinus-rhythm ECGs from a patient are aggregated
- 55.7% of AF-positive patients had a sinus-rhythm ECG within 1 week of their first recorded AF ECG — model detects pre-AF structural signature in near-term AF
- Model detects pre-AF changes on ECGs recorded up to 31 days before first AF event

**Companion methodology:** A separate Attia et al. 2019 *Nature Medicine* paper from the same group applied the same CNN framework to asymptomatic LV systolic dysfunction (EF <35%), achieving AUC 0.93 — the two papers together establish the ECG-AI methodology adopted by subsequent HFpEF-directed studies.

## Relevance to HFpEF Wiki

This paper is **not an HFpEF study** but belongs in this wiki for three reasons:

1. **AF is a major HFpEF comorbidity** (25–50% prevalence) and a diagnostic confounder; paroxysmal AF may be unrecognised in HFpEF patients, creating both diagnostic and prognostic uncertainty.
2. **ECG-AI methodology:** The convolutional neural network architecture and training approach established here are the direct methodological precursor for subsequent ECG-AI studies applied to HFpEF diagnosis — including Gao 2025 (*ESC Heart Fail*) which applies this paradigm to detect HFpEF from sinus-rhythm ECGs ([[gao2025ecgdl]]).
3. **Diagnostic implications:** An AI-ECG detecting AF probability could assist HFpEF workup by flagging patients likely to have unrecognised paroxysmal AF — a potential confound in natriuretic peptide interpretation and treatment decisions.

## Connections
- Provides methodology for: [[ml-ai-hfpef]] — CNN/ECG-AI framework adopted by subsequent HFpEF diagnostic AI papers
- Adjacent: [[atrial-fibrillation]] — AF detection in sinus rhythm; relevant to AF burden in HFpEF
- Foundational for: [[gao2025ecgdl]] — ECG deep learning applied directly to HFpEF detection
- Adjacent: [[hfpef-diagnosis]] — unrecognised paroxysmal AF as diagnostic confound

## Related Pages
- Concepts: [[ml-ai-hfpef]], [[hfpef-diagnosis]]
- Entities: [[atrial-fibrillation]], [[echocardiography]]
- Sources: [[gao2025ecgdl]], [[pandey2021deepnnecho]]

## Contradictions
None within this wiki.
