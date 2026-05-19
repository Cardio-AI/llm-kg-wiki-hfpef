Purpose: answer questions using canonical wiki knowledge graph.
Outputs: `wiki/queries/`

---

# Rules
1. Resolve aliases first
2. Check `wiki/queries/` for existing answers before generating a new one
3. Revalidate against newer wiki knowledge before reusing old answers
4. Preserve provenance — cite sources inline (`[[page]]`, APA format from `wiki/citations.md`)
5. Link densely

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
## Related Pages
```

Save to `wiki/queries/`. Maintain `wiki/queries/index.md`.
