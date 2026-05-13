---
title: Transmitter for X-Plane
parent: Operations
nav_order: 3
---

# Transmitter for X-Plane

The X-Plane version of the VFO Transmitter is a **FlyWithLua** script for **X-Plane 11** and **X-Plane 12**. It sends real-time aircraft telemetry to a transmitter server so X-Plane pilots can take part in the same shared tracking environment.

## Why it matters

X-Plane pilots often want a clearer view of where other human pilots are flying, especially during shared flights or informal ATC sessions. The VFO Transmitter helps bridge that gap by sending aircraft data to a central server that can then power radar and compatible data feeds.

## Highlights

- real-time position transmission
- persistent configuration between sessions
- optional auto-connect at startup
- text-to-speech connection feedback
- automatic reconnection handling
- Little Navmap compatibility through IVAO-style feeds

## Typical setup

1. Install **FlyWithLua**
2. Copy the transmitter script into the FlyWithLua `Scripts` folder
3. Reload Lua scripts or restart X-Plane
4. Open the Transmitter XP window from the plugin menus
5. Configure the server URL, callsign, pilot name, and group
6. Connect and begin transmitting

## Best fit

This client is ideal for:

- shared VFO group flights in X-Plane
- community fly-ins where live situational awareness matters
- users who want to feed Little Navmap or the VFO radar from X-Plane

## Good details to capture in future revisions

As the migration continues, this page is a natural place to expand with:

- illustrated installation steps
- example server URLs
- configuration screenshots
- troubleshooting for FlyWithLua and LuaSocket

## Related pages

- [Transmitter overview](transmitter.md)
- [Self-hosted server guide](transmitter-server.md)
- [Live radar and status tools](live-radar.md)
