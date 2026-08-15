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
- [x] Two concrete recommendation tracks in index.md — budget/secondhand/short-range vs. nicer everyday family car — replacing the earlier single-list recommendation
- [x] Extended secondhand survey to the budget segment: Fiat 500e has a real (and wide) secondhand market; confirmed Twingo E-Tech and ë-C3 are too new to have one yet — see [04-secondhand-market-survey.md](04-secondhand-market-survey.md)
- [x] EV vs. petrol (ICE) total cost of ownership, purchase price + depreciation + running costs together — see [09-ev-vs-ice-total-cost.md](09-ev-vs-ice-total-cost.md)
- [x] Euro NCAP safety pass on the budget/family shortlist — decisive, reshuffled the list: Leaf (5★) top pick, Fiat 500e (4★) second, Dacia Spring/Zoe (1★/0★) ruled out despite price — see [04-secondhand-market-survey.md](04-secondhand-market-survey.md)
- [x] Budget-track recommendation confirmed: secondhand Nissan Leaf, per real annual mileage (~10,000km/yr, confirmed low-mileage isn't a risk to the EV-vs-ICE case) and home-charging-dependent range math
- [x] Added BYD Dolphin Surf and Peugeot e-208 to the safety pass — both also 5★, genuinely competing with the Leaf recommendation, not just fallbacks
- [x] **Correction:** the Citroën ë-C3's earlier "0-star" rating was for a different, India-spec car (Global NCAP), not the France-market ë-C3, which is actually unrated — fixed in 04 and index.md
- [x] Full comparison table — new + secondhand, price, ~75%-incentive net price, safety, range, maintenance/yr, and total running cost/yr at 10,000km — see [10-budget-ev-shortlist-comparison.md](10-budget-ev-shortlist-comparison.md)
- [x] Stacked bar chart, base price + 3yr maintenance per car, sorted by total — see [11-budget-shortlist-cost-bars.html](11-budget-shortlist-cost-bars.html)
- [x] Added VW ID.3 to Track B — new price (€34,990-48,100), secondhand (€17,790-39,990), 5-star Euro NCAP, fast charging — see [04-secondhand-market-survey.md](04-secondhand-market-survey.md) and index.md

## Still to do

- [ ] **Charts embed via iframe, not inline HTML/JS — known limitation, not fixed.** Flowershow renders plain `.md` raw-HTML blocks via something like `innerHTML`, which browsers never execute `<script>` tags from — confirmed live: our inline `<script>` code survives in the published page source untouched, but the SVGs/tables it should populate stay empty. Flowershow does have a `<CustomHtml html={...}/>` component built for exactly this (their own example embeds a Tally form's script), but it requires MDX rendering (`syntaxMode: mdx` in frontmatter, or a `.mdx` file extension) and its docs don't confirm whether inline `<script>` logic (not just external `script src=`) executes through it — untested. Worth revisiting if iframe's mobile UX (fixed height, nested scroll) becomes a real problem.
- [ ] Resolve BYD Dolphin Surf's actual bonus écologique eligibility right now — depends on whether the specific car being bought is still China-built or already from the Hungary plant (ramping up from Q2 2026); the 10-table flags this as uncertain rather than resolving it
- [ ] Get a real Euro NCAP rating for the France-spec Citroën ë-C3 and a rating (once available) for Renault Twingo E-Tech — both currently unrated in this research
- [ ] ⏭️ Real price-vs-quality efficient frontier — weight charging speed, safety, boot space, brand reliability etc. instead of range/mileage-only; run it on new *and* used prices together. Safety data now exists for the budget shortlist and should be a weighted factor, not just a filter
- [ ] Deeper used-market pass — individual listing samples (not aggregate/aggregator-summary bands) and battery SOH figures where sellers disclose them, especially for the Nissan Leaf and Peugeot e-208 now that both are leading picks
- [ ] Extend the price-vs-mileage chart to the used candidates that don't have mileage sourced yet: Zoe, Leaf, e-208, ID.3, Atto 3, Dacia Spring, Fiat 500e
- [ ] Confirm home charging access — the Leaf recommendation assumes overnight home charging; public-only charging would weaken the case
- [ ] Flesh out 08-why-buying-a-used-car-is-hard.md — more worked examples, a proper checklist; decide if/when it splits into its own piece outside this folder
- [ ] Weigh VW ID.3 properly against Model 3/e-208 in Track B — currently just added as a name with data, not yet compared in any depth
- [ ] Final recommendation and purchase decision — Track A (budget) narrowed to Leaf/e-208/Dolphin Surf pending the incentive question; Track B (family) still open, now three-way between Model 3, e-208, and ID.3

## Files

- `index.md` — the article
- `plan.md` — this file
- `01-tax-incentives.md` — bonus écologique, leasing social, malus, sources
- `02-model-tco-survey.md` — models surveyed, running costs, depreciation trends, sources
- `03-price-range-sketch.html` — interactive new-car price-vs-range chart
- `04-secondhand-market-survey.md` — used-listing price bands, sources, Euro NCAP safety data
- `05-secondhand-price-bands.html` — used price-band chart, Tesla by trim
- `06-secondhand-price-vs-mileage.html` — used price-vs-mileage Pareto sketch
- `07-reading-a-real-listing.md` — Model Y vs. Model 3 secondhand + a real listing priced against the research
- `08-why-buying-a-used-car-is-hard.md` — stub piece on the general problem
- `09-ev-vs-ice-total-cost.md` — is EV actually better value than petrol, purchase price + depreciation + running costs
- `10-budget-ev-shortlist-comparison.md` — full table: new/secondhand, price, incentive-adjusted price, safety, range, running costs
- `11-budget-shortlist-cost-bars.html` — stacked bar chart, base price + 3yr maintenance per car
- `assets/leboncoin-model-y-listing.png` — the listing screenshot used in 07
- `data-ev-models.json` / `data-used-ev-price-bands.json` — datasets behind the charts
