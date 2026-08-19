---
name: ReWild — The Field List
description: A waterproof field notebook for your yard — ruled stock, coded rows, running tallies.
colors:
  stock: "#E7EBE3"
  sheet: "#F7F8F5"
  shade: "#DDE3D8"
  graphite: "#1F2420"
  graphite-2: "#4A544C"
  rule: "#B9C4B4"
  rule-firm: "#7E8F73"
  hivis: "#F2C300"
  hivis-deep: "#C79E00"
  survey: "#E2571E"
  survey-ink: "#B03B0F"
  stamp: "#5B3A8C"
  survey-deep: "#C44A14"
  stamp-wash: "rgba(255,255,255,0.42)"
typography:
  display:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(1.9rem, 6vw, 3.4rem)"
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(1.4rem, 3.6vw, 2.1rem)"
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: "-0.025em"
  title:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "1.02rem"
    fontWeight: 800
    lineHeight: 1.5
    letterSpacing: "0.03em"
  body:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "normal"
  label:
    fontFamily: "Azeret Mono, ui-monospace, monospace"
    fontSize: "0.72rem"
    fontWeight: 700
    lineHeight: 1.5
    letterSpacing: "0.1em"
  figure:
    fontFamily: "Azeret Mono, ui-monospace, monospace"
    fontSize: "clamp(1.35rem, 3.4vw, 2rem)"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.03em"
    fontFeature: "tabular-nums"
rounded:
  none: "0"
spacing:
  grid: "22px"
  gutter: "clamp(0.9rem, 3vw, 1.6rem)"
  pad: "clamp(1rem, 3vw, 1.7rem)"
  row: "0.62rem 0.4rem"
components:
  button:
    backgroundColor: "{colors.sheet}"
    textColor: "{colors.graphite}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "0.6rem 1rem"
  button-hover:
    backgroundColor: "{colors.shade}"
  button-go:
    backgroundColor: "{colors.survey}"
    textColor: "#FFFFFF"
    padding: "0.6rem 1rem"
  button-go-hover:
    backgroundColor: "#C44A14"
  button-hi:
    backgroundColor: "{colors.hivis}"
    textColor: "{colors.graphite}"
  button-hi-hover:
    backgroundColor: "{colors.hivis-deep}"
  button-sm:
    padding: "0.34rem 0.6rem"
  chip:
    backgroundColor: "transparent"
    textColor: "{colors.graphite-2}"
    padding: "0.16rem 0.42rem"
    rounded: "{rounded.none}"
  chip-on:
    backgroundColor: "{colors.hivis}"
    textColor: "{colors.graphite}"
  chip-warn:
    backgroundColor: "transparent"
    textColor: "{colors.survey-ink}"
  tab:
    backgroundColor: "{colors.shade}"
    textColor: "{colors.graphite}"
    padding: "0.5rem 0.85rem"
    rounded: "{rounded.none}"
  tab-current:
    backgroundColor: "{colors.sheet}"
    padding: "0.5rem 0.85rem 0.66rem"
  tick:
    backgroundColor: "{colors.sheet}"
    rounded: "{rounded.none}"
    size: "23px"
  tick-on:
    backgroundColor: "{colors.hivis}"
  input-blank:
    backgroundColor: "{colors.sheet}"
    textColor: "{colors.graphite}"
    typography: "{typography.body}"
    padding: "0.5rem 0.6rem"
    rounded: "{rounded.none}"
  option:
    backgroundColor: "transparent"
    textColor: "{colors.graphite}"
    padding: "0.45rem 0.7rem"
  option-on:
    backgroundColor: "{colors.hivis}"
    textColor: "{colors.graphite}"
  panel:
    backgroundColor: "{colors.sheet}"
    textColor: "{colors.graphite}"
    rounded: "{rounded.none}"
  panel-header:
    backgroundColor: "{colors.graphite}"
    textColor: "{colors.sheet}"
    typography: "{typography.label}"
    padding: "0.4rem 0.7rem"
  locality-band:
    backgroundColor: "{colors.hivis}"
    textColor: "{colors.graphite}"
    padding: "0.75rem 0"
  locality-stamp:
    textColor: "{colors.stamp}"
    padding: "0.3rem 0.62rem"
  demo-bar:
    backgroundColor: "{colors.stamp}"
    textColor: "#FFFFFF"
    padding: "0.42rem 0"
