# Secondhand Market Survey (France, 2026)

First pass at real used-listing price ranges, not aggregate depreciation stats. Pulled from listing-aggregator summaries (La Centrale, AutoScout24, L'Argus Occasion, LeBonCoin, Le Parking) via search — not individually verified per-listing, so treat as ballpark for shortlisting. Same caveat as the other research files: mostly SEO/blog aggregation, not raw marketplace data pulls.

**Market context:** average used-EV price in France fell below €20k in H2 2025 (~€19,990 at Q2 2025), driven by end-of-lease returns pushing supply up; typical used-EV mileage is 30,000-90,000km. Decote up to 50% over 3 years on some models (consistent with the depreciation note in [02-model-tco-survey.md](02-model-tco-survey.md)).

## Tesla Model 3 — the headline "check secondhand even though not buying new" candidate

Wide spread by year/version/mileage. Rough bands (Tesla-Mag analysis, cross-checked against La Centrale's ~€32k-48k typical-listing range):

| Version | Year | Mileage | Price |
|---|---|---|---|
| Propulsion/SR+ | 2019 | 100-150k km | €13,000-17,000 |
| Propulsion/SR+ | 2021 | 50-90k km | €19,000-25,000 |
| Propulsion/SR+ | 2023 | 20-50k km | €26,000-32,000 |
| Highland (2024 facelift) | 2024 | <30k km | €28,000-35,000 |
| Grande Autonomie (Long Range) | 2021 | 50-90k km | €24,000-30,000 |
| Grande Autonomie | 2022-2023 | 20-60k km | €27,000-36,000 |
| Performance | 2022 | 20-50k km | €30,000-37,000 |

**Battery/condition notes:** >15% capacity loss under 100,000km is the flag threshold; pre-Oct-2020 cars lack a heat pump and lose 35-40% winter range vs. 20-25% for equipped cars; 8yr/160,000km battery warranty transfers to a new owner; HW2.5 (2017-19) cars can't run current FSD/Autopilot software — irrelevant for FSD but check if any driver-assist features matter.

**Read on this**: an early-2020s Model 3 (2021-22, 50-90k km, Propulsion/SR+) at ~€20-28k lands well inside the mainstream-new-car price band from [03-price-range-sketch.html](03-price-range-sketch.html) while likely beating everything on that chart for range/charging speed — worth putting on the frontier once feature weights exist.

## Tesla Model Y — the other "look even though above new-car budget" candidate

- Broad 2026 used range: **€28,000-33,000** depending on mileage — about €20k under a new one.
- Tesla-Mag breakdown: Propulsion 2022 (40-80k km) €27-33k · Propulsion 2023 (20-50k km) €31-38k · Juniper facelift 2024 (<25k km) €36-43k · Grande Autonomie AWD 2022 €33-40k · 2023 €37-44k · Juniper GA 2024 (<20k km) €42-49k · Performance 2022-23 €38-47k.
- Same battery-warranty transfer (4-5 years typically left on the 8yr/192,000km warranty for a 2-3yr-old car) and free lifetime software updates as Model 3.

## Other used candidates surveyed

- **Peugeot e-208**: wide range **€18,000-35,000**; very-low-mileage nearly-new cars (2026 reg, <10,000km) cluster €24-31k — barely a discount off new (€21,950 new-price baseline from the TCO survey), consistent with the survey's note that e-208 holds value unusually well (~62% at 3yrs).
- **Renault Mégane E-Tech**: e.g. a 2022 EV60 220 (57,202km) listed at €15,990 (vs. ~€17,600 original) — steep discount for a mid-size EV, worth a closer look.
- **Renault Zoe** (older/smaller, budget end): **€9,500-19,500** depending on year/mileage; phase 2 (52kWh battery) 2020-22 cars run €14-19k. **Caveat:** some Zoes were sold with a battery-lease subscription rather than owned battery — verify this before valuing a listing, since a leased-battery car needs an extra monthly line-item and a battery-owned equivalent is worth €2-3k more.
- **Nissan Leaf**: **€11,500-22,500** for 2019-2024 cars; 40kWh (~220km real range) or 62kWh (~340km) packs. Passive (not liquid-cooled) battery thermal management — flagged risk for repeated DC fast-charging/highway use ("Rapidgate"), less of an issue for round-town driving.
- **Hyundai Kona Electric**: used examples from ~€13,000; a 2022 facelifted car with ~40,000km around €20,000 — well under the €35-36.9k new starting price in the TCO survey.
- **VW ID.3**: starting from ~€18,060 used (BYmyCAR listings).
- **BYD Atto 3**: **€24,990-36,990** used — not much room under new (€37,990-39,990), consistent with BYD being too new to France to show real depreciation yet (same point made about the Dolphin Surf in [02-model-tco-survey.md](02-model-tco-survey.md)).
- **Dacia Spring**: from ~€6,500 used — cheapest entry point by far, consistent with new-price being the lowest surveyed (~€16,900).

## What this changes for the frontier

- The Tesla pair (Model 3, Model Y) secondhand undercuts several *new* premium/mainstream cars on the price-range chart while likely beating them on range and charging speed — they need a place on the frontier even though neither is a new-car candidate.
- Budget-segment used cars (Zoe, Leaf, Dacia Spring) go well under €20k, undercutting even the cheapest *new* budget EVs — but carry real caveats (battery lease status, thermal management, older safety tech) that a range-only frontier would miss entirely.
- e-208 and Atto 3 barely discount off new — for these, buying new (with tax incentives factored in) may beat buying "used" that's really nearly-new-at-a-small-discount.

## Still needed

- Individual listing-level data (not just aggregate ranges) for the actual frontier — ideally scrape/sample 5-10 real listings per model at a target mileage band (e.g. ~40-60k km, 2-3 years old) rather than relying on aggregator summaries.
- Battery SOH (State of Health) figures where sellers disclose them — flagged as the single biggest resale-value driver in the TCO survey.
- Confirm Zoe/older-EV battery-lease-vs-owned status before treating any Zoe listing price as comparable to an owned-battery car.

**Caveat:** as with the other research files, these figures are aggregator/SEO summaries, not a raw pull from La Centrale/LeBonCoin/AutoScout24 — verify against live listings before treating any number here as a real quote.

Sources: [Tesla-Mag (Model 3 & Model Y used pricing)](https://www.tesla-mag.com/combien-coute-une-tesla-doccasion-prix-et-analyse-pour-la-model-3-et-la-model-y/) · [La Centrale (Model 3 occasion)](https://www.lacentrale.fr/occasion-voiture-modele-tesla-model+3.html) · [fplusd.org (Model 3 La Centrale price filters)](https://www.fplusd.org/tesla-model-3-la-centrale-32-48-000-euros-filtres/) · [La Centrale (Model Y occasion)](https://www.lacentrale.fr/voiture-occasion-tesla-model+y-model+y.html) · [L'Argus Occasion (Model Y)](https://occasion.largus.fr/auto/tesla/model-y/) · [CapCar (Tesla occasion guide)](https://www.capcar.fr/blog/tesla-occasion-quel-modele-choisir-et-a-quel-prix) · [AutoUncle (e-208 cote)](https://www.autouncle.fr/fr/voitures-occasion/Peugeot/e-208) · [Le Parking (Mégane E-Tech occasion)](https://www.leparking.fr/voiture-occasion/renault-megane-e-tech.html) · [Bayrou92 (Zoe occasion guide)](https://www.bayrou92.fr/autoombile/renault-zoe-occasion-92/) · [Bayrou92 (Leaf occasion guide)](https://www.bayrou92.fr/autoombile/nissan-leaf-occasion-92/) · [Automobile Propre (Kona Electric occasion)](https://www.automobile-propre.com/articles/hyundai-kona-electric-doccasion-a-partir-de-13-000-e-voici-tout-ce-quil-faut-savoir-avant-dacheter/) · [BYmyCAR (ID.3 occasion)](https://www.bymycar.fr/voiture-occasion/volkswagen/id-3) · [BYmyCAR (Atto 3 prix)](https://www.bymycar.fr/webzine/prix-du-byd-atto-3-neuf-et-occasion/) · [CapCar (top 10 EV occasion <15k)](https://www.capcar.fr/blog/top-10-des-voitures-electriques-doccasion-a-moins-de-15-000-euro) · [Caradisiac (marché occasion 2026)](https://www.caradisiac.com/vehicule-electrique-d-occasion-le-bon-calcul-en-2026-223343.htm)
