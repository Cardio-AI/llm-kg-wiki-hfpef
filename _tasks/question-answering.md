Purpose: answer questions using canonical wiki knowledge graph.
Outputs: `wiki/queries/`

---

# Rules
1. Resolve aliases first
2. Check `wiki/queries/` for existing answers before generating a new one
3. Revalidate against newer wiki knowledge before reusing old answers
4. Preserve provenance — cite sources inline (`[[citekey]]`); include full APA references at end of answer
5. Link densely
6. Never fabricate. Apply CLAUDE.md's Citation & Evidence sourcing taxonomy (the OK / borderline / not-OK tiers) to every claim in the answer. If the wiki doesn't cover part of a question, say so explicitly (`[not covered in wiki — needs ingest]`) rather than answering from memory.
7. If the question is ambiguous — unclear scope, could reasonably mean two different things, or is missing a qualifier needed to answer precisely — ask a clarifying question before drafting. Do not guess and bury the ambiguity inside hedging language in the answer.

---

# Step 0 — Scope & Intent Triage

Run this before drafting anything.

**Check for ambiguity first (Rule 7).** If the question can't be scoped without guessing — genuinely unclear which concept/entity it targets, or missing a qualifier that would change the answer — stop here and ask the user rather than proceeding to the steps below.

**Name the exact scope.** Identify the canonical wiki page(s) that are authoritative for the question. Do not silently merge adjacent-but-distinct concepts — e.g. "diastolic dysfunction" (mechanism) is not "HFpEF" (clinical diagnostic entity); a parameter's role inside one algorithm does not make it definitional for an adjacent concept (GLS appearing as a minor criterion in HFA-PEFF's HFpEF-probability score doesn't make it a "diastolic dysfunction parameter" — it's a systolic-strain marker used there for a different purpose). If the question names the narrower concept, answer the narrower concept; bring in the broader one only as a clearly labeled cross-reference.

**Extract qualifier words that bound the answer.** "Demonstrated *benefit*" excludes neutral/negative trials from the primary list. "Most *commonly used*" means guideline-endorsed/routine, not "appears somewhere in a paper." This filter governs the default answer (TL;DR / Short / Standard). **Extended Discussion may relax it**: neutral/negative trials can be brought in if benefit was asked about, and "commonly used" can widen to methods substantively discussed in a source (not just named in a related-work list) — as long as it's clearly framed as broader context, not blended into the direct answer.

**Classify question type:** Fact-lookup / Yes-or-No-with-justification / Comparative / Case-based clinical-reasoning / Mechanistic-explanatory. Case-based questions must open with **one** clear recommended pathway before any enumeration of alternatives — don't make the reader assemble the answer from a flat list of equally-weighted options.

**Estimate evidence load/difficulty** — this sets where in the Standard-mode word range (see below) the answer should land.

---

# Output Format

**Style:** Concise, precise, scientific. No padding, no hedging beyond warranted uncertainty.
**Structure:** Prose for short answers; headers, bullet points, and tables where the content has multiple dimensions or comparisons.
**Sentence construction:** no em-dash-appended clauses (" — like this") tacking extra information onto a sentence. Use a new sentence, a comma, or a semicolon instead. The Bottom Line especially must be one grammatically complete, unambiguous sentence; reread it before finalizing, since if it needs an em-dash or a run-on to fit, it's really two sentences.
**Citations:** Inline `[[citekey]]` for every factual claim, **including every bullet/list item, not just paragraph prose**. Citations do not count toward a tier's word budget; never drop or water down a citation to save words, state the claim as fully and correctly as needed and cite it properly. If a claim can't be sourced, mark `[needs source]` or drop the claim, not the citation.
**No internal-bookkeeping leakage:** don't surface wiki-internal cross-reference plumbing in the answer (contradiction entry numbers, "logged as," log-file pointers). Pointers to a genuinely useful canonical/detail page ("Full detail, tables, and all citations: [[page]]") are encouraged and unaffected by this rule; the test is whether the pointer helps the reader find more information (keep) or just exposes internal wiki bookkeeping (cut).
**Reference Overview (all four tiers, including TL;DR):** every answer ends with a compact block listing each citekey actually used, as a full APA reference pulled from `wiki/citations.md` → Full Formatted References (same lookup/conversion already used for citation-lookup requests — do not reformat from memory). This block does not count toward the tier's word budget.

## Answer Modes

Produce four possible tiers. **Standard is the default and is always produced** unless the user asks for a different tier.