---

# Design System: ReWild — The Field List

## Overview

**Creative North Star: "The Rite-in-the-Rain Notebook"**

ReWild is a field book, not an app that happens to be about plants. Every surface behaves like a page of waterproof ruled stock: a cool grey-green ground printed with a real 22px grid, graphite ink, heavy black rules that box the sheet, and a high-visibility cover yellow that marks anything logged, active or tallied. The yard is a running record — dated, coded, tallied rows — and the interface's job is to look like the place that record is kept.

Density is the point. Rows are short, rules are thin and constant, labels are set in mono and shouted small. Nothing floats: there are no shadows anywhere in the build, no rounded corners anywhere in the build, and no soft card surfaces. Depth comes from three tonal grounds (stock behind, sheet in front, shade for pressed and inert regions) separated by 1px printed rules and 2–2.5px graphite borders. Content that reads as a form is drawn as a form: ruled blanks with an underline instead of a box, tick boxes you press, index tabs that sit up over the sheet edge.

This world explicitly refuses the calm-plant-app arrangement — soft cards on a sage ground, generous whitespace, muted pastels, cream paper. The page ground is cool on purpose and is never to be warmed toward cream. Because the image workspace was unavailable, the build is fully code-led: species illustrations are authored SVG plates drawn by growth form, which is what a field guide does anyway.

**Key Characteristics:**
- Printed 22px grid on the page ground, always visible around the sheet
- Zero radius, zero shadow, hard graphite rules at 1px / 2px / 2.5px
- Hi-vis yellow means state (logged / active / tallied); surveyor orange means action
- Azeret Mono is measurement only: codes, figures, tallies, dates, labels
- Tonal stack of three grounds — stock, sheet, shade — instead of elevation
- Exactly one authored motion moment in the whole build

## Colors

Six working roles over three paper grounds: an ink, a ruling, a state flag, an action flag, and a stamp.

### Primary
- **High-Visibility Cover Yellow** (`hivis`): the cover of the notebook. Fills the locality band across the top of every view, a ticked tick box, a selected option, an active chip. It means *this is logged, active, or counted* — never decoration, never a ground for long text. Graphite on it measures 9.45:1.
- **Hi-Vis Pressed** (`hivis-deep`): the hover and pressed state of any hi-vis surface. Nowhere else.

### Secondary
- **Surveyor Flagging Orange** (`survey`): the action colour. Fills the one primary button per view and lights the single emphasized tally figure. Large sizes and fills only.
- **Surveyor Ink** (`survey-ink`): the same flag darkened for anything small — warning chips, the unverified line under a rebate figure, inline caveats.

### Tertiary
- **Locality Stamp Violet** (`stamp`): stamp ink. The rotated locality stamp in the hi-vis band, the record code at the head of every list row, the demo banner, and the focus ring. It marks *where you are* and *what this record is called*. White on violet measures 8.65:1; violet on hi-vis 5.18:1.

### Neutral
- **Waterproof Grid Stock** (`stock`): the page ground behind everything, cool and explicitly never cream. Carries the printed grid.
- **The Sheet** (`sheet`): the whiter page you write on — the interior of the main sheet, panels, the tally band, buttons at rest.
- **Shaded Region** (`shade`): the shaded area of a printed blank — inert tabs, row hover, button hover, the ground behind a drawn plate.
- **Graphite** (`graphite`): pencil ink; all body and heading text, all heavy borders. 14.80:1 on sheet.
- **Secondary Pencil** (`graphite-2`): lede copy, meta text, small-caps labels, scientific names. 7.40:1 on sheet, 6.53:1 on stock.
- **Printed Rule** (`rule`) and **Heavy Rule** (`rule-firm`): the 1px grid line and the 1.5–2px structural stroke on chips, options and month cells. The heavy rule is also the scrollbar thumb.

### Named Rules

**The Two-Orange Rule.** Surveyor orange exists in two values and they are not interchangeable. The bright flag measures 3.51:1 on the sheet — legal for large figures and for white-on-orange fills, and used for nothing else. Any orange text below large size uses the darkened ink (5.66:1). Do not simplify these back into one token; the split is what keeps the flag bright and the caveats readable.

**The Hi-Vis Is State Rule.** Yellow is never applied for emphasis, mood or branding inside the sheet. If a surface is hi-vis, something is logged, active, selected or tallied. If nothing is true of it, it is sheet or shade.

