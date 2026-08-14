# Plan of work

Working task list for this piece — the [index.md](index.md) article is the writeup; this is the status tracker.

## Done

- [x] Tax incentives — see [01-tax-incentives.md](01-tax-incentives.md)
- [x] Model & TCO survey — see [02-model-tco-survey.md](02-model-tco-survey.md)
- [x] First-cut new-car price vs. range chart (22 trims) — see [03-price-range-sketch.html](03-price-range-sketch.html)
- [x] Secondhand market survey — see [04-secondhand-market-survey.md](04-secondhand-market-survey.md)
- [x] Secondhand price-band chart, Tesla by trim tier — see [05-secondhand-price-bands.html](05-secondhand-price-bands.html)
- [x] Price-vs-mileage Pareto sketch — see [06-secondhand-price-vs-mileage.html](06-secondhand-price-vs-mileage.html)
- [x] Worked case study: Model Y vs. Model 3 secondhand + pricing a real LeBonCoin listing — see [07-reading-a-real-listing.md](07-reading-a-real-listing.md)
- [x] Stub: why it's hard to tell if a used car is a good deal — see [08-why-buying-a-used-car-is-hard.md](08-why-buying-a-used-car-is-hard.md)

## Still to do

- [ ] **Charts embed via iframe, not inline HTML/JS — known limitation, not fixed.** Flowershow renders plain `.md` raw-HTML blocks via something like `innerHTML`, which browsers never execute `<script>` tags from — confirmed live: our inline `<script>` code survives in the published page source untouched, but the SVGs/tables it should populate stay empty. Flowershow does have a `<CustomHtml html={...}/>` component built for exactly this (their own example embeds a Tally form's script), but it requires MDX rendering (`syntaxMode: mdx` in frontmatter, or a `.mdx` file extension) and its docs don't confirm whether inline `<script>` logic (not just external `script src=`) executes through it — untested. Worth revisiting if iframe's mobile UX (fixed height, nested scroll) becomes a real problem.
- [ ] ⏭️ Real price-vs-quality efficient frontier — weight charging speed, safety, boot space, brand reliability etc. instead of range/mileage-only; run it on new *and* used prices together
- [ ] Deeper used-market pass — individual listing samples (not aggregate/aggregator-summary bands) and battery SOH figures where sellers disclose them
- [ ] Extend the price-vs-mileage chart to the used candidates that don't have mileage sourced yet: Zoe, Leaf, e-208, ID.3, Atto 3, Dacia Spring
- [ ] Flesh out 08-why-buying-a-used-car-is-hard.md — more worked examples, a proper checklist; decide if/when it splits into its own piece outside this folder
- [ ] Final recommendation and purchase decision

## Files

- `index.md` — the article
- `plan.md` — this file
- `01-tax-incentives.md` — bonus écologique, leasing social, malus, sources
- `02-model-tco-survey.md` — models surveyed, running costs, depreciation trends, sources
- `03-price-range-sketch.html` — interactive new-car price-vs-range chart
- `04-secondhand-market-survey.md` — used-listing price bands, sources
- `05-secondhand-price-bands.html` — used price-band chart, Tesla by trim
- `06-secondhand-price-vs-mileage.html` — used price-vs-mileage Pareto sketch
- `07-reading-a-real-listing.md` — Model Y vs. Model 3 secondhand + a real listing priced against the research
- `08-why-buying-a-used-car-is-hard.md` — stub piece on the general problem
- `assets/leboncoin-model-y-listing.png` — the listing screenshot used in 07
- `data-ev-models.json` / `data-used-ev-price-bands.json` — datasets behind the charts
