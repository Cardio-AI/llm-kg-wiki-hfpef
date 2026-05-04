# Zotero Integration

Claude uses the Zotero Web API to check and add references on every ingest.

## Setup (one-time)
1. Go to https://www.zotero.org/settings/keys → **Create new private key**
   - Enable: Read/Write access to your personal library
2. Your **User ID** is shown on the same page (numeric)
3. Fill in the values below

## Configuration
```
ZOTERO_USER_ID=       # numeric ID from zotero.org/settings/keys
ZOTERO_API_KEY=       # private key generated above
```

## How Claude uses this on ingest
1. **Look up** paper by DOI first, then title:
   ```
   GET https://api.zotero.org/users/{ZOTERO_USER_ID}/items?q={doi_or_title}&key={ZOTERO_API_KEY}
   ```
2. **If found:** read citekey from the `extra` field (Better BibTeX format: `Citation Key: AuthorYearKeyword`)
3. **If not found:** add item via:
   ```
   POST https://api.zotero.org/users/{ZOTERO_USER_ID}/items?key={ZOTERO_API_KEY}
   ```
   Then generate citekey as `AuthorYearKeyword` and write it into the `extra` field.
4. Use that citekey in all wiki pages for this source.

## Citekey Format
`AuthorYearKeyword` — first author's last name + year + 1–2 word topic.  
Examples: `Shah2022HFpEFPheno` · `Borlaug2014Exercise` · `Paulus2013Diagnostic`

## Notes
- Requires Better BibTeX plugin in Zotero for automatic citekey generation (recommended)
- Without Better BibTeX, Claude generates and manually stores the citekey in the `extra` field
- If API credentials are missing or the call fails, Claude generates the citekey locally and flags it with `[zotero-unverified]` in the source page frontmatter
