---
title: Transmitter
parent: Operations
nav_order: 1
---

# Transmitter

The **VFO Transmitter** is the best-developed operational tool in the Virtual Flight Online ecosystem. It allows pilots to send real-time aircraft position data to a server so flights can be tracked, shared, and displayed on a live radar.

## What it does

The Transmitter ecosystem makes it possible to:

- broadcast your aircraft position in real time
- fly with friends while seeing each other on a shared map
- support virtual ATC and organised group flights
- expose data feeds for other tools such as Little Navmap
- run a lightweight, community-focused tracking network without a database-heavy setup

## Main parts of the ecosystem

| Component | Purpose |
| --- | --- |
| [MSFS client](transmitter-msfs.md) | Windows client that reads simulator data through SimConnect |
| [X-Plane client](transmitter-xplane.md) | FlyWithLua-based script for X-Plane 11 and 12 |
| [Server](transmitter-server.md) | PHP/APCu server that receives telemetry and serves live views |
| [Live radar tools](live-radar.md) | Radar, status views, embeds, and compatible data feeds |

## Why VFO uses it

Many simulator tools are either too heavyweight for casual community use or are designed around a different style of flying. The VFO Transmitter gives the community a practical middle ground:

- simple enough for pilots to install and use
- flexible enough to support self-hosting
- rich enough to power radar, dashboards, and integrations

## Recommended reading order

1. Start with the client page for your simulator
2. Review the [live radar tools](live-radar.md) to understand what the data enables
3. If you want to host your own instance, continue to the [server guide](transmitter-server.md)
