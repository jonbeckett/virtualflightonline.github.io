---
title: IFR basics
parent: Guides
nav_order: 4
---

# IFR basics

IFR stands for **Instrument Flight Rules** — flying by reference to instruments rather than external visual cues. IFR is used when flying in cloud, at night, or on long-haul routes where visual navigation is impractical. The VFO airline's scheduled routes are typically flown IFR.

> All content on this page is for entertainment purposes in flight simulation only and is not intended for real-world use.

## When IFR is used

- Flying in or above cloud
- Flying above the transition altitude (where altimeters are set to standard pressure)
- Commercial and airline operations
- Night flights where terrain clearance relies on navigation, not sight

## The IFR flight structure

A typical IFR flight follows a defined sequence:

### 1. Clearance

Before taxiing, you request an **IFR clearance** from Delivery or Ground. The clearance tells you:

- The route you are cleared on (or an abbreviated version — "as filed")
- Your initial altitude
- Your departure procedure
- The squawk code for your transponder

A clearance response sounds like:

> *"[Callsign], cleared to [destination] via [SID / as filed], climb to [altitude], squawk [code]."*

### 2. Departure — SID

A **SID** (Standard Instrument Departure) is a published route from the runway to the first en-route waypoint. It is shown on departure charts and is programmed into your FMS or GPS before departure.

Follow the altitude restrictions and turn points on the SID exactly — ATC expects you to fly it precisely.

### 3. En route

Once clear of the departure procedure, you follow airways — named routes between navaid waypoints. Airways have minimum altitudes for terrain clearance and are shown on IFR en-route charts.

At each waypoint, your FMS (if equipped) sequences automatically. Simpler aircraft use the OBS on the VOR receiver to track from one navaid to the next.

### 4. Arrival — STAR

A **STAR** (Standard Terminal Arrival Route) transitions you from the en-route structure to the approach phase. It is the mirror image of the SID — a published route from the last en-route waypoint to the initial approach fix (IAF).

### 5. Approach

The approach takes you from the IAF to the runway. Common approach types:

| Type | How it works |
| --- | --- |
| **ILS** (Instrument Landing System) | Radio beams guide you precisely to the runway — most common at major airports |
| **RNAV/GPS** | Satellite-based precision approach — increasingly common |
| **VOR** | Non-precision approach using a VOR station — no vertical guidance |
| **NDB** | Older non-precision approach using a radio beacon |

The approach chart shows all the altitudes, headings, and decision points you need.

### 6. Missed approach

If you reach the **Decision Altitude (DA)** or **Minimum Descent Altitude (MDA)** and cannot see the runway, you execute a **missed approach** — a published go-around procedure that takes you safely away from the terrain and back into the circuit.

## Key instruments

| Instrument | What it shows |
| --- | --- |
| Attitude Indicator (AI) | Pitch and bank — the most important instrument in IMC |
| Altimeter | Altitude by pressure |
| Airspeed Indicator | Current airspeed |
| Vertical Speed Indicator (VSI) | Rate of climb or descent |
| Heading Indicator (HI) / HSI | Magnetic heading |
| VOR/ILS receiver | Bearing to a navaid, or localiser/glideslope for ILS |
| DME | Distance to a navaid |

## Practical tips for simulation

- Always file a flight plan with SimBrief or the in-sim planner before an IFR flight — see the [SimBrief guide](simbrief.md)
- Program your FMS before engine start, not while taxiing
- Fly the altitude restrictions on SIDs and STARs — ATC (or the sim) will often catch violations
- Brief the approach before starting the descent — know the DA/MDA and missed approach before you need them

## Next steps

- [Navigation](navigation.md) — VOR, NDB, GPS, and FMS in detail
- [SimBrief](simbrief.md) — planning your IFR flight plan and obtaining an OFP
- [ATC communications](atc-communications.md) — phraseology for IFR clearances and position reports
