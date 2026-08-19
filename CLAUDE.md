# ReWild

A single-file HTML app. No framework, no build step, no package manager, no
backend — open `index.html` in a browser and it runs.

- `index.html` — the app (~1,050 lines of readable source, ~66 KB)
- `PRODUCT.md` — product truth
- `DESIGN.md` — the visual system, derived from the shipped code

Two superseded builds sit in the folder, gitignored and unpublished:
`ReWild Build 6-29.html` and `ReWild Build 6-29 with Supabase api.html`. Both
embed a live Supabase project URL and anon key, which is why they stay out of
the repository. Do not copy code from them without stripping those first.

## Architecture

One file, three parts: a `<style>` block, a direction-contract comment as the
first child of `<body>`, and one `<script>`.

The script is plain functions that build HTML strings, plus a single `render()`
that swaps the result into `#app`. There is no component system and no virtual
DOM. State is one object `S`, persisted to `localStorage` under
`rewild_field_list_v1`, mutated only through `set()`.

Data lives in the `DATA` object at the top of the script: 17 plants, 17 rebates,
7 wildlife groups, 12 months of care tips across four climate bands, and 16
marketplace entries. It was extracted programmatically from the previous build —
if it needs regenerating, do that rather than retyping records.

Events use one delegated `click` listener keyed on `data-act`. Adding an
interaction means adding a `data-act` branch, not wiring a new listener.

## Design tokens — extend these, never fork them

The world is a Rite-in-the-Rain field notebook. Every value lives on `:root`.

- **Ground:** `--stock` (waterproof grid stock, cool — never cream) `--sheet` `--shade`
- **Ink:** `--graphite` `--graphite-2` (both AA on stock and sheet)
- **Rules:** `--rule` `--rule-firm`
- **Signal:** `--hivis` / `--hivis-deep` (logged, active, tallied) · `--survey`
  (fills and large figures only) · `--survey-ink` (the same flag darkened for
  small text — `--survey` fails AA below large sizes) · `--stamp` (locality ink)
- **Type:** `--field` (Archivo) / `--code` (Azeret Mono)
- **Motion:** `--ease` · **Grid:** `--grid` (22px, the notebook's ruling pitch)

The printed grid on `body` is the signature of the whole world. Do not replace it
with a flat fill.

## Standing rules

- **Any motion:** hold it to the `emil-design-eng` / `animate` bar whether or not
  those skills were invoked. `ease-out` on entrances, under 300ms for UI,
  `transform`/`opacity` only, never `scale(0)`, and no animation on anything hit
  100+ times a day. There is exactly one authored motion moment — the plant list
  FLIP re-rank in `reRank()`. Do not add a second without removing it.
- **New surface or redesign:** `impeccable`. The world is committed; a new
  section inherits it rather than starting an identity exercise.
- **Multiple directions to choose between:** `prototype`, which must be named —
  it never triggers on its own.
- **Truthfulness:** rebate figures are real but unverified. Every figure must
  carry that on its own row. Never imply an approved or guaranteed payout, and
  never invent users, testimonials, partnerships, or counts.

## Known constraints

- All state is local. No account, no server, no sync.
- Rebates cover eight states; everywhere else must degrade honestly rather than
  showing an empty grid with no explanation.
- External dependencies are CDN tags only: Google Fonts and Tabler icons. The
  Tabler URL needs the `/dist/` path segment — without it the CSS 404s and all
  42 icons silently vanish, which is the bug the previous build shipped with.

## Tooling

```bash
npx impeccable detect index.html
```
