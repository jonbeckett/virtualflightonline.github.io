---
title: Live radar and status tools
parent: Operations
nav_order: 7
---

# Live radar and status tools

The VFO Transmitter server provides two live views and a LittleNavMap integration so you can see online pilots in real time.

## Status page

**<https://transmitter.virtualflight.online/status>**

A sortable table showing all currently online pilots. Updates automatically every 30 seconds. Click a callsign to zoom the radar to that aircraft.

## Radar display

**<https://transmitter.virtualflight.online/radar>**

An interactive map showing live aircraft positions. Updates every 5 seconds with smooth movement between position reports.

Features:

- multiple map layers to choose from
- aircraft list with group filtering
- measurement tools
- fullscreen mode
- URL-based tracking of a specific callsign or group

## LittleNavMap integration

You can connect LittleNavMap to the VFO server to see online VFO pilots on your chart.

1. In LittleNavMap, open **Tools → Options** and go to the **Online Flying** tab
2. Select **Custom** as the online service
3. Set the **Status URL** to `https://transmitter.virtualflight.online/ivao`
4. Set the **Whazzup URL** to `https://transmitter.virtualflight.online/ivao`
5. Set the format to **IVAO** and the update interval to **5 seconds**
6. Click **OK** — online VFO pilots will now appear on your chart
