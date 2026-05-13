---
title: ATC communications
parent: Guides
nav_order: 6
---

# ATC communications

Clear radio communication with Air Traffic Control is a core skill in flight simulation, especially during VFO group flights where voice coordination with other pilots matters. This guide covers standard phraseology and how radio communication works in practice.

{: .warning }
All content on this page is for entertainment purposes in flight simulation only and is not intended for real-world use.

## The basic formula

Every radio call follows the same structure:

> **Who you are calling → Who you are → Where you are → What you want**

Example:
> *"Manchester Ground, Speedbird 123, stand 14, requesting push and start."*

Once established with a frequency, you can drop the station name from your calls.

## The phonetic alphabet

Use the NATO phonetic alphabet to spell callsigns, waypoints, and runway designators:

| Letter | Word | Letter | Word |
| --- | --- | --- | --- |
| A | Alpha | N | November |
| B | Bravo | O | Oscar |
| C | Charlie | P | Papa |
| D | Delta | Q | Quebec |
| E | Echo | R | Romeo |
| F | Foxtrot | S | Sierra |
| G | Golf | T | Tango |
| H | Hotel | U | Uniform |
| I | India | V | Victor |
| J | Juliet | W | Whiskey |
| K | Kilo | X | X-ray |
| L | Lima | Y | Yankee |
| M | Mike | Z | Zulu |

Numbers are spoken digit by digit. Altitudes, headings, and frequencies use standard spoken form: 7,500 ft is *"seven thousand five hundred"*, runway 27L is *"runway two seven left"*.

## Standard calls — IFR departure

| Phase | Example call |
| --- | --- |
| ATIS | (Listen first — note the ATIS letter, e.g. "Information Bravo") |
| Delivery | *"[Airport] Delivery, [callsign], [aircraft type], stand [X], IFR to [destination], Information [ATIS letter]."* |
| Ground (push/start) | *"[Airport] Ground, [callsign], stand [X], request push and start."* |
| Ground (taxi) | *"[Airport] Ground, [callsign], ready to taxi, runway [X]."* |
| Tower (line-up) | *"[Airport] Tower, [callsign], holding short runway [X], ready."* |
| Tower (airborne) | *(Tower will hand you off to Departure — acknowledge and switch)* |

## Standard calls — VFR arrival

| Phase | Example call |
| --- | --- |
| Approach/Info | *"[Airport] Information, [callsign], [aircraft type], [position], [altitude], [intentions]."* |
| Tower | *"[Airport] Tower, [callsign], [position], [altitude], request landing runway [X]."* |
| Downwind | *"[Callsign], downwind, runway [X]."* |
| Final | *"[Callsign], final, runway [X]."* |

## Acknowledging instructions

Always **read back** altitude, heading, speed, and runway instructions:

- ATC: *"Speedbird 123, climb to flight level 250."*
- You: *"Climb flight level 250, Speedbird 123."*

A readback confirms you heard the instruction correctly. If you are unsure, ask:
> *"Say again, [callsign]."*

Or if you cannot comply:
> *"Unable, [callsign]."* — and then state what you can do.

## Squawk codes

ATC assigns a four-digit transponder code (**squawk**). Set it in your transponder before departure. Special codes:

| Code | Meaning |
| --- | --- |
| 7500 | Hijack |
| 7600 | Radio failure |
| 7700 | Emergency |
| 2000 | Entering controlled airspace without a clearance (unintentional) |
| 1200 | VFR (US default) |

In simulation, squawk 2000 unless ATC assigns you a code.

## VFO group flight comms

During VFO group flights, comms are typically handled over Discord voice rather than simulated ATC. Practical tips:

- **Use push to talk** — background noise is disruptive in voice channels
- **Keep calls brief** — state your position and what you intend to do
- **Acknowledge other pilots** — especially if they are calling a go-around or missed approach
- **Set your nickname** to your callsign so others know who is speaking

For more on how VFO handles voice coordination, see [Virtual ATC](../operations/virtual-atc.md).
