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
- [x] Created a top-level "Buy a Car" hub page — links here as the current project, highlights 4 key sub-pages as cards; a home for future car-buying research beyond just this one — see [../Buy a Car/index.md](../Buy%20a%20Car/)
- [x] Added Volkswagen ID.7 (Pro/Pro S) to the premium segment in the price-vs-range dataset and chart
- [x] Rewrote index.md as a proper article: verdict table up top, price-vs-range chart reframed as the computed 8-car efficient frontier (drawn as a connected line, replacing the old unlabelled scatter), tight comparison tables for both tracks, methodology moved down under "The research"
- [x] Added the first real secondhand BYD Dolphin Surf listing (SIPA Mérignac, 2026-08-12, €19,990, 100km, "Occasion récente") to 04 and to the used price-vs-mileage Pareto chart — priced at new, not below it, which corrects the earlier "too new for a secondhand market" note; it becomes the new frontier anchor point at the low-mileage end
- [x] Filled the [06](06-secondhand-price-vs-mileage.html) data gap — real listings sourced for Dacia Spring, Nissan Leaf, Peugeot e-208, VW ID.3, BYD Atto 3, Renault Zoe, plus a range-midpoint for Fiat 500e. Result: the price-vs-mileage frontier collapses to just Dolphin Surf + Dacia Spring, exposing why range/mileage alone is the wrong frontier axis (see top priority above)
- [x] Added reader-facing caveats before both frontier charts (03, 06, and index.md) flagging that Dacia Spring anchors both frontiers on price/range or price/mileage alone despite its 1★ safety rating — plus a new appendix, [12-weighted-quality-score-notes.md](12-weighted-quality-score-notes.md), mapping candidate dimensions and open questions for a real weighted quality score. Design notes only.
- [x] Extended the appendix to a second, equally-broken axis: sticker price is the wrong X-axis on both frontiers — should be annualized cost of ownership (depreciation/yr + running costs/yr + risk-adjusted damage/repair), with a worked example (€60k car depreciating €2k/yr beats €30k car depreciating €3k/yr on true cost). Design notes only — both axes now flagged as the top priority above, still unsolved.
- [x] **First real pass at the price/cost axis** — [13-five-year-cost-of-ownership.html](13-five-year-cost-of-ownership.html): (entry − 5yr resale) + 5yr running costs, for 8 cars across both tracks, using real secondhand listings where available (Spring, Model 3, Model Y) and clearly-flagged estimates where not (Dolphin Surf, ID.7 — both too new for real 5yr data). Findings: secondhand Leaf beats every car here including the Spring; Model Y currently beats Model 3 (thin data, flagged provisional). Genuine progress, not a finished answer — see caveats in 12 and 13.
- [x] **Content architecture cleanup:** trimmed narrative/callouts out of the standalone chart pages (03, 06, 11) that duplicated or belonged in index.md/the numbered docs — chart pages now carry a one-line standalone caption + the chart + data table + source links, with all interpretation living in index.md (03→index.md, 06→04-secondhand-market-survey.md, 11→10-budget-ev-shortlist-comparison.md). Also fixed two stale footer references left over from an earlier template. Reduces the duplicate-editing risk that caused the earlier redundant-callout cleanup.
- [x] Restyled index.md's verdict section as HTML pick-cards (matching the "Buy a Car" hub's visual language: CSS custom-property theme tokens, light/dark aware) with inline SVG car-silhouette icons in place of the old plain markdown table.
- [x] Swapped the SVG icons for real car photos — Wikimedia Commons, CC BY-SA 4.0, downloaded locally to `assets/car-photos/` (not hotlinked) with in-card attribution to the photographer and a license link, satisfying the CC BY-SA attribution/share-alike terms. Nissan Leaf (2018 Tekna, photo by Vauxford) and Tesla Model 3 (2023, photo by Alexander Migl).

## Still to do

- [ ] ⏭️ **TOP PRIORITY — both frontier charts have the wrong axes, not just one.** Quality axis still fully open (see [12](12-weighted-quality-score-notes.md)) — concrete evidence: the used price-vs-mileage frontier collapses to just Dolphin Surf + Dacia Spring, with the Spring dominating on price alone despite 1★ safety. **Price axis has a first pass now** ([13](13-five-year-cost-of-ownership.html)) but isn't rigorous yet: several exit values are estimated not sourced, running costs lean on brackets not full distributions, no damage/repair-risk line item, and no real per-model depreciation *curve* (13 uses single point-in-time listings, not a curve). Both still rank above the other open items below.
- [ ] **Charts embed via iframe, not inline HTML/JS — known limitation, not fixed.** Flowershow renders plain `.md` raw-HTML blocks via something like `innerHTML`, which browsers never execute `<script>` tags from — confirmed live: our inline `<script>` code survives in the published page source untouched, but the SVGs/tables it should populate stay empty. Flowershow does have a `<CustomHtml html={...}/>` component built for exactly this (their own example embeds a Tally form's script), but it requires MDX rendering (`syntaxMode: mdx` in frontmatter, or a `.mdx` file extension) and its docs don't confirm whether inline `<script>` logic (not just external `script src=`) executes through it — untested. Worth revisiting if iframe's mobile UX (fixed height, nested scroll) becomes a real problem.
- [ ] Resolve BYD Dolphin Surf's actual bonus écologique eligibility right now — depends on whether the specific car being bought is still China-built or already from the Hungary plant (ramping up from Q2 2026); the 10-table flags this as uncertain rather than resolving it
- [ ] Get a real Euro NCAP rating for the France-spec Citroën ë-C3 and a rating (once available) for Renault Twingo E-Tech — both currently unrated in this research
- [ ] Deeper used-market pass — individual listing samples (not aggregate/aggregator-summary bands, several still 1-listing anchors after this pass) and battery SOH figures where sellers disclose them, especially for the Nissan Leaf and Peugeot e-208 now that both are leading picks
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
- `12-weighted-quality-score-notes.md` — appendix: design notes for a real price/quality frontier (both the quality axis and the price→annualized-cost axis)
- `13-five-year-cost-of-ownership.html` — first real pass at the price/cost axis: (entry − 5yr resale) + 5yr running costs, 8 cars
- `assets/leboncoin-model-y-listing.png` — the listing screenshot used in 07
- `data-ev-models.json` / `data-used-ev-price-bands.json` — datasets behind the charts
