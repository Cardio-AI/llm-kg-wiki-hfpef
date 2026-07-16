Purpose: create concise synthesis of ONE topic/source/study/guideline. "ONE topic" bounds the summary's *subject*, not its source count — a concept summary may synthesize several canonical pages/citekeys as long as they all serve that one topic.
Outputs: `wiki/summaries/`

---
# Rules
1. Use canonical pages only (see CLAUDE.md Governance Terms)
2. Resolve aliases first
3. Prefer concise synthesis
4. Preserve uncertainty
5. Include contradictions
6. Link densely

---
# Structure
- TL;DR — one or two sentences, plain language, the single most important takeaway
- Key findings
- Mechanisms
- Clinical implications
- Evidence quality
- Open questions
- Related pages

---
# Anti-Patterns
Never:
- rewrite entire source
- duplicate long prose
- create detached summaries — a summary is detached when it doesn't link back to the canonical page(s) it was synthesized from; every summary must cite/link its source canonical page(s)

---
# Output Naming

`wiki/summaries/<topic>.md`, kebab-case, matching the topic's canonical page name where one exists.
