# lens — a closer look at complex things

One topic per page: interactive maps, charts and numbers, with sources and an
arithmetic check.

Live at [lens.gramoflava.xyz](https://lens.gramoflava.xyz). Static HTML on
GitHub Pages, no build step, no backend.

## Add a page

1. `name.html` in repo root: topic + two-digit year (`oilmegashock26.html`).
2. Copy an existing story's head: no-flash snippet, favicon lines, font link, `gramofdesign/gramof.css`, `editorial.css`, own `<style>`; deferred `tools.js` + `theme.js`; `<html lang="en" data-accent="lens">`. Index card reads:
   ```html
   <title>Page name · lens</title>
   <meta name="description" content="One or two sentences.">
   <meta name="date" content="2026-10-02">
   <meta name="keywords" content="energy, economics">
   ```
3. Name the source; show the arithmetic.
4. `../gramofdesign/check.py .` → all clear. Push; the index lists root `*.html` via the GitHub contents API (newest `date` first, 10 min browser cache).

## Look

gramof design (slate `lens` accent) → `editorial.css` (display scale, story motion, shared furniture) → page `<style>` (story-unique only, story colours as tokens). Rules in `AGENTS.md`. `lens.css` = index layout only.

## Licence

[Unlicense](LICENSE). Third-party content (videos, data) belongs to its
authors and is linked, not copied.
