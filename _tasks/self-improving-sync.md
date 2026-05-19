Purpose: propagate canonical knowledge updates to derived artifacts.

---
# Rules
When canonical pages change:
1. identify dependent pages
2. identify stale summaries/comparisons/queries/html
3. rewrite derived artifacts
4. update timestamps
5. log changes

---
# Dependency Sources
Use:
- wiki-links
- derived_from metadata

---
# Derived Artifacts
Possible stale artifacts:
- summaries
- comparisons
- queries
- html

---
# Canonical Priority
Canonical wiki pages override derived artifacts.
Never propagate changes upstream from summaries/questions/html.