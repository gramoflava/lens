# Agent rules

## Design
- Built on gramof design: `../gramofdesign` (github.com/gramoflava/gramofdesign). Read its README before any visual/UX change. Vendored `gramofdesign/` = deploy copy, never edit.
- Order: gramof has it → use it. Reusable → add to gramofdesign, `../gramofdesign/check.py --sync`. Site-only → build here from tokens; new values = `--ed-*` tokens.
- No raw sizes/weights/durations/colours in rules. Don't restyle shared components; scope to site classes.
- Before commit: `../gramofdesign/check.py .` → all clear.

## Site: editorial magazine (owned flavour)
- One story per page; long pages OK; animations serve comprehension.
- Order: gramof → `editorial.css` → page `<style>`.
- `editorial.css` owns: display scale `--ed-text-*`, story motion `--ed-dur-*`/`--ed-ease-*` (longer than 120–200 ms by design), shared furniture. Used by 2+ stories → move there; by all sites → gramofdesign.
- Page `<style>`: story-unique only; story colours as `:root` tokens built on gramof (`--crude: var(--chart-2)`).
- No parallel variable sets (`--ink`, `--body`…), no emoji icons. New page: see README "Add a page".
