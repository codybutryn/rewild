# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Single-file HTML: hand-written vanilla JS, no framework, no build step, no package
manager. Open the `.html` directly and it runs. This replaces an earlier build whose
core was a 220 KB minified React bundle with six vanilla modules layered on top of it;
the rewrite exists so the source is readable, the app is fully restylable, and the
repository is worth reading.

## Users

Anyone with outdoor space they could plant into — suburban homeowners with a
conventional lawn, renters with a balcony, and small-plot urban gardeners alike. The
common thread is intent without expertise: they want more life in the space they have
and do not know which plants belong there, what it costs, or what to do this month.

Their situation is seasonal and location-bound. What they should do in August in
Milwaukee is not what they should do in August in Phoenix, and the app's job is to know
the difference on their behalf.

## Product Purpose

ReWild turns "I should plant natives" into a specific plan for a specific plot: which
species suit this location and light, what money is available to offset the work, what
to do this month, and what showed up afterward.

Success is a user who plants something they would not otherwise have planted, and who
comes back the following season because the yard changed.

## Positioning

Three things most native-plant resources keep apart, joined in one place:

1. **Plant guidance tied to a real location and light level**, not a national list.
2. **Cash rebates**, which are the strongest argument for converting lawn and are
   almost never surfaced next to the plants themselves.
3. **A wildlife log**, which turns an abstract ecological claim into evidence the user
   collected in their own yard.

A plant database alone cannot make the money argument. A rebate finder alone cannot say
what to plant. The wildlife log is what makes either worth returning to.

## Operating Context

Used at a desk while planning and on a phone while standing in the yard. Sessions are
short and seasonal: heavy in spring and fall, sparse in winter. Care guidance is
month-specific, so the app is expected to say something different every time it is
opened across a year.

## Capabilities and Constraints

Confirmed and shipping:

- **Yard setup** — state, city, ZIP, square footage, sun exposure, and goals.
- **Plant catalogue** — 17 native species with symbol, scientific name, family,
  category, duration, wildlife value, and an image.
- **Rebate finder** — 17 programs across WI, CO, AZ, CA, MD, DC, NV, and TX, matched by
  state and ZIP prefix, with per-square-foot amounts, caps, and minimums.
- **Wildlife log** — sightings across 7 species groups (bee, butterfly, bird, beetle,
  mammal, amphibian, spider) with a weighted habitat score.
- **Care calendar** — 12 months of guidance across four climate bands (all / cold /
  temperate / warm).
- **Marketplace** — seed products, starter kits, and native nurseries, linking out to
  the sellers.
- **Yard map designer** — a drag-and-place plan of the plot.

Constraints:

- All state lives in `localStorage`. There is no account, no server, and no sync.
- Data is US-only. Rebates cover eight states; everywhere else must degrade honestly.
- No build step is permitted. External dependencies are CDN tags only.

## Brand Commitments

The name is **ReWild**. It is an early-stage real product, not a mockup, and copy should
read as a product that exists — without claiming users, funding, partnerships, or
launch status it does not have.

## Evidence on Hand

- 17 plant records with scientific names and Wikimedia images.
- 17 rebate programs with real program names, real municipal URLs, and dollar figures.
  **Real but unverified**: amounts and eligibility may be stale, so every rebate figure
  must be presented as needing confirmation on the program's own site. The app must
  never imply a guaranteed payout.
- Named real nurseries and seed suppliers with working links.
- Month-by-month care guidance across four climate bands.

Absent, and not to be fabricated: users, testimonials, download or signup counts,
partnerships, press, funding, certifications, and any claim that a rebate is approved.

## Product Principles

1. **Location before advice.** Nothing generic is worth saying. Every recommendation is
   filtered by where the user is and what light they have.
2. **Money is the argument.** Rebates are the most persuasive fact available; surface
   them next to the plants, not in a separate tab nobody opens.
3. **Evidence over assertion.** The wildlife log is the product's proof mechanism. The
   claim "natives support life" should be something the user watches happen.
4. **Honest about what it does not know.** Unverified figures say so. Unsupported
   locations say so. Sample state is labelled as sample state.
5. **The season is the interface.** A visit in March and a visit in September should not
   look the same.

## Accessibility & Inclusion

Used outdoors on phones in bright sun, so contrast and tap-target size are functional
requirements rather than compliance items. Target WCAG AA at minimum.