| Mode | Length | Contents | When |
|---|---|---|---|
| TL;DR | 20–80 words | Direct answer only — no bottom-line line (it *is* the bottom line). If the question's scope exceeds what fits in this tier, append: `WARNING! Scope not fully covered, see Standard/Extensive Answer.` Still ends with the Reference Overview block (not counted toward the word budget). | On request |
| Short | ~80–150 words | Direct answer + one-line **Bottom line:** + evidence tag | On request |
| **Standard** | 50–400 words, scaled to evidence load/difficulty — not a fixed target | Direct answer, literal to question scope + **Bottom line:** + evidence tag | **Default, always produced** |
| Extended | Unbounded | `## Extended Discussion` — mechanism, secondary trials, nuance, edge cases; relaxed scope filter (see Step 0). In-scope framing preserved; material outside the question's literal scope gets a `[[link]]` pointer instead of being folded in | Appended after Standard, offered not forced |

A simple fact question (e.g. "what LVEF defines HFpEF") should sit near the bottom of the Standard range; a multi-mechanism or multi-trial question can run toward 400 — but every sentence must trace back to something the question actually asked.

## Evidence Tag (Short / Standard / Extended)

For every load-bearing claim:
1. **List** the evidence — source/citekey.
2. **Cite correctly** — reopen the source and confirm it actually supports *this specific claim* before attaching the citekey. A citekey attached to a claim the source doesn't directly address is worse than no citation.
3. **Critically grade directness** — was this the paper's primary result, a secondary/subgroup finding, or only a tertiary/incidental 1–2 sentence mention? A topic being *mentioned* in a paper is not sufficient to count as supporting evidence at full weight — a tertiary/incidental mention does not carry primary-finding weight and must be flagged as such.

## Evidence Quality Block

End every Short/Standard/Extended answer with:

```
## Evidence Quality
**Rating: X / 5**
- Sources: [number and identity]
- Evidence type per source: [primary result / secondary or subgroup result / tertiary-incidental mention / mechanistic-only / expert opinion / guideline]
- Publication year(s): [range]
- Directness: does the evidence directly answer THIS question, or is it adjacent/indirect?
- Limitations: [gaps, heterogeneity, outdated data, single-cohort/small-N caveats]
```

Rating scale — each score requires the evidence to be *primary/direct* at that tier, not merely recent and plentiful:

| Score | Meaning |
|---|---|
| 5 | Multiple concordant RCTs or high-certainty meta-analysis; recent (≤5 years); each is primary/direct evidence for the literal question |
| 4 | ≥1 RCT or high-quality cohort; recent; primary or secondary evidence; minor gaps |
| 3 | Single RCT or moderate cohort evidence; or the evidence is secondary/subgroup rather than the source's primary endpoint |
| 2 | Registry data, subgroup analyses, or expert consensus; no direct RCT; or evidence is a tertiary/incidental mention in the cited source(s) |
| 1 | Case series, mechanistic-only reasoning, or a single small/low-quality study (flag N) |
| 0 | No wiki sources; cannot answer from canonical knowledge base |

**Rating reflects the weakest load-bearing claim, not an average of all cited sources.** A finding resting on a single small/mechanistic study (e.g. N<100, no guideline endorsement) must be presented in prose with explicit "preliminary, N=x, not guideline-endorsed" framing — never in a table styled like a guideline-recommendation table. Presenting weak evidence with guideline-table authority is a safety issue, not a style choice.

## List / Strategy Hygiene

- Rank items by evidence strength and centrality to the literal question — do not flatly enumerate unequal items as a numbered list of peers.
- Nest minor variants/adjuncts under their parent item instead of listing them as separate top-level items.
- Exclude items outside the literal scope of the question (e.g. post-diagnosis workup when the question is about diagnosing an undiagnosed patient) — reference via `[[link]]` instead of expanding inline.

---

# Workflow
1. Run Step 0 (Scope & Intent Triage)
2. Read `wiki/index.md` to locate relevant pages
3. Read those pages; synthesize answer with citations, in the correct answer mode
4. For "how did thinking on X evolve?" — consult `wiki/timeline.md` and `## History` sections; trace evidence chronologically
5. **Verification pass (mandatory before finalizing):** for every inline citekey attached to a specific claim, reopen the source and confirm it is directly supported there. Fix or remove any claim that doesn't hold up.
6. If evidence is insufficient: say so clearly (`[not covered in wiki — needs ingest]`); offer to save an open-question note to `inbox/`
7. If the answer is valuable: offer to save it as a query page (see Query Page Structure below)

---

# Query Page Structure

```
---
question:
answer_summary:
answer_mode:        # TL;DR | Short | Standard | Extended
scope_note:         # one-line statement of what's in / out of scope
sources_used: []
timestamp:
verification_status:  # verified | unverified | needs-recheck — set "verified" only after Workflow step 5's verification pass has checked every citekey
derived_from: []
---

## Question
## Answer
## Evidence
## Contradictions
## References
## Evidence Quality
```

Save to `wiki/queries/`. Maintain `wiki/queries/index.md`.
