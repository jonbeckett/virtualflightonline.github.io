---
title: LittleNavMap
parent: Guides
nav_order: 8
---

# LittleNavMap

LittleNavMap (LNM) is a free, open-source moving map application for flight simulation. It connects to your simulator to show your live position, lets you plan routes, and integrates with the VFO Transmitter to display online pilots.

Download it free at [littlenavmap.org](https://albar965.github.io/littlenavmap.html).

## Installing LittleNavMap

1. Download the latest release for your operating system from the website
2. Extract the zip to a folder of your choice — no installer is required
3. Launch `littlenavmap.exe`

On first launch, LNM will ask you to run the **Scenery Library Loader** to read your simulator's airport and navaid data. This takes a few minutes but only needs to be done once (and again after major simulator updates).

## Connecting to your simulator

LittleNavMap connects to your simulator through a small companion application called **Little Navconnect**.

### For MSFS

1. Launch **Little Navconnect** (included in the LNM download, in the `littlenavconnect` folder)
2. In LNM, go to **Tools → Connect** and select **Connect directly** if both applications are on the same PC, or enter the Navconnect IP if on a different machine
3. Start MSFS and load into an aircraft — your position will appear on the LNM map

### For X-Plane

1. In LNM, go to **Tools → Connect** and select **X-Plane** from the connection type
2. LNM connects directly via the X-Plane UDP interface — no separate application is needed

## Key features

### Moving map

The main map shows your live position, heading, and aircraft symbol updating in real time. You can choose from several map layers:

- **OpenStreetMap** — general map
- **OpenTopoMap** — terrain with contour lines
- **ESRI satellite** — photorealistic satellite imagery
- **IFR low/high charts** — styled navigation charts

### Route planning

To plan a route:

1. Right-click the departure airport on the map and choose **Set as Flight Plan Departure**
2. Right-click the destination airport and choose **Set as Flight Plan Destination**
3. LNM will calculate a direct route — you can add waypoints by right-clicking the route line and selecting **Add waypoint**
4. Export the route via **File → Export Flight Plan** in the format your simulator or FMS needs

LNM also imports SimBrief OFPs directly. Go to **File → Import Flight Plan → Import SimBrief OFP** and paste your SimBrief offer ID or import the downloaded file.

### Airport information

Click any airport to see:

- Runways, taxiways, and parking spots
- ILS and navaid frequencies
- ATIS and weather (if connected to the internet)
- Departure and approach procedures
- Fuel and services

### Search

Use **Search → Airport** or **Search → Navaid** to find specific airports and navaids by ICAO code, name, or region.

## VFO Transmitter integration

LNM can connect to the VFO Transmitter server to show online VFO pilots on your map.

1. Go to **Tools → Options → Online Flying**
2. Select **Custom** as the online service
3. Set **Status URL** and **Whazzup URL** both to `https://transmitter.virtualflight.online/ivao`
4. Set the format to **IVAO** and update interval to **5 seconds**
5. Click **OK** — VFO pilots who are transmitting will appear on your map as additional aircraft symbols

This is especially useful during group flights — you can see other members' positions even if your simulator does not show them directly.

## Practical tips

- Keep LNM open on a second monitor if you have one — having the moving map visible during flight significantly improves situational awareness
- Use the **Traffic Pattern** tool (right-click an airport → **Show Traffic Pattern**) to overlay the circuit on the map
- The **Hold** tool draws holding patterns at waypoints — useful if ATC puts you in a hold
- **Profile view** (toggle at the bottom of the map) shows a side-on elevation profile of your route including terrain clearance
