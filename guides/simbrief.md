---
title: SimBrief
parent: Guides
nav_order: 7
---

# SimBrief

SimBrief is a free online flight dispatch tool used by virtual and real-world pilots to generate professional Operational Flight Plans (OFPs). It integrates with the VFO airline and with most major FMS add-ons.

## Creating a free account

Register at [simbrief.com](https://www.simbrief.com). A free account gives you full access to all dispatch features.

## Your first flight plan

### Setting up your airline profile

Before your first dispatch:

1. Log in and go to **Dispatch → Pilot Profile**
2. Enter your pilot ID (your VFO airline number in the format `VFA0123` if using for airline flights)
3. Add your preferred aircraft if you fly the same type regularly

### Creating a flight plan

1. Go to **Dispatch → New Flight**
2. Fill in the main fields:
   - **Origin** — departure airport ICAO code (e.g. `EGLL`)
   - **Destination** — arrival airport ICAO code (e.g. `EDDF`)
   - **Aircraft type** — select from the list or type your ICAO aircraft type code
   - **Cruise altitude** — leave as "AUTO" to let SimBrief calculate the optimum FL
   - **Route** — leave blank to auto-generate, or paste in a preferred route
3. Click **Generate OFP**

SimBrief will calculate the route, fuel, wind data, and performance figures, then produce the OFP.

### Reading the OFP

The Operational Flight Plan is a long document — here are the key sections:

| Section | What it contains |
| --- | --- |
| Header | Flight number, origin/destination, aircraft, times |
| Route | Full ICAO route string — waypoints, airways, SID/STAR |
| Fuel | Planned fuel, reserves, alternates |
| Weather | METAR and TAF for departure, destination, and alternate |
| NOTAM summary | Active notices at the airports on your route |
| Weight and balance | ZFW, TOW, landing weight estimates |
| Wind/altitude chart | Forecast winds at cruise altitude for each waypoint |

You do not need to read every section before every flight. At minimum, check: the route, the fuel figures, and the destination weather.

### Exporting to your simulator

SimBrief can export flight plans in many formats:

| Export | How to use |
| --- | --- |
| **MSFS .PLN** | Download and place in `Documents\Microsoft Flight Simulator\Plans` — load from the World Map |
| **X-Plane FMS** | Download and place in `X-Plane\Output\FMS Plans` — load from the GPS or FMS |
| **Send to ACARS** | From the VFO airline website, click **Send to ACARS** next to a flight — SimBrief is integrated |
| **Garmin G1000/530** | Export in the appropriate format for your add-on |

### Integration with the VFO airline

When you open a flight on the [VFO airline website](https://airline.virtualflight.online) and click the Simbrief button, it pre-fills your aircraft and route. The resulting OFP links to your PIREP, which means both the planned and actual routes are visible when you review your flight after landing.

This is the recommended workflow for airline flights — it produces the best PIREP detail.

## Practical tips

- Use the **Alias** field to set a custom callsign so your radio comms match your OFP
- SimBrief uses real-world weather data — if you are flying in real-weather mode in your simulator, the OFP winds will be accurate
- Save your OFP as PDF before the flight — useful if something goes wrong mid-flight and you need to refer to the alternates or fuel reserves
- The **NavLog** section of the OFP lists every waypoint with estimated times and fuel — useful for cross-checking your FMS

## Related pages

- [IFR basics](ifr-basics.md) — understanding the flight plan structure SimBrief produces
- [LittleNavMap](littlenavmap.md) — viewing your SimBrief route on a moving map
- [ACARS](../operations/airline/acars.md) — sending SimBrief plans to ACARS for VFO airline flights
