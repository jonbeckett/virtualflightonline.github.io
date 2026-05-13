---
title: Transmitter for X-Plane
parent: Operations
nav_order: 5
---

# Transmitter for X-Plane

The X-Plane version of the VFO Transmitter is a **FlyWithLua** script for **X-Plane 11** and **X-Plane 12**. It sends your aircraft position to the VFO Transmitter server in real time.

## Requirements

- X-Plane 11 or X-Plane 12
- FlyWithLua NG plugin

## Step 1 — Install FlyWithLua

If you do not already have FlyWithLua installed:

1. Download **FlyWithLua NG** from the [X-Plane.org forums](https://forums.x-plane.org/index.php?/files/file/38445-flywithlua-ng-next-generation-edition-for-x-plane-11-win-lin-mac/)
2. Extract the download and copy the `FlyWithLua` folder into your X-Plane `Resources/plugins/` directory
3. Restart X-Plane to confirm the plugin is loaded (it will appear in the Plugins menu)

## Step 2 — Install the transmitter script

1. Download the latest transmitter script from [GitHub](https://github.com/jonbeckett/virtualflightonlinetransmitter/releases/tag/Transmitter)
2. Copy `transmitter_xp.lua` into your `Resources/plugins/FlyWithLua/Scripts/` folder
3. In X-Plane, go to **Plugins → FlyWithLua → Reload all Lua scripts** (or restart X-Plane)

## Step 3 — Configure and connect

1. Open the Transmitter XP window from **Plugins → FlyWithLua → FlyWithLua Macros**
2. Enter your **callsign**, **pilot name**, **group** (use `VFO` for VFO community flights), and the server URL `https://transmitter.virtualflight.online`
3. Click **Connect**
4. Your position will now appear on the [live radar](live-radar.md)

## Troubleshooting

- If the script does not appear in the Macros menu, confirm `transmitter_xp.lua` is in the correct `Scripts/` folder and that FlyWithLua loaded without errors
- LuaSocket must be available — it is included with FlyWithLua NG
