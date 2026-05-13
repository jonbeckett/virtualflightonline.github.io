---
title: Weather planning
parent: Guides
nav_order: 9
---

# Weather planning

Weather is one of the most significant variables in flight simulation. Understanding how to read weather reports and plan around them makes every flight more realistic and more satisfying.

{: .warning }
All content on this page is for entertainment purposes in flight simulation only and is not intended for real-world use.

## METAR

A METAR (Meteorological Aerodrome Report) is a standardised weather observation issued every 30 or 60 minutes for an airport. It is the primary tool for departure and arrival weather decisions.

### Reading a METAR

Example: `EGLL 121250Z 24015KT 9999 FEW025 SCT040 14/08 Q1012`

| Part | Meaning |
| --- | --- |
| `EGLL` | Airport ICAO code (London Heathrow) |
| `121250Z` | Day 12, time 12:50 UTC (Z = Zulu = UTC) |
| `24015KT` | Wind 240° at 15 knots |
| `9999` | Visibility 10 km or more |
| `FEW025` | Few clouds at 2,500 ft |
| `SCT040` | Scattered clouds at 4,000 ft |
| `14/08` | Temperature 14°C, dew point 8°C |
| `Q1012` | QNH 1012 hPa (set this on your altimeter) |

Wind gusts are shown as `24015G28KT` (gusting to 28 kt). Reduced visibility uses a number in metres: `0800` is 800 m visibility.

### Cloud cover codes

| Code | Meaning | Sky coverage |
| --- | --- | --- |
| SKC / CLR | Sky clear | 0/8 |
| FEW | Few | 1–2/8 |
| SCT | Scattered | 3–4/8 |
| BKN | Broken | 5–7/8 |
| OVC | Overcast | 8/8 |

BKN and OVC count as a cloud ceiling — VFR may not be possible if the ceiling is too low.

## TAF

A TAF (Terminal Aerodrome Forecast) is a weather forecast for an airport, typically covering 24 to 30 hours. TAFs use similar codes to METARs with additional markers for time-based changes:

| Code | Meaning |
| --- | --- |
| `BECMG` | Weather is expected to gradually change to the values that follow |
| `TEMPO` | Temporary conditions lasting less than one hour at a time |
| `FM` | From — a significant change at a specific time |
| `PROB30/40` | Probability of 30% or 40% that the conditions will occur |

Always check the TAF for your destination before departure on longer flights.

## SIGMETs and AIRMETs

**SIGMETs** (Significant Meteorological Information) warn of severe weather:

- Severe or extreme turbulence
- Severe icing
- Volcanic ash
- Tropical cyclones

**AIRMETs** cover less severe but still significant conditions affecting lower altitudes:

- Moderate icing
- Moderate turbulence
- Mountain obscuration

In simulation, SigMets are relevant if you fly real-world weather. LittleNavMap and SimBrief both pull real-world SigMet data.

## Wind and turbulence

### Wind at altitude

Upper winds are typically faster and from a different direction than surface winds. SimBrief calculates fuel and routing based on forecast upper winds — this is why the SimBrief OFP fuel figure can vary significantly from day to day on the same route.

Jet streams are high-altitude winds of 100–200 kt. Flying with a jet stream tailwind dramatically reduces flight time and fuel burn. Flying against one has the opposite effect.

### Turbulence

| Type | Cause |
| --- | --- |
| Mechanical turbulence | Wind flowing over rough terrain or buildings |
| Thermal turbulence | Uneven surface heating creating updrafts and downdrafts |
| Clear air turbulence (CAT) | Jet stream wind shear at high altitudes — no cloud, no warning |
| Wake turbulence | Vortices shed by large aircraft — especially dangerous on approach |

In simulation, turbulence is modelled by both MSFS and X-Plane when weather is enabled.

## Density altitude

At high temperatures or high elevations, air is less dense — this reduces engine performance and increases the runway length required for take-off. The **density altitude** is the pressure altitude corrected for temperature.

In simulation, this matters most at high-elevation airports (e.g. Lukla, Mexico City, Denver) or on hot summer days.

## Practical pre-flight weather check

1. Check the destination METAR — is visibility and ceiling acceptable?
2. Check the destination TAF — will it still be acceptable when you arrive?
3. Check the alternate airport weather — if the destination closes, where will you go?
4. Check SigMets along your route — any severe weather to avoid?
5. Check upper winds in SimBrief — how will they affect your fuel and routing?

Resources for checking weather:
- [NOAA Aviation Weather](https://aviationweather.gov) — METARs, TAFs, SigMets (real-world data)
- [SkyVector](https://skyvector.com) — charts with weather overlay
- SimBrief OFP — includes all weather data for your planned route automatically
