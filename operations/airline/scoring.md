---
title: Scoring
parent: Airline
nav_order: 5
---

# Scoring

Every flight starts with a score of **100 points**. Penalties are deducted for rule violations detected by ACARS during the flight. Scoring is intended to help you identify areas for improvement — PIREPs are not rejected purely on the basis of a low score.

## Scoring rules

| Rule | Penalty |
| --- | --- |
| Taxi speed exceeds 30 knots | 5 points |
| G-force exceeds 2G | 5 points |
| Refuelling while airborne | 10 points |
| Overspeed warning triggered | 2 points |
| Bank angle exceeds 60° | 2 points |
| Pitch angle exceeds 30° | 2 points |
| Runway or taxiway overrun | 10 points |
| Simulation rate manipulated | 2 points |
| Slew mode activated | 2 points |
| IAS exceeds 250 knots below 10,000 ft | 2 points |
| Unstabilised approach below 1,500 ft AGL (gear/flaps not set) | 5 points |
| Stall warning triggered | 5 points |
| Thrust reversers used below 60 knots | 2 points |
| Hard landing (above 500 ft/min) | 20 points — aircraft grounded for checks |
| Soft landing (below 50 ft/min) | 0 points — aircraft grounded for checks |
| Tail strike (pitch >15° on landing) | 0 points — aircraft grounded for checks |
| Wing strike (roll >10° on runway) | 0 points — aircraft grounded for checks |

Most rules have a 10–30 second reaction window before the penalty is applied, and a 60 second cooldown before the rule can trigger again. Light violations (beacon, strobe, landing lights) do not incur points due to MSFS aircraft inconsistencies.

## General guidance

- Maximum taxi speed: **30 kts**
- Maximum roll: **60°**
- Maximum pitch: **30°**
- Maximum G-force: **3 m/s²**
- Maximum speed below 10,000 ft: **250 kts**
- Hard landing threshold: **500 ft/min**
- Thrust reversers: off below **60 kts** after landing

## Lights guidance

| Phase | Beacon | Strobes | Landing lights | Taxi lights |
| --- | --- | --- | --- | --- |
| Apron / taxi out | On (engines running) | Off (on at runway crossings) | Off | Pilot's discretion |
| Take-off and departure | On | On | On (off above 10,000 ft) | On (off after take-off) |
| Cruise | On | On | Off | Off |
| Descent and landing | On | On (off leaving runway) | On below 10,000 ft, on below 1,500 ft | On after gear down |
| Apron / taxi in | On until engines off | Off (on at runway crossings) | Off | Pilot's discretion |

Navigation lights should be on whenever the crew is in the cockpit and the aircraft has electrical power.
