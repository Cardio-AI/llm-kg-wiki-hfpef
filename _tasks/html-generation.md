Purpose: compile `wiki/` markdown into a browsable static HTML site and graph JSON artifacts.

Outputs: `html/` (site) · `graph/` (JSON artifacts) · build report appended to `wiki/log.md`

---

# Rules
1. HTML and `graph/` are derived — never modify `wiki/` during this task
2. `[[wikilinks]]` → relative `<a href>` links; broken link targets → `<span class="broken-link">` and logged in build report
3. Frontmatter fields → `<meta>` tags in each page `<head>`
4. Update `graph/derivations.json` with source file SHA-256 hashes and build timestamp
5. Re-running `build.py` is always safe — idempotent overwrite

---

# Workflow
1. **Write `build.py`** in the project root (Python stdlib only — no pip installs required):
   - Enumerate all `wiki/**/*.md` pages
   - Parse YAML frontmatter (between `---` delimiters)
   - Convert markdown body to HTML (`markdown` module preferred; fallback to `mistune`; last resort: minimal regex for headings/bold/code/links)
   - Resolve `[[PageName]]` → relative URL (kebab-case path to `index.html`); log unresolved links
   - Wrap each page in an HTML shell: sidebar nav (generated from `wiki/index.md`), page content, footer with `last_updated`
   - Write to `html/<same relative subpath>/index.html`

2. **Build `graph/`** JSON artifacts:
   - `entities.json` — `[{file, title, entity_type, tags, summary}]` for all entity pages
   - `aliases.json` — all `## Aliases` table rows extracted from entity and concept pages
   - `relations.json` — all `[[wikilink]]` edges as `[{source, target}]`
   - `derivations.json` — `{built_at, source_hashes: {filepath: sha256}}`

3. **Build `html/search.json`** — `[{title, url, summary, tags}]` for all pages (enables client-side search)

4. **Run `build.py`** and fix any errors until the build completes cleanly

5. **Append build report to `wiki/log.md`**: pages compiled, broken wikilinks, orphan pages, build timestamp

---

# Styling
Single CSS file at `html/style.css`. Requirements: clean sans-serif font, max-width ~800px, sidebar navigation, `<pre>` code blocks, no external CDN dependencies. Prefer readability over decoration.
