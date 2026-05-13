---
title: Navigation
parent: Guides
nav_order: 5
---

# Navigation

Navigation in flight simulation mirrors real-world aviation navigation techniques. This guide covers the main systems — from traditional radio navaids to modern GPS and FMS.

> All content on this page is for entertainment purposes in flight simulation only and is not intended for real-world use.

## Dead reckoning

The most basic form of navigation. You track position using:

- **Heading** — the direction you are flying
- **Airspeed** — how fast you are moving
- **Time** — how long you have been flying

From these, you can estimate where you are. Dead reckoning is the foundation of all other navigation. Even with GPS, understanding it helps you catch errors.

## Pilotage

Navigating by reference to landmarks visible from the aircraft:

- Roads, rivers, railways, and coastlines
- Towns, cities, and distinctive terrain features
- Airfields (identified by their shape and runway markings)

Pilotage is the primary navigation method for VFR flying in good visibility.

## VOR (VHF Omnidirectional Range)

VOR stations transmit a signal that tells your receiver the **bearing** (called a radial) from the station to your aircraft.

### Flying to a VOR

1. Tune the VOR frequency on your NAV radio
2. Identify the station (listen for the Morse code ident or check the ATIS)
3. Rotate the **OBS** (Omni Bearing Selector) until the CDI needle centres with a **TO** flag
4. The OBS reading is the bearing you need to fly

### Flying from a VOR

Rotate the OBS until the CDI centres with a **FROM** flag. The OBS reading is the radial you are on — useful for position fixing.

### Intercepting a radial

1. Set the desired inbound track on the OBS
2. Turn to a heading that will intercept the radial (roughly 30–45° cut from the radial)
3. When the CDI begins to move, turn to the inbound heading
4. Fly with small corrections to keep the CDI centred

## NDB (Non-Directional Beacon) and ADF

NDB stations broadcast a signal in all directions. Your **ADF** (Automatic Direction Finder) receiver points an arrow toward the station.

To fly to an NDB: turn until the ADF needle points straight up (to the aircraft nose). Keep it there by making heading corrections. This is called "homing" and works but does not correct for wind drift well.

For accurate NDB tracking, use the **RMI** (Radio Magnetic Indicator) if available — it shows bearing to the station on the heading indicator.

## DME (Distance Measuring Equipment)

DME gives you slant-range distance to a navaid in nautical miles. Combined with a VOR bearing, two DME distances from different stations, or a DME arc approach, it provides accurate position fixing.

## GPS

GPS receivers show your position as latitude/longitude, and most have a moving map display. In simulation:

- Basic GPS units (Garmin GNS 430/530, G1000) are common in GA aircraft
- Enter a flight plan by selecting departure and destination, then intermediate waypoints
- The CDI on the GPS shows deviation from the planned track
- Follow the magenta line (or CDI) to stay on track

The GPS auto-sequences between waypoints. When you pass a waypoint, it automatically turns to the next leg.

## FMS (Flight Management System)

The FMS is a computerised navigation and performance management system found in airliners and business jets.

### Programming a route

1. Enter the departure and destination airports
2. Select a SID (departure procedure)
3. Enter airways and waypoints for the en-route section (or import from SimBrief)
4. Select a STAR (arrival procedure) and approach
5. Enter performance data: cost index, cruise altitude, fuel, weights

### Using the FMS in flight

- **LNAV** (Lateral Navigation) — autopilot follows the FMS route
- **VNAV** (Vertical Navigation) — autopilot manages altitude and descent profile per the FMS
- The FMS shows ETA, fuel remaining, and TOD (top of descent) point

SimBrief can export directly to many FMS formats — see the [SimBrief guide](simbrief.md).

## Practical tips

- Always cross-check GPS/FMS position with visual landmarks or radio navaids when possible
- Set up navaids (VOR, ILS) before you need them — not when you are already on the approach
- The moving map in LittleNavMap is invaluable for situational awareness — see the [LittleNavMap guide](littlenavmap.md)
- If you get lost, climb, confess, and comply — gain altitude for better radio reception, tell ATC you are unsure of position, and follow their instructions
