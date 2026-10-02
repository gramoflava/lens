# lens — a closer look at complex things

One topic per page: interactive maps, charts and numbers, with sources and an
arithmetic check.

Live at [lens.gramoflava.xyz](https://lens.gramoflava.xyz). Static HTML on
GitHub Pages, no build step, no backend.

## Add a page

1. Put a self-contained `name.html` in the repo root. Short lowercase name,
   topic plus two-digit year, e.g. `oilmegashock26.html`.
2. Give it a full document with inline CSS and JS, a link back to `./`, and
   these head tags — the index reads its card from them:

   ```html
   <meta charset="utf-8">
   <title>Page name · lens</title>
   <meta name="description" content="One or two sentences.">
   <meta name="date" content="2026-10-02">
   <meta name="keywords" content="energy, economics">
   ```

3. Name the source on the page.
4. Commit and push. No index edit is needed.

`index.html` lists every `*.html` in the repo root (except itself) through the
GitHub contents API, then reads each page's head from the same site. Newest
`date` first. The list is cached in the browser for 10 minutes; the API allows
60 unauthenticated requests per hour per visitor IP.

## Look

The index and every page use the shared [gramof design](gramofdesign/README.md)
with the silver `lens` accent (`data-accent="lens"` on `<html>`). A new page gets
the family look by adding to its `<head>`:

```html
<link rel="stylesheet" href="gramofdesign/gramof.css">
<script defer src="gramofdesign/tools.js"></script>
<script defer src="gramofdesign/theme.js"></script>
```

plus the no-flash theme snippet and the font link from the gramof README, and
one empty element for the top-right tools (theme · Ko-fi · whois):
`<div class="site-tools site-tools--glass site-tools--float" data-site-tools></div>`. Colours come from tokens only
(`--text`, `--line`, `--chart-*`), so charts and maps follow the switch. Icons
are Tabler from `gramofdesign/icons/`, never emoji. `lens.css` is the index
layout only.

## Licence

[Unlicense](LICENSE). Third-party content (videos, data) belongs to its
authors and is linked, not copied.