**The Cool Stock Rule.** The page ground is cool grey-green. Warming it toward cream breaks the waterproof-stock premise and is not a fix.

## Typography

**Display Font:** Archivo (with system-ui, sans-serif)
**Body Font:** Archivo (with system-ui, sans-serif)
**Label/Mono Font:** Azeret Mono (with ui-monospace, monospace)

**Character:** Archivo is the printed form — grotesque, tight, set heavy at 800 for anything titular. Azeret Mono is the hand that fills the form in: square, tabular, mechanical. The pairing reads as a document rather than a product.

### Hierarchy
- **Display** (800, `clamp(1.9rem, 6vw, 3.4rem)`, 1.1): the landing headline only, capped at 16ch.
- **Headline** (800, `clamp(1.4rem, 3.6vw, 2.1rem)`, 1.1): the top-of-view heading inside the app.
- **Title** (800, 1.02rem, uppercase, +0.03em): section heads, underlined with a 2px graphite rule, carrying an optional mono note pushed to the right end of that rule.
- **Body** (400, 1rem, 1.5): running copy. Ledes cap at 66ch and set in secondary pencil.
- **Label** (mono 700, 0.70–0.76rem, +0.08em to +0.12em, uppercase): tabs, buttons, field captions, panel headers, chips.
- **Figure** (mono 700, `clamp(1.35rem, 3.4vw, 2rem)` in the tally band, up to `clamp(2rem, 6vw, 3.2rem)` for the habitat score, tabular figures, −0.03em): running totals and scores.

### Named Rules

**The Mono-Is-Measurement Rule.** Azeret Mono is reserved for things that were measured or recorded: record codes, figures, tallies, dates, units, and the small-caps labels that name them. Never a sentence of running prose, never atmosphere.

**The Tabular Figures Rule.** Every number that can change while the user watches is set with tabular figures, so a tally never reflows its own digits.

### Known limit
The in-app heading clamps at 2.1rem, so Archivo 800 gets a genuine display moment only on the landing view. Inside the app the ramp is compressed by design, consistent with a form, but the top of the ramp is currently unexercised.

## Layout

A single centred column at `max-width: 1080px` with a `clamp(0.9rem, 3vw, 1.6rem)` gutter. The page ground is the printed grid — two crossed linear-gradients in the rule colour at a 22px pitch — visible on all sides of the sheet. The sheet itself is a `--sheet` fill with a 2px graphite border on left, right and bottom, open at the top where the index tabs meet it. Interior padding is `clamp(1rem, 3vw, 1.7rem)`.

The vertical order of the shell is fixed and is the world's first viewport: demo bar (when demoing) → hi-vis locality band → four-cell tally band → index tabs → sheet → mono footer.

Two-column content uses a `1fr / 340px` split collapsing to one column at 900px. Catalogue grids use `repeat(auto-fill, minmax(240px, 1fr))`. The tally band drops from four columns to two at 720px and grows an internal horizontal rule. List rows go from `78px / 1fr / auto` to `64px / 1fr` at 640px, with actions wrapping to a full-width third line indented to align under the name column. The locality stamp unpins from the right and centres full-width at 640px. No horizontal overflow at 1440 or 390; all six index tabs stay reachable at 390 because the tab strip wraps rather than scrolls.

**The 22px Pitch Rule.** The grid pitch is the rhythm. Vertical spacing should land near multiples of it rather than on an invented 4/8 scale, and nothing should tile over the ground so completely that the ruling disappears.

## Elevation & Depth

There are no shadows in this system. Not one box-shadow exists in the build, and none should be added. Depth is entirely tonal and linear: three stacked grounds (stock behind, sheet in front, shade for inert or pressed regions) separated by printed rules. Stroke weight encodes hierarchy — 1px rule for a divider inside a list, 2px graphite for a structural edge (sheet border, section underline, tally band base), 2.5px graphite for anything you can press or type into (buttons, tick boxes, panels, ruled blanks).

Depth cues native to this world and permitted: the index tab sitting 2px proud of the sheet edge with its bottom border removed, the panel's inverted graphite header bar, and the locality stamp's −1.2° rotation.

**The No-Lift Rule.** Nothing in this system lifts. If a surface needs to read as nearer, change its ground (shade → sheet), change its border weight, or invert it. Never add a shadow, and never a hard offset shadow, which belongs to a neobrutalist world this one is not.

## Shapes

Radius is zero everywhere, without exception: buttons, chips, tick boxes, panels, plates, inputs, tabs. Corners are square because the world is printed. Borders do the work radius normally does; every interactive element is defined by a rectangle of graphite or heavy rule rather than by a fill.

The recurring silhouettes are the ruled row (78px code column, name/species stack, actions right), the boxed tick, the tab that overlaps the sheet edge, the ruled blank (bottom border only, no box), and the 58×44 plate rectangle.

**The Drawn Plate Rule.** Species imagery is authored SVG, not photography. Four line plates — Grass, Forb/herb, Shrub, Cactus — are drawn by growth form at 58×44 in `currentColor` on the shade ground, keyed off the record's category with Forb/herb as fallback. This is not a placeholder: a field guide draws its plates. It became the answer after all 17 inherited image URLs were found dead (every one 400s at Wikimedia), and it is the world's own solution, so future imagery extends the plate set rather than reverting to photos.

**The Icon Rule.** Icons are the Tabler webfont at its single outline weight, loaded from CDN: 23 distinct glyphs across the app, 9 written directly into markup and the rest supplied by data records for wildlife groups, goals, sun options and marketplace entries. They appear in tick boxes, option toggles, buttons, the locality stamp, empty states and the wildlife log. They are permitted because Tabler is a real drawn library at one consistent stroke, which is what the craft floor asks for — the refusal is Unicode glyphs and emoji standing in for an icon system, not a drawn icon set. Two constraints bind them here: icons take world ink only (`--graphite`, `--hivis`, `--survey`, `--stamp`) and never a per-item colour, which is the rule that removed ~15 inherited Material-palette hexes; and the CDN URL needs its `/dist/` path segment, without which the stylesheet 404s and every icon silently vanishes — the exact bug the superseded build shipped with. Icons label controls; species imagery is the plate set above, never an icon.

## Components

### Buttons
- **Shape:** square (0 radius), 2.5px graphite border, mono uppercase label at +0.08em.
- **Default:** sheet fill, graphite text, `0.6rem 1rem`.
- **Primary (go):** surveyor orange fill, white text, graphite border. One per view — it is the row you add.
- **State (hi):** hi-vis fill, for actions that record something.
- **Small:** `0.34rem 0.6rem`, 0.7rem label, border drops to 2px. Used inline in list rows.
- **Hover / Active:** hover only under `(hover: hover) and (pointer: fine)` — default goes to shade, orange to `#C44A14`, hi-vis to the pressed yellow. Every button presses to `scale(0.97)` in 110ms.

### Chips
- **Style:** mono 0.7rem, 1.5px heavy-rule border, secondary pencil text, no fill.
- **On:** hi-vis fill, graphite border and text at weight 700 — the logged state.
- **Warn:** surveyor-ink border and text, no fill — used for a species outside the yard's climate band.

### Cards / Containers
- **Panel:** 2.5px graphite border, sheet fill, square, no shadow. Header is an inverted bar — graphite fill, sheet text, mono uppercase at +0.12em, `0.4rem 0.7rem`. Body padding `0.8rem 0.85rem`.
- **Rebate block:** 2px graphite border, mono amount at 1.5rem/700, bold progress line, and a mandatory unverified line separated by a 1px dashed surveyor-ink rule.

### Inputs / Fields
- **Ruled blank:** the label is a mono uppercase caption in secondary pencil; the control has no box — sheet fill, no border except a 2.5px graphite bottom rule. Set in mono at 0.92rem because a filled form is written, not typed.
- **Focus:** the global ring, a 2.5px stamp-violet outline at 2px offset, on `:focus-visible` only.
- **Option toggle:** 2px heavy-rule box; when pressed, border goes graphite and fill goes hi-vis at weight 600, in 130ms.

### Navigation
- **Index tabs:** mono 0.74rem uppercase, shade fill, 2px graphite border with the bottom edge removed, sitting 2px proud of the sheet. The current tab takes the sheet fill and grows its bottom padding so it merges with the page. The strip wraps at narrow widths — it never becomes a horizontal scroller, so all six stay reachable at 390px.

