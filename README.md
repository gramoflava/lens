# lens — a closer look at complex things

One topic per page: interactive maps, charts and numbers, with sources and an
arithmetic check.

Live at [lens.gramoflava.xyz](https://lens.gramoflava.xyz). Static HTML on
GitHub Pages, no build step, no backend.

## Pages

| Page | Topic | Source |
|---|---|---|
| [oilmegashock26.html](https://lens.gramoflava.xyz/oilmegashock26.html) | Oil Megashock 2026: crude, shipping, diesel | [video](https://www.youtube.com/watch?v=OETnuwwsv9U) |

## Add a page

1. Put a self-contained `name.html` in the repo root. Short lowercase name,
   topic plus two-digit year, e.g. `oilmegashock26.html`.
2. Give it a full document (`<!doctype html>`, `<meta charset="utf-8">`,
   viewport, `<title>`), inline CSS and JS, and a link back to `./`.
3. Name the source on the page.
4. Add an entry at the top of the list in `index.html` and a row in the table
   above.

Each analysis page keeps its own visual identity. The index uses the shared
[gramof design](gramofdesign/README.md) with the `lens` accent defined in
`lens.css`.

## Licence

[Unlicense](LICENSE). Third-party content (videos, data) belongs to its
authors and is linked, not copied.
