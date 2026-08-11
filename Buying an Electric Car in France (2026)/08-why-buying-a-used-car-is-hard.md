# Why it's hard to tell if a used car is a good deal

**Stub — this is the seed of what might eventually become its own CompareThe piece, not specific to EVs.** For now it lives alongside the electric-car research since that's where the problem showed up.

## The problem

A used-car ad gives you a spec string, a price, and a few photos. Working out whether that price is actually good requires things the ad never gives you:

- **Jargon decoding.** "534ch Performance, 79kWh" isn't self-explanatory — it takes knowing the model line to translate a marketing spec into an actual trim and battery pack. See the worked example in [07-reading-a-real-listing.md](07-reading-a-real-listing.md).
- **A fair-price benchmark.** Without knowing what comparable trims at comparable mileage/age actually sell for, "€34,990" is just a number. This project had to go build that benchmark itself — see [05-secondhand-price-bands.html](05-secondhand-price-bands.html) — before the listing in 07 could be judged at all.
- **Condition signals an ad doesn't surface.** Battery State of Health, accident/repair history, fast-charging habits — the single biggest driver of used-EV value (per [02-model-tco-survey.md](02-model-tco-survey.md)) isn't in the ad and usually isn't offered up by the seller.
- **Legal/market context specific to the country.** Whether a seller is a private individual or a professional changes the legal protection you get (France's *garantie légale de conformité* for professional sellers) — a fact that changes how much risk a given price represents, and one a buyer has to already know to even think to check.
- **Regional variation.** The same car can be a good deal in one region and an average one in another, for reasons that have nothing to do with the car itself.

## Why this isn't solved by just asking an AI

Worth naming directly, since it's part of the motivation: an AI assistant can decode the jargon and reason about what to check — that's genuinely useful and is most of what made the case study in 07 possible. But it doesn't have a fair-price benchmark sitting in its head, and it can't tell you the car's real condition from a photo. The benchmark had to be built — sourced, checked, corrected when wrong (see the trim-mismatch correction in [02-model-tco-survey.md](02-model-tco-survey.md)) — before "is this a good deal" had any real answer. That gap between general reasoning ability and grounded, sourced comparison data is exactly the space CompareThe is trying to fill.

## What a fuller version of this piece would need

- A worked-example library (more listings like 07, across more models/trims) rather than one data point.
- A clearer checklist format: what to ask/check before any used-car purchase, EV or not (Histovec, SOH tools, professional-vs-private-seller protections, regional pricing context).
- Whether "appreciation database" is even the right frame — probably closer to a living, sourced price-band dataset per model/trim, kept current, which is what [05-secondhand-price-bands.html](05-secondhand-price-bands.html) is a first sketch of.

Not written yet. Flagging it here so it's not lost, and so [07](07-reading-a-real-listing.md) has somewhere to point.
