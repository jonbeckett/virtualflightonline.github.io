---
title: Getting started with X-Plane
parent: Guides
nav_order: 2
---

# Getting started with X-Plane

X-Plane 11 and X-Plane 12 are fully supported in the VFO community. X-Plane is known for its realistic flight model and strong support for third-party aircraft and plugins.

## Getting the simulator

X-Plane 12 is the current release. It is available from:

- **Laminar Research** directly at [x-plane.com](https://www.x-plane.com)
- **Steam**

X-Plane 11 is still widely used and fully supported for VFO flights, though X-Plane 12 is recommended for new installs.

## System requirements

X-Plane 12 recommended specs:

| Component | Recommended |
| --- | --- |
| CPU | Intel Core i5-8600K / AMD Ryzen 5 3600 or better |
| RAM | 16 GB (32 GB recommended) |
| GPU | NVIDIA GTX 1070 / AMD RX 5700 or better (8 GB VRAM) |
| Storage | SSD strongly recommended |

## Initial setup

### Installing scenery

X-Plane ships with global scenery, but coverage varies. You can improve scenery quality by installing:

- **Ortho4XP** or similar orthophoto tools for photorealistic ground textures
- **Airport scenery** from X-Plane.org — many freeware airport packages are available

### Control bindings

1. Go to **Settings → Joystick**
2. Select your device
3. Assign axes for pitch, roll, yaw, and throttle on the **Axis** tab
4. Assign buttons for brakes, flaps, and other functions on the **Buttons: Basic** tab

### Plugins

X-Plane's plugin system is a major strength. Key plugins for VFO flying:

- **FlyWithLua NG** — required for the [VFO Transmitter](../operations/transmitter-xplane.md) (X-Plane client)
- **BetterPushback** — tug-based pushback for added realism
- **AutoGate** — animated jetways at supported airports

Install plugins by copying their folder into `X-Plane/Resources/plugins/`.

## Your first flight

1. From the main menu, choose **New Flight**
2. Select a small GA airport — somewhere with a visible runway and clear surroundings
3. Choose a **Cessna 172** (included with X-Plane)
4. Set weather to **Clear skies**, time of day to daytime
5. Click **Start Flight**

X-Plane starts with the aircraft loaded and engines running by default. You can change this in the flight configuration to start cold and dark if you prefer.

When ready to depart, apply throttle slowly, keep straight with rudder input, and rotate at around 65 knots.

## Key differences from MSFS

If you have come from Microsoft Flight Simulator, a few things work differently in X-Plane:

| Feature | MSFS | X-Plane |
| --- | --- | --- |
| Flight model | Based on lookup tables | Blade element theory (very realistic) |
| Default scenery | Photorealistic global coverage | Vector-based, varies by region |
| Aircraft library | Large default + Marketplace | Smaller default, strong freeware scene |
| ATC | Built-in AI ATC | Built-in AI ATC + third-party options |
| Weather | Real-world weather injection | Real-world weather (XP12 improved) |

## Next steps

- Install the [VFO Transmitter for X-Plane](../operations/transmitter-xplane.md) to appear on the live radar during group flights
- Read [VFR basics](vfr-basics.md) to understand the rules of visual flying
- Join the [Discord server](../community/discord.md) — there is a dedicated X-Plane channel
