---
title: Transmitter for MSFS
parent: Operations
nav_order: 2
---

# Transmitter for MSFS

The Microsoft Flight Simulator client is a lightweight Windows application that reads live aircraft data through **SimConnect** and sends regular updates to a compatible VFO Transmitter endpoint.

## What it is good for

- sharing your position during community flights
- feeding live radar and status pages
- keeping setup straightforward for Microsoft Flight Simulator pilots

## Core workflow

1. Launch the client while MSFS is running
2. Enter your callsign, pilot name, and group name
3. Select the correct transmitter server URL
4. Connect and allow the app to send live updates

## Information it can transmit

The client is designed to send a practical operating snapshot, including:

- aircraft type
- latitude and longitude
- altitude
- heading
- airspeed and groundspeed
- touchdown velocity
- transponder code
- pilot and group details
- optional notes

## Requirements

- Microsoft Windows
- .NET Framework 4.7.2
- Microsoft Flight Simulator with SimConnect available

## Notes for VFO members

This client is a good fit if you want the simplest path into the Transmitter ecosystem from MSFS. It focuses on dependable, low-friction position sharing rather than a large feature set in the client itself.

## Troubleshooting themes

The related project notes a few common issues worth checking first:

- confirm MSFS and SimConnect are both available
- verify the configured server URL is correct
- check the app status text if transmissions fail
- reconnect after simulator restarts or temporary network interruptions

## Next page

Once the client is connected, the most useful follow-up is the [Live radar and status tools](live-radar.md) page so you can see how the shared data is presented.
