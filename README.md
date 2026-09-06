# PICKS HANABI — Phase 2 (local features)

## Files
- `index.html` — the app (single file)
- `words.json` — word list exported from PICKS_HANABI_core_words.xlsx (176 words)
- `assets/` — background, logo, fireworks, NEW RECORD

Upload the whole folder to GitHub Pages (drag & drop). Opening index.html directly from a local file
falls back to a 20-word built-in list, because browsers block reading words.json from file://.

## Updating words (until GAS is connected)
Edit the spreadsheet, then re-export `words.json` in the same shape:
{ "words": [ { "id": "W001", "ja": "…", "en": "…", "category": "verb", "tag": "…" }, … ] }
Rows with empty ja/en or enabled=FALSE are skipped. In Phase 3 this file is replaced by the GAS endpoint.

## Tuning fireworks
Everything is in `FIREWORK_CONFIG` at the top of the script: category → colour, combo milestones,
sizes and praise text. 
