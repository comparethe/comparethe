# Appendix: notes toward a real price/quality frontier

Both efficient-frontier charts in this project ([03](03-price-range-sketch.html) for new cars, [06](06-secondhand-price-vs-mileage.html) for used) have **two axes wrong, not one**: the quality axis (currently WLTP range or mileage as a stand-in) and the price axis (currently sticker price, which is the wrong number to optimize against). Neither is solved here — these are design notes for the next pass, tracked as the top priority in [plan.md](plan.md), not a computed result.

## Axis 1: a real weighted quality score

### Why this is now a blocking problem, not a nice-to-have

Both frontiers are currently anchored by the **Dacia Spring** — cheapest car in the survey, and (on the used chart) undominated on price at any mileage out to 160,000km. A frontier built on price and one axis alone will keep recommending the Spring. But the Spring is **ruled out elsewhere in this project on Euro NCAP safety (1★, 49% adult / 56% child)** — see [04](04-secondhand-market-survey.md) and the Track A table in [index.md](index.md). Range-only and mileage-only frontiers can't see that, or anything else that actually separates a €7,500 Spring from a €19,990 Dolphin Surf with similar WLTP range: safety, charging speed, battery thermal management, warranty, interior quality.

### Candidate dimensions for a composite score

Roughly in order of how well-sourced each already is in this project:

| Dimension | Status here | Notes |
|---|---|---|
| **Range (WLTP)** | Well sourced | Current stand-in for new-car quality; overstates real-world range, especially in winter |
| **Euro NCAP safety** | Well sourced for the budget shortlist ([04](04-secondhand-market-survey.md)) | Star rating alone is lossy — a 1★ and 5★ car aren't "80 percentage points apart" in real risk; sub-scores (adult/child/VRU/assist) may need separate weights, and protocol-year matters (Zoe went 5★→0★ on the same car, no redesign) |
| **Charging speed** | Sourced for some models (kW figures, 10-80% times) but not systematically for all | Matters far more for Track B (longer trips) than Track A (school run); needs a "minutes to add 200km" normalization, not raw kW |
| **Boot/cargo space** | Only mentioned qualitatively (Model Y vs. Model 3) | Not sourced systematically — would need a real pass |
| **Brand reliability** | Not sourced at all | No consumer-reliability-survey data (e.g. an equivalent to JD Power/What Car?) has been pulled into this project yet |
| **Battery health / degradation risk** | Not sourced for used cars beyond anecdotal notes (Leaf "Rapidgate", Tesla >15% loss under 100k km) | Matters a lot for used cars specifically — a used-car quality score probably needs this as its own axis, not folded into "range" |

Note: depreciation, resale, and running costs used to be listed here as quality dimensions — they've moved to Axis 2 below, since annualized cost is really where they belong, not a "quality" score.

### Open methodological questions, unresolved

- **Weighting.** Equal weights are the easy default and almost certainly wrong — safety plausibly deserves a much higher weight than boot space for a family car, but "much higher" needs a defensible number, not a guess dressed up as one.
- **Hard filters vs. weighted penalties.** Does a 1★ or 0★ safety car get excluded outright (as Track A already effectively does for the Spring and Zoe), or does it just lose a lot of points in a composite score and still theoretically win on price alone? The two produce different frontiers.
- **New vs. used need different scores.** A new-car score can lean on range/charging/safety as specified. A used-car score needs degradation risk, remaining warranty, and actual condition — specs alone undersell how different a well-maintained vs. neglected used EV can be.
- **Normalizing very different units.** Range (km), charging speed (kW or minutes), safety (%) — putting these on a common 0-1 scale before weighting is a real methodological choice (min-max vs. percentile vs. something else), not a mechanical step.
- **Where does this live?** Two options: (a) one composite frontier chart replacing 03 and 06, or (b) keep range/mileage frontiers as-is (they're honest about what they show) and add a separate weighted scorecard alongside them, similar in spirit to the existing budget shortlist table in [10](10-budget-ev-shortlist-comparison.md) but covering all tracks.

### What exists already that a real pass could build on

- Euro NCAP sub-scores for the whole budget shortlist ([04](04-secondhand-market-survey.md))
- Charging speed figures for several models (ID.3, ID.7, Model 3/Y)
- A working frontier-computation pattern already implemented twice (in [03](03-price-range-sketch.html) and [06](06-secondhand-price-vs-mileage.html)) that a composite-axis version could reuse directly

## Axis 2: price should be annualized cost of ownership, not sticker price

Sticker/purchase price is the wrong X-axis. What actually matters is **what it costs to own the car per year** — depreciation + running costs (insurance, maintenance, charging) + a risk-adjusted allowance for damage/repair, not the number on the price tag.

**Worked example of why this isn't a rounding error:** a €60,000 car depreciating €2,000/year is a *better* buy on this axis than a €30,000 car depreciating €3,000/year, even though it costs twice as much upfront — the cheaper car is actually losing you more money every year you own it. Sticker price alone gets this backwards. Every frontier in this project so far plots sticker price, which means every "cheap" pick on it could be a false economy if its depreciation curve is steep enough. This is exactly the kind of thing the [model & TCO survey](02-model-tco-survey.md) already flags in general (50-60% depreciation over 3yr for EVs vs. 30-40% for petrol, and it varies a lot by model — e-208 and Model 3 hold value unusually well) — but no chart in this project actually plots against it yet.

What an annualized-cost axis needs, roughly:

- **Depreciation/year** — needs a real curve per model (not just "50-60% over 3 years" in aggregate), since the whole point of the worked example above is that the *rate*, not the starting price, is what matters
- **Running costs/year** — already sourced for the budget shortlist in [10](10-budget-ev-shortlist-comparison.md) (insurance, maintenance, charging), not yet extended to Track B or the premium segment
- **Risk-adjusted damage/repair cost** — not sourced anywhere in this project yet; would need something like average repair cost data or insurance claim-rate proxies per model, which is a genuinely new research pass, not a re-slice of existing data
- **Time horizon** — annualizing requires picking a holding period (3yr? 5yr? until resale?), and the answer probably changes the ranking, especially for cars with non-linear depreciation curves (steep early, flatter later)

This reframes the x-axis for *both* frontier charts, not just one — the same fix applies to 03 (new) and 06 (used) once a per-model depreciation curve exists.

**Update:** a first attempt now exists — [13-five-year-cost-of-ownership.html](13-five-year-cost-of-ownership.html) computes this for 8 cars across both tracks. It's a genuine first pass, not the rigorous version described above: several exit (5-year resale) values are estimated rather than sourced (BYD Dolphin Surf, VW ID.7 — both too new to have real 5-year-old examples), running costs lean on project-established brackets rather than full distributions, and there's still no damage/repair-risk line item. Worth reading alongside its caveats, not as a finished answer — but it's real progress on this axis specifically.

---

Nothing here is decided — this is a map of the problem on both axes, not a plan of record.
