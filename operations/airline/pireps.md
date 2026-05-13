---
title: PIREPs
parent: Airline
nav_order: 6
---

# PIREPs

A PIREP (Pilot Report) is the record of a completed flight. There are two ways to file one: automatically through ACARS, or manually using the manual PIREP form.

## Filing with ACARS

When you complete a flight using ACARS and click **Submit**, the PIREP is filed automatically. The accuracy of the PIREP depends on the data you entered into ACARS before the flight.

For the PIREP to be matched correctly against a scheduled or tour flight, the following fields must be accurate:

| Field | Format |
| --- | --- |
| Airline | Must match the airline in the flight database |
| Flight number | Integer only — no prefixes or punctuation (e.g. `1234`) |
| Flight or tour code | Alphanumeric only (e.g. `TUK`) |
| Leg number | Integer only (e.g. `1`) |

For free flights and scheduled flights, the code and leg fields can be left blank.

If you sent the flight to ACARS from the airline website, these fields are pre-populated automatically.

## Filing manually

If ACARS fails or a flight cannot be submitted normally, you can file a manual PIREP at [airline.virtualflight.online/pireps/create](https://airline.virtualflight.online/pireps/create).

Note: pilot pay is reduced by **50%** for manually filed PIREPs.

The same field accuracy rules apply — make sure airline, flight number, code, and leg match the flight in the database.

## Simbrief integration

If you use the Simbrief integration when sending a flight from the airline website, the planned and actual routes will both be visible when reviewing the PIREP later. Manually entered routing information will not produce the same result.

## Tour progress

Tour leg PIREPs must have the correct airline, flight number, code, and leg number for the tour leg to be marked as complete (green tick) in the airline. Filing with incorrect details means the leg will not be ticked off, even if the PIREP is accepted.
