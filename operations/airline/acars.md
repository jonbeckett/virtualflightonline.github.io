---
title: ACARS
parent: Airline
nav_order: 2
---

# ACARS

ACARS (Aircraft Communications Addressing and Reporting System) is a software application you run alongside your flight simulator. It tracks your flight in real time and files your pilot report automatically on landing.

## Installing ACARS

### Download and install

1. Download the phpVMS ACARS client: [bit.ly/phpvms-acars](https://bit.ly/phpvms-acars)
2. ACARS does not have an installer — extract it and run it from wherever you like
3. ACARS requires **.NET 6** — it will prompt you to install it if needed

### Create a profile

On first launch, ACARS will ask for a phpVMS URL and API key:

- **URL:** `https://airline.virtualflight.online`
- **API key:** find this on your [profile page](https://airline.virtualflight.online/profile) (click the eye icon next to "API Key")

To update these later, click the pencil icon next to the profile name in ACARS.

### Add the fsuipc-lvar-module (MSFS only)

For ACARS to work correctly with Microsoft Flight Simulator, you need the fsuipc-lvar-module in your Community folder:

1. Download from [fsuipc.com/download/fsuipc-lvar-module.zip](https://www.fsuipc.com/download/fsuipc-lvar-module.zip)
2. Extract the zip — you will get a folder called `fsuipc-lvar-module`
3. Move the `fsuipc-lvar-module` folder into your MSFS Community folder

Note: you do not need to run FSUIPC itself — only the LVAR module is required.

## Using ACARS

The left margin of ACARS contains the following icons:

| Icon | Purpose |
| --- | --- |
| Dashboard | Current location, total flights, flight time, NOTAMs |
| New Flight | Configure flight details, start and finish flights |
| Flight Search | Search scheduled flights or load bids |
| Briefing | Read the OFP for the current flight plan |
| Map | Flight plan route, current position, and past track |
| Start Flight | Quick start/stop button |

## Starting a flight

Before starting a flight in ACARS, make sure:

- The aircraft is on the ground at the departure airport with power **off**
- The correct airline, flight number, code, and leg are filled in
- Departure, arrival, and aircraft are set
- Passengers and payload are populated

Click **Start Flight** when everything is ready, then proceed with your normal startup.

## Ending a flight

1. Land, taxi to a parking stand, and shut down the aircraft
2. In ACARS, click **End Flight**
3. Review the summary, then click **Submit** to file the PIREP

## Choosing flights

You can start a flight in several ways:

- **Free flight:** enter details directly into ACARS (use flight numbers below 1000)
- **Website:** find a flight on the [Flights](https://airline.virtualflight.online/flights) or [Tours](https://airline.virtualflight.online/dtours) page and click "Send to ACARS" (ACARS must not already be running)
- **Bid:** bid on a flight in the website; ACARS will load it automatically on launch
- **ACARS search:** search flights directly in the ACARS Search page by departure/arrival ICAO

## Filing manually if something goes wrong

If ACARS fails to file your flight, you can submit a manual PIREP — but pilot pay is reduced by 50%. File at [airline.virtualflight.online/pireps/create](https://airline.virtualflight.online/pireps/create).

## Other simulators

### FSX and Prepar3D

Install [FSUIPC](http://www.fsuipc.com/) (free version is sufficient) and [MakeRwys](http://fsuipc.simflight.com/beta/MakeRwys.zip), then run MakeRwys. Re-run MakeRwys after any scenery changes.

### X-Plane

Inside the ACARS download there is an `X-Plane` folder. Copy the `AcarsConnect` folder from it into your X-Plane `resources/plugins/` directory.
