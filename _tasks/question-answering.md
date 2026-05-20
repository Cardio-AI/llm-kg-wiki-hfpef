Purpose: answer questions using canonical wiki knowledge graph.
Outputs: `wiki/queries/`

---

# Rules
1. Resolve aliases first
2. Check `wiki/queries/` for existing answers before generating a new one
3. Revalidate against newer wiki knowledge before reusing old answers
4. Preserve provenance — cite sources inline (`[[citekey]]`); include full APA references at end of answer
5. Link densely

---

# Output Format

**Style:** Concise, precise, scientific. No padding, no hedging beyond warranted uncertainty.  
**Structure:** Prose for short answers; headers, bullet points, and tables where the content has multiple dimensions or comparisons.  
**Citations:** Inline `[[citekey]]` for every factual claim. Full APA references listed under `## References` at the end, drawn from `wiki/citations.md`.  
**Uncertainty rating:** End every answer with an `## Evidence Quality` block:

```
## Evidence Quality
**Rating: X / 5**
- Sources: [number and identity]
- Evidence type: [RCT / meta-analysis / guideline / registry / expert opinion]
- Publication year(s): [range]
- Limitations: [any gaps, heterogeneity, outdated data, indirect evidence]
```

Rating scale:
| Score | Meaning |
|---|---|
| 5 | Multiple concordant RCTs or high-certainty meta-analysis; recent (≤5 years); directly answers the question |
| 4 | ≥1 RCT or high-quality cohort; recent; minor gaps or indirect evidence |
| 3 | Single RCT or moderate cohort evidence; some limitations (age, population, surrogate endpoints) |
| 2 | Registry data, subgroup analyses, or expert consensus; no direct RCT |
| 1 | Case series, mechanistic reasoning, or single low-quality study |
| 0 | No wiki sources; cannot answer from canonical knowledge base |

---

# Workflow
1. Read `wiki/index.md` to locate relevant pages
2. Read those pages; synthesize answer with citations
3. For "how did thinking on X evolve?" — consult `wiki/timeline.md` and `## History` sections; trace evidence chronologically
4. If evidence is insufficient: say so clearly; offer to save an open-question note to `inbox/`
5. If the answer is valuable: offer to save it as a query page (see Query Page Structure below)

---

# Query Page Structure

```
---
question:
answer_summary:
sources_used: []
timestamp:
verification_status:
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
