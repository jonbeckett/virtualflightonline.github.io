---
title: Transmitter
parent: Operations
nav_order: 3
---

# Transmitter

The **VFO Transmitter** is a live tracking system that lets sim pilots broadcast their aircraft position to a shared server. Other pilots, spectators, and tools can then see the live air picture on the VFO radar.

## Why it exists

Microsoft Flight Simulator and X-Plane do not expose user positions to external tracking tools out of the box. The VFO Transmitter fills that gap with a lightweight client/server system built specifically for community flying.

## How it works

1. You install a small client for your simulator
2. The client reads your aircraft position from the simulator in real time
3. Position data is sent to the VFO Transmitter server
4. The server powers the live radar, status dashboard, and data feeds

## Ecosystem overview

| Component | Purpose |
| --- | --- |
| [MSFS client](transmitter-msfs.md) | Windows app for Microsoft Flight Simulator (SimConnect) |
| [X-Plane client](transmitter-xplane.md) | FlyWithLua script for X-Plane 11 and 12 |
| [Server](transmitter-server.md) | PHP/APCu server that receives and serves live data |
| [Live radar tools](live-radar.md) | Radar map, status table, and LittleNavMap integration |

The VFO community uses a shared hosted server, so most pilots only need to install the client for their simulator.
