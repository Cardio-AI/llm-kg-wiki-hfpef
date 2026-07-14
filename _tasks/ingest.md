1. Read the full source document
2. Analyze: key entities, concepts, core arguments, connections to existing wiki, contradictions
3. **Discuss analysis with user before writing anything** — cover: key entities found, concepts updated, contradictions identified, gaps remaining
4. Zotero: read `_config/zotero.md` for credentials. Search Zotero by DOI or title. If not found, add it. Retrieve or generate citekey (`AuthorYearKeyword`). Citekey + DOI only in frontmatter/body — never the local `raw/` path (gitignored, local-only).
5. Write pages:
   - `wiki/sources/<citekey>.md` — use `_templates/study.md` for clinical studies, `_templates/source.md` for all others
   - Create/update concept pages in `wiki/concepts/`
   - Create/update entity pages in `wiki/entities/`
6. Link densely with `[[wiki-links]]`
7. When updating an existing page, migrate it to the current template structure if it still uses the old `## Content` format
8. `## History` on concept pages requires ≥2 sources to be meaningful; if only one source exists, write what's known and mark `[expand as sources added]`
9. Update: `wiki/index.md`, `wiki/log.md`, `wiki/overview.md`, `wiki/contradictions.md`, `wiki/timeline.md`

One source may touch 10–15 wiki pages. That is normal.