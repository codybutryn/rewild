# ReWild — the field list for your yard

Native plants matched to your location and light, the cash rebates that pay for
replacing lawn, and a wildlife log that turns the argument into something you
watched happen.

**One HTML file. No framework, no build step, no package manager, no backend.**
Open `index.html` in a browser and it runs.

## What it does

| Section | |
| --- | --- |
| **My yard** | Locality, plot size, sun and goals — the one control everything else reads from |
| **Plants** | 17 native species, ranked against your goals, re-ranking in place when you change them |
| **Rebates** | 17 real programs across WI, CO, AZ, CA, MD, DC, NV and TX, matched by state and ZIP |
| **Wildlife** | A sighting log across 7 species groups, weighted into a habitat score |
| **Calendar** | 12 months of care guidance across four climate bands |
| **Marketplace** | Seed, starter kits and native nurseries — links out, sells nothing |

The landing screen offers a worked demo yard (Milwaukee, WI) or your own setup.
All state lives in `localStorage`; nothing is sent anywhere.

## On the rebate figures

The programs, amounts, and URLs are **real but unverified** — amounts and
eligibility change, and this app is not a party to any of them. Every figure in
the UI says so on its own row. Confirm on the program's site before counting on
the money.

## Photographs

Each of the 17 species carries a photograph from Wikimedia Commons, bundled in
`assets/` rather than hotlinked — the previous build shipped with 17 dead image
URLs, and linking to files that can be renamed upstream re-earns that failure.
Every licence was verified before download and every photo is credited on its
plant sheet; the full list is in [CREDITS.md](CREDITS.md).

You can also photograph your own plants and sightings. Those images are resized
and stored in your browser only — never uploaded, never sent anywhere.

## Design

The interface is a field notebook: waterproof grid stock, a high-visibility
locality band, a violet locality stamp, graphite ink, and species codes set in
mono. Rows are dated, coded and tallied, because that is what a field list is.

The full system — palette, type ramp, component grammar, named rules — is in
[DESIGN.md](DESIGN.md), derived from the shipped code. Product truth is in
[PRODUCT.md](PRODUCT.md).

One authored motion moment: change a goal on the Plants view and the list
FLIP-animates its re-rank, so a changed constraint is something you see happen
rather than something that silently already happened. It is disabled under
`prefers-reduced-motion`.

Built with [Impeccable](https://github.com/pbakaus/impeccable).

## Running it

No install. Open the file. To serve it over HTTP instead:

```bash
npx http-server -p 8433 -c-1
```

## Editing

Everything is in `index.html`: tokens in `:root`, one `<style>` block, then
plain functions that build HTML strings and one `render()` that swaps them into
`#app`. Data lives in a single `DATA` object near the top of the script.

To add a plant, push a record onto `DATA.plants` with `symbol`, `name`,
`sciName`, `family`, `category`, `duration`, `wildlifeValue` and `imageUrl`.
To add a rebate, push onto `DATA.rebates` with `state`, `city`, `zip_prefixes`,
`program`, `amount_per_sqft`, `max_amount`, `min_sqft`, `description` and `url`.

## History

This replaces an earlier build whose core was a 220 KB minified React bundle
with six vanilla modules patching its DOM after mount. The rewrite exists so the
source is readable, the design is fully changeable, and the repository is worth
opening. The old builds are kept locally but not published — they embed a live
Supabase project URL and key, and nothing here needs them.

## License

Code is available for reference. The ReWild name and content are not licensed
for reuse.
