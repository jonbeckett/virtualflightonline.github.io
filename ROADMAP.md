# VFO Website Expansion Roadmap

A planning document for growing the VirtualFlight.Online GitHub Pages site beyond its current state.

---

## Current state

The site has four top-level sections:

| Section | Pages |
| --- | --- |
| About | 1 page |
| Community | 4 pages (index + Discord, Newsletter, Facebook) |
| Operations | 9 pages (index + Group Flights, Airline section with 8 children, Transmitter x4, Live Radar) |
| Resources | 4 pages (index + Liveries, Code of Conduct, Support) |

The foundations are in place. The gaps are: no beginner learning content, no in-depth guides for common sim tools, no event-specific content, and the Resources section is thin.

---

## Proposed expansions

### 1. New section — Guides

This would be the most impactful addition. A Guides section gives new members a path into flight simulation itself, not just VFO's specific tools. It positions the site as a genuine reference resource.

**Proposed structure:**

```
guides/
  index.md                  # Overview of the guides library
  getting-started-msfs.md   # Installing MSFS, first flight, key settings
  getting-started-xplane.md # Installing X-Plane, first flight, key settings
  vfr-basics.md             # Visual flight rules — chart reading, weather, altimetry
  ifr-basics.md             # Instrument flight — departures, airways, arrivals
  navigation.md             # VOR, NDB, GPS, FMS — how to navigate
  atc-communications.md     # ATIS, clearances, phraseology, talking to Vatsim/IVAO/MSFS AI
  simbrief.md               # Creating a flight plan — dispatch page, OFP, exporting
  littlenavmap.md           # Installing LNM, planning a flight, connecting to the simulator
  weather-planning.md       # Reading METARs/TAFs, SIGMETs, how to plan around weather
  checklists.md             # What checklists are, why to use them, how to build your own
```

**Why it matters:** Most community forums and Discord servers are reactive — someone asks a question and gets an answer. A written guide library is proactive, reduces repeated questions, and gives new members confidence before their first group flight.

---

### 2. Expand — Operations section

Several topics are referenced across the existing pages but never explained in full.

**Proposed additions:**

```
operations/
  virtual-atc.md          # What virtual ATC is, how VFO uses it, Discord voice procedures
  event-guide.md          # How VFO events are structured — briefings, timing, formation flying
  simbrief-dispatch.md    # Using SimBrief specifically in the context of VFO airline flights
  multi-crew.md           # Flying in formation or multi-crew — best practices, comms discipline
```

**SimBrief** is already referenced on the airline pages (send to ACARS, OFP) but there is no guide. A dedicated `simbrief-dispatch.md` under Operations (or under Guides) would fill that gap.

**Virtual ATC** comes up naturally during group flights. A page explaining what it is, how VFO handles voice comms, and what pilots should do makes the Discord voice channels less intimidating for newcomers.

---

### 3. Expand — Community section

The community section is accurate but minimal. Two additions would significantly improve it.

**Proposed additions:**

```
community/
  events.md        # How to find upcoming events, how to propose one, how to sign up
  forums.md        # Points to the Discord channels that act as async discussion spaces
```

An **events page** is particularly valuable. Even if the canonical event listing stays on Discord, a page that explains how events work, what to expect, and how to sign up gives casual visitors a clearer picture of the community.

---

### 4. Expand — Resources section

Currently Resources has three content pages. It should become a meaningful reference library.

**Proposed additions:**

```
resources/
  scenery.md              # Recommended freeware/payware scenery — airports, terrain, ortho
  aircraft.md             # Recommended aircraft add-ons by category and rank class
  peripherals.md          # Hardware guide — joysticks, yokes, rudder pedals, throttles, VR
  tools.md                # Useful third-party software — SimBrief, LNM, Navigraph, MSFS Addons Linker
  glossary.md             # Definitions of common terms — ICAO, PIREP, METAR, FBO, etc
  useful-links.md         # Curated external links — charts, weather, airline databases, etc
```

A **glossary** is especially useful for the airline section, where terms like PIREP, ACARS, OFP, and bid are used without explanation. A single reference page removes the need to explain each term on every page that uses it.

---

### 5. New section — Events (optional, higher effort)

If VFO stages events regularly, a dedicated Events section could record past events and list upcoming ones. This is higher effort because it requires ongoing maintenance — but it also makes the site feel alive.

```
events/
  index.md          # What VFO events are; links to upcoming and past
  upcoming.md       # Current / soon events (manually maintained)
  archive/
    2025.md         # Summary of events flown in 2025
    2024.md         # Summary of events flown in 2024
```

This is an optional addition and should only be pursued if someone is willing to keep it up to date.

---

### 6. Site-level improvements

Beyond content, several site-level improvements would enhance the experience.

**Navigation and branding:**
- Add a logo and favicon to `_config.yml` (VFO has existing branding)
- Consider a custom colour scheme matching VFO's colours rather than the default just-the-docs palette
- Review `aux_links` in `_config.yml` — quick links to the airline, Discord, and radar in the header would be useful

**Home page:**
- Embed the live transmitter radar (or a link to it) on the home page — the real site does this and it is immediately engaging
- Add a "What's on" callout pointing to the Discord events channel

**Search:**
- The default just-the-docs search is good — no changes needed unless the site grows very large

**Callouts:**
- The guides and operations pages would benefit from note/warning callouts for things like "power must be off before starting a flight in ACARS"
- Requires confirming `callouts` are configured in `_config.yml` first

---

## Priority order

Suggested order based on effort vs impact:

| Priority | Item | Effort | Impact |
| --- | --- | --- | --- |
| 1 | `guides/simbrief.md` | Low | High — referenced on 3 existing pages |
| 2 | `guides/littlenavmap.md` | Low | High — referenced on transmitter pages |
| 3 | `resources/glossary.md` | Low | High — many unexplained terms throughout site |
| 4 | `community/events.md` | Low | High — makes community more approachable |
| 5 | `resources/tools.md` | Low | Medium — useful reference |
| 6 | `guides/getting-started-msfs.md` | Medium | High — largest audience |
| 7 | `guides/atc-communications.md` | Medium | High — common newcomer question |
| 8 | `operations/virtual-atc.md` | Medium | Medium |
| 9 | `guides/vfr-basics.md` | Medium | Medium |
| 10 | `guides/ifr-basics.md` | High | Medium — narrower audience |
| 11 | `resources/aircraft.md` | Medium | Medium |
| 12 | `resources/scenery.md` | Medium | Medium |
| 13 | `events/` section | High | Medium — requires ongoing maintenance |

---

## Page count projection

| Section | Current pages | After expansion |
| --- | --- | --- |
| About | 1 | 1 |
| Community | 4 | 6 |
| Operations | 9 | 13 |
| Resources | 4 | 10 |
| Guides (new) | 0 | 11 |
| Events (optional) | 0 | 4 |
| **Total** | **18** | **45** |

---

## Notes

- All page content should be written in the VFO tone: friendly, accessible, practical, not overly technical
- Avoid linking to specific payware products without editorial reason — preference to freeware and widely-used tools
- The airline section is already detailed; guides should not duplicate it — cross-link instead
- Real-world accuracy matters for navigation and ATC content — flag with "for entertainment purposes only" per the VFO convention
