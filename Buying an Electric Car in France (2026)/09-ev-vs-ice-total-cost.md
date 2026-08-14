# Is an EV actually better value than petrol, once everything is counted?

The running-cost numbers in [02-model-tco-survey.md](02-model-tco-survey.md) already show EVs cheaper to run day-to-day. But "cheaper to run" isn't the same as "better value" — EVs also cost more to buy new and depreciate faster (50-60% over 3 years vs. 30-40% for petrol, per 02). This piece puts purchase price, depreciation, and running costs together to answer the actual question: **if I factor in everything, would a cheap petrol car beat an EV on value right now?**

## Running costs, EV vs. petrol (annual)

| | EV | Petrol |
|---|---|---|
| Fuel/charging | €2.50-2.80/100km home charging (~€325-365/yr at 13,000km) | SP95-E10 ~€1.85/L (spring 2026) × ~6L/100km ≈ €14.4/100km (~€1,872/yr at 13,000km) |
| Maintenance | €381-700/yr | €535-1,200/yr |
| Insurance | €784-818/yr (citadine entry-level closer to ~€600/yr regardless of powertrain) | €735-753/yr |
| **Combined** | **~€4,300/yr** (entretien + assurance + recharge, per 02) | **~€5,250/yr** (per 02) |

Running costs alone: **EV saves roughly €950/year**, mostly from the fuel/charging gap — home charging runs at less than a fifth the cost per km of petrol at spring-2026 pump prices. Insurance is the one line where EVs now cost *more* (the TSCA tax exemption that used to offset this ended in 2025), though that gap is narrower for cheap city cars (~€600/yr either way) and has been shrinking generally as insurers get more comfortable with EV claims data — it was +25-40% a few years ago, now +9-16%.

## Two worked examples, purchase price included

Depreciation is the thing that could flip this, since EVs lose value faster. Working it through for a 3-year ownership horizon, comparing new prices, resale value, and 3 years of running costs — both *without* and *with* the bonus écologique (up to €5,700 for lower-income households) applied to the EV side:

**Budget segment: Dacia Spring vs. Dacia Sandero (petrol)**

| | Spring (EV) | Spring w/ bonus | Sandero (petrol) |
|---|---|---|---|
| New price | €16,900 | €11,200 | €12,490 |
| 3yr resale (~55% EV budget, ~50% petrol citadine — both estimated) | €9,295 | €9,295 | €6,245 |
| Depreciation cost | €7,605 | €1,905 | €6,245 |
| 3yr running costs (~€4,300/yr EV, ~€5,250/yr petrol) | €12,900 | €12,900 | €15,750 |
| **3yr total** | **€20,505** | **€14,805** | **€21,995** |

**Mainstream segment: Peugeot e-208 vs. Peugeot 208 (petrol)**

| | e-208 (EV) | e-208 w/ bonus | 208 (petrol) |
|---|---|---|---|
| New price | €21,950 | €16,250 | €17,950 |
| 3yr resale (~62% e-208, ~55% petrol 208, both sourced in 02) | €13,609 | €13,609 | €9,873 |
| Depreciation cost | €8,341 | €2,641 | €8,077 |
| 3yr running costs | €12,900 | €12,900 | €15,750 |
| **3yr total** | **€21,241** | **€15,541** | **€23,827** |

**Verdict, held loosely:** in both examples, the EV comes out ahead over 3 years even *without* any incentive — by a modest €1,490 (budget) to €2,586 (mainstream) — because the running-cost savings outweigh the faster depreciation. With the bonus écologique applied, the gap opens up substantially, €6,000-7,000 in the EV's favor. A cheap petrol car is not obviously better value on this analysis, even at the pure-budget end.

## Where this could flip, and what would change it

- **Battery health risk isn't priced in here.** A resale estimate assumes an average car; a genuinely degraded battery (per the SOH warnings throughout this project) could push actual EV resale well below the ~55-62% used above, closing or reversing the gap. This is the single biggest wildcard.
- **Low annual mileage weakens the EV case.** The whole running-cost advantage comes from the fuel/charging gap, which scales with distance driven. At very low annual mileage (well under the ~13,000km French average used here), the running-cost savings shrink and the EV's depreciation disadvantage matters proportionally more — worth recomputing for the actual school-run/short-trip use case this project has in mind, which likely drives meaningfully fewer km/year than the national average.
- **No incentive eligibility narrows things.** The bonus écologique needs income under set thresholds (see [01-tax-incentives.md](01-tax-incentives.md)) — without it, the EV's advantage is real but much smaller (roughly €1,500-2,600 over 3 years in the examples above, not several thousand).
- **Longer or shorter ownership horizons shift the math** — EVs depreciate more in the first 3 years but the running-cost savings keep compounding every year after, so a longer hold likely favors EVs more, not less.

## Caveats

This is a **first-cut model, not a certified TCO calculator**: fuel consumption (6L/100km), annual mileage (13,000km), and resale percentages are estimates from earlier research and general French averages, not model-specific figures for the Spring/Sandero/e-208/208 pairing directly. Running costs use the blended EV/petrol averages from 02, not figures specific to these exact models. Treat the *direction* of the answer (EV ahead, even before incentives, for anyone driving close to average French mileage) as reasonably solid; treat the exact euro figures as ballpark.

Sources: [02-model-tco-survey.md](02-model-tco-survey.md) (running costs, resale %) · [01-tax-incentives.md](01-tax-incentives.md) (bonus écologique) · [LegiPermis (assurance EV vs essence 2026)](https://www.legipermis.com/blog/2026/03/05/cout-assurance-voiture-electrique-vs-essence/) · [supercarbu.fr (prix carburant 2026)](https://supercarbu.fr/guide/evolution-prix-carburant-2026/) · [prix-carburant.eu (baromètre janvier 2026)](https://prix-carburant.eu/barometre-mensuel-2026-01) · [manouvellevoiture.com (Peugeot 208 essence prix)](https://www.manouvellevoiture.com/actualites/peugeot-208-essence-prix-modeles-et-offres-2025) · [euromotor.fr (Dacia Sandero prix 2026)](https://euromotor.fr/blog/dacia-sandero-2026-prix-fiche-technique-avis/) · [autovillage.fr (Dacia Sandero prix)](https://autovillage.fr/actus/quelle-est-le-prix-dacia-sandero/)
