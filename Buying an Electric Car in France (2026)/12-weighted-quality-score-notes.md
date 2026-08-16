# Appendix: notes toward a real weighted quality score

Both efficient-frontier charts in this project ([03](03-price-range-sketch.html) for new cars, [06](06-secondhand-price-vs-mileage.html) for used) currently use a single stand-in for "quality": WLTP range for new cars, mileage for used ones. That's not solved here — this is a design note for the next pass, tracked as the top priority in [plan.md](plan.md), not a computed result.

## Why this is now a blocking problem, not a nice-to-have

Both frontiers are currently anchored by the **Dacia Spring** — cheapest car in the survey, and (on the used chart) undominated on price at any mileage out to 160,000km. A frontier built on price and one axis alone will keep recommending the Spring. But the Spring is **ruled out elsewhere in this project on Euro NCAP safety (1★, 49% adult / 56% child)** — see [04](04-secondhand-market-survey.md) and the Track A table in [index.md](index.md). Range-only and mileage-only frontiers can't see that, or anything else that actually separates a €7,500 Spring from a €19,990 Dolphin Surf with similar WLTP range: safety, charging speed, battery thermal management, warranty, interior quality.

## Candidate dimensions for a composite score

Roughly in order of how well-sourced each already is in this project:

| Dimension | Status here | Notes |
|---|---|---|
| **Price** | Well sourced (new + used bands) | The one axis every chart already has |
| **Range (WLTP)** | Well sourced | Current stand-in for new-car quality; overstates real-world range, especially in winter |
| **Euro NCAP safety** | Well sourced for the budget shortlist ([04](04-secondhand-market-survey.md)) | Star rating alone is lossy — a 1★ and 5★ car aren't "80 percentage points apart" in real risk; sub-scores (adult/child/VRU/assist) may need separate weights, and protocol-year matters (Zoe went 5★→0★ on the same car, no redesign) |
| **Charging speed** | Sourced for some models (kW figures, 10-80% times) but not systematically for all | Matters far more for Track B (longer trips) than Track A (school run); needs a "minutes to add 200km" normalization, not raw kW |
| **Depreciation / resale** | Sourced in aggregate ([02](02-model-tco-survey.md)) but not per-model consistently | e-208 and Model 3 resale unusually well; feeds back into whether "price" should be purchase price or 3-year cost |
| **Running costs (insurance, maintenance, charging)** | Sourced for the budget shortlist ([10](10-budget-ev-shortlist-comparison.md)) | Could fold into an effective "3-year total cost" price axis instead of a separate quality dimension |
| **Boot/cargo space** | Only mentioned qualitatively (Model Y vs. Model 3) | Not sourced systematically — would need a real pass |
| **Brand reliability** | Not sourced at all | No consumer-reliability-survey data (e.g. an equivalent to JD Power/What Car?) has been pulled into this project yet |
| **Battery health / degradation risk** | Not sourced for used cars beyond anecdotal notes (Leaf "Rapidgate", Tesla >15% loss under 100k km) | Matters a lot for used cars specifically — a used-car quality score probably needs this as its own axis, not folded into "range" |

## Open methodological questions, unresolved

- **Weighting.** Equal weights are the easy default and almost certainly wrong — safety plausibly deserves a much higher weight than boot space for a family car, but "much higher" needs a defensible number, not a guess dressed up as one.
- **Hard filters vs. weighted penalties.** Does a 1★ or 0★ safety car get excluded outright (as Track A already effectively does for the Spring and Zoe), or does it just lose a lot of points in a composite score and still theoretically win on price alone? The two produce different frontiers.
- **New vs. used need different scores.** A new-car score can lean on range/charging/safety as specified. A used-car score needs degradation risk, remaining warranty, and actual condition — specs alone undersell how different a well-maintained vs. neglected used EV can be.
- **Normalizing very different units.** Range (km), charging speed (kW or minutes), safety (%), price (€) — putting these on a common 0-1 scale before weighting is a real methodological choice (min-max vs. percentile vs. something else), not a mechanical step.
- **Where does this live?** Two options: (a) one composite frontier chart replacing 03 and 06, or (b) keep range/mileage frontiers as-is (they're honest about what they show) and add a separate weighted scorecard alongside them, similar in spirit to the existing budget shortlist table in [10](10-budget-ev-shortlist-comparison.md) but covering all tracks.

## What exists already that a real pass could build on

- Euro NCAP sub-scores for the whole budget shortlist ([04](04-secondhand-market-survey.md))
- Charging speed figures for several models (ID.3, ID.7, Model 3/Y)
- A working frontier-computation pattern already implemented twice (in [03](03-price-range-sketch.html) and [06](06-secondhand-price-vs-mileage.html)) that a composite-axis version could reuse directly

Nothing here is decided — this is a map of the problem, not a plan of record.
