---
title: Transmitter for MSFS
parent: Operations
nav_order: 4
---

# Transmitter for MSFS

The MSFS client is a small Windows application that reads your aircraft position through **SimConnect** and sends it to the VFO Transmitter server.

## Requirements

- Microsoft Windows
- .NET Framework 4.7.2 or newer
- Microsoft Flight Simulator 2020 or 2024

## Installation

1. Download the latest release from [GitHub](https://github.com/jonbeckett/vfo-transmitter-client-msfs/releases/)
2. Run the installer and follow the prompts
3. The client will appear in the Start Menu as **VFO Transmitter**

## Setup

1. Launch **VFO Transmitter** from the Start Menu
2. Enter your **callsign**, **pilot name**, and **group** (for VFO flights, use `VFO` as the group)
3. The server URL is pre-configured to use the VFO hosted server — you do not need to change it
4. Start Microsoft Flight Simulator and load into an aircraft
5. Click **Connect** in the VFO Transmitter client
6. The status indicator will show that you are transmitting

## Checking it is working

Once connected, open the [live radar](live-radar.md) in your browser. Your callsign should appear on the map within a few seconds.

## Troubleshooting

- If the client will not connect, make sure MSFS is fully loaded into the simulator (not just the main menu)
- If your position does not appear on the radar, check that the server URL is set to `https://transmitter.virtualflight.online`
- Restart the client after a simulator crash or reload