### Locality Band (signature)
The hi-vis strip across the top of every view, closed by a 3px graphite bottom border. Brand lockup left (Archivo 800 at 1.22rem with a mono sub-label at 0.7rem); the locality stamp pushed right — mono 0.76rem uppercase, stamp violet, 2.5px violet border, translucent white fill, rotated −1.2°, with an inline underlined change control. The stamp is the one control whose value propagates through the whole record.

### Tally Band (signature)
Four equal cells on the sheet, divided by 1px rules and closed by a 2px graphite base. Each cell is a mono tabular figure over a small uppercase caption in secondary pencil. Exactly one cell per band is lit and prints its figure in surveyor orange. The band runs on the landing view too, on static counts, so the world is present before the first click.

### Coded Row (signature)
The unit of the whole product. `78px / 1fr / auto`: a mono record code in stamp violet, the common name at weight 600 with the scientific name beneath in mono italic secondary pencil, actions right. The plated variant inserts the drawn plate as a second column (`70px / 58px / 1fr / auto`) and drops the plate entirely below 640px. Rows divide on the 1px rule and take a shade ground on hover.

### Tick Box
23px square, 2.5px graphite border, sheet fill. Pressed state fills hi-vis and fades the check in over 120ms; the box presses to `scale(0.92)` in 110ms. It is the gesture the whole product is built around.

### Motion
**The One Moment Rule.** This build spends its entire motion budget on the list re-rank: a FLIP over the plant list when a goal changes, so rows visibly travel to their new rank instead of silently re-rendering (420ms on `cubic-bezier(0.23, 1, 0.32, 1)`, transform only). It is guarded twice — a CSS `prefers-reduced-motion: no-preference` wrapper on the moving class, and a `matchMedia` early return in JS that skips the measurement entirely. Everything else in the system is 110–140ms colour and scale micro-state. A second authored moment is not free: adding one means removing this one.

### Browser surfaces
The palette continues past the document. Selection is hi-vis on graphite, the focus ring is 2.5px stamp violet at 2px offset, and the scrollbar is a heavy-rule thumb with a 3px stock inset on a stock track. Themed browser chrome is part of the world, not an extra.

## Do's and Don'ts

### Do:
- **Do** keep the printed 22px grid on the page ground — two crossed linear-gradients in the rule colour at the grid pitch. It is the signature of the whole world.
- **Do** split orange by size: the bright flag for fills and large figures, the darkened ink for any small text.
- **Do** reserve hi-vis yellow for logged / active / tallied state.
- **Do** set every code, figure, tally, date and label in Azeret Mono with tabular figures, and everything else in Archivo.
- **Do** build depth from the three grounds and border weight (1px / 2px / 2.5px).
- **Do** draw new species imagery as SVG plates by growth form, extending the existing plate set.
- **Do** print truth as content, not as decoration: every rebate figure carries its own unverified line as body copy under a dashed surveyor-ink rule, a species outside the yard's climate band is flagged on its own row with a warn chip, and the marketplace states in its lede that it takes no commission. These are visual rules here, not copy to tidy away.
- **Do** guard any motion twice — CSS `prefers-reduced-motion` and a JS `matchMedia` return.

### Don't:
- **Don't** add a box-shadow. There are none in this system, and a hard offset shadow in particular belongs to a neobrutalist world this one is not.
- **Don't** add a corner radius. Zero, everywhere.
- **Don't** warm the ground toward cream. The stock is cool by design.
- **Don't** flatten the two oranges into one token, and don't set small text in the bright flag (3.51:1 — it fails AA below large sizes).
- **Don't** replace the printed grid with a flat fill or tile a full-bleed surface over it.
- **Don't** introduce a kicker or eyebrow line above a heading. The mono sub-label exists once, inside the brand lockup, and is not a pattern to repeat.
- **Don't** use Azeret Mono for running prose or for atmosphere.
- **Don't** add a second authored motion moment while the list re-rank stands.
- **Don't** animate the tick box beyond its existing 110–120ms press; it is hit constantly.
- **Don't** substitute photography for the drawn plates.

### Open, not shipped
Named in the finish review and deliberately not built: real tally strokes, a serialized sheet header (SHEET __ OF __, REC. BY), dotted leader lines, a perforation edge, a carbon-duplicate tint, and a printed form number in the footer. These are candidate extensions of the world, not current rules — nothing in the build implements them.
