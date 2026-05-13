# Current Navigation Structure

> Always read the actual front matter of sibling files before assigning a `nav_order` — this table may be out of date.

## Top-level pages (project root)

| File | Title | nav_order |
| --- | --- | --- |
| `index.md` | Welcome | 1 |
| `about.md` | About Virtual Flight Online | 2 |
| `community/index.md` | Community | 3 |
| `operations/index.md` | Operations | 4 |
| `resources/index.md` | Resources | 5 |
| `guides/index.md` | Guides | 6 |
| `events/index.md` | Events | 7 |

## Community section (`community/`)

| File | Title | nav_order |
| --- | --- | --- |
| `community/discord.md` | Discord | 1 |
| `community/newsletter.md` | Newsletter | 2 |
| `community/facebook.md` | Facebook group | 3 |
| `community/events.md` | Events | 4 |
| `community/forums.md` | Forums and discussion | 5 |

## Operations section (`operations/`)

| File | Title | nav_order |
| --- | --- | --- |
| `operations/group-flights.md` | Group flights | 1 |
| `operations/airline/index.md` | Airline | 2 |
| `operations/transmitter.md` | Transmitter | 3 |
| `operations/transmitter-msfs.md` | Transmitter for MSFS | 4 |
| `operations/transmitter-xplane.md` | Transmitter for X-Plane | 5 |
| `operations/transmitter-server.md` | Self-hosted server | 6 |
| `operations/live-radar.md` | Live radar and status tools | 7 |
| `operations/virtual-atc.md` | Virtual ATC | 8 |
| `operations/event-guide.md` | Event guide | 9 |
| `operations/multi-crew.md` | Multi-crew flying | 10 |

## Airline section (`operations/airline/`)

| File | Title | nav_order |
| --- | --- | --- |
| `operations/airline/beginners-guide.md` | Beginners guide | 1 |
| `operations/airline/acars.md` | ACARS | 2 |
| `operations/airline/flights.md` | Flights | 3 |
| `operations/airline/ranks.md` | Ranks | 4 |
| `operations/airline/scoring.md` | Scoring | 5 |
| `operations/airline/pireps.md` | PIREPs | 6 |
| `operations/airline/fleet.md` | Fleet | 7 |
| `operations/airline/tours.md` | Tours | 8 |

## Resources section (`resources/`)

| File | Title | nav_order |
| --- | --- | --- |
| `resources/liveries.md` | Liveries | 1 |
| `resources/code-of-conduct.md` | Code of conduct | 2 |
| `resources/support.md` | Support VFO | 3 |
| `resources/scenery.md` | Scenery | 4 |
| `resources/aircraft.md` | Aircraft | 5 |
| `resources/peripherals.md` | Peripherals | 6 |
| `resources/tools.md` | Tools and software | 7 |
| `resources/glossary.md` | Glossary | 8 |
| `resources/useful-links.md` | Useful links | 9 |

## Guides section (`guides/`)

| File | Title | nav_order |
| --- | --- | --- |
| `guides/getting-started-msfs.md` | Getting started with MSFS | 1 |
| `guides/getting-started-xplane.md` | Getting started with X-Plane | 2 |
| `guides/vfr-basics.md` | VFR basics | 3 |
| `guides/ifr-basics.md` | IFR basics | 4 |
| `guides/navigation.md` | Navigation | 5 |
| `guides/atc-communications.md` | ATC communications | 6 |
| `guides/simbrief.md` | SimBrief | 7 |
| `guides/littlenavmap.md` | Little Navmap | 8 |
| `guides/weather-planning.md` | Weather planning | 9 |
| `guides/checklists.md` | Checklists | 10 |

## Events section (`events/`)

| File | Title | nav_order |
| --- | --- | --- |
| `events/upcoming.md` | Upcoming events | 1 |
| `events/archive/index.md` | Archive | 2 |

## Events archive section (`events/archive/`)

| File | Title | nav_order |
| --- | --- | --- |
| `events/archive/2025.md` | 2025 events | 1 |
| `events/archive/2024.md` | 2024 events | 2 |

## Adding a new top-level page

The current highest top-level `nav_order` is **7** (Events). A new top-level page should use `nav_order: 8` or higher.

## Adding a new child page to Operations

The current highest child `nav_order` in Operations is **10** (Multi-crew flying). A new child should use `nav_order: 11` or higher.

## Adding a new child page to Community

The current highest child `nav_order` in Community is **5** (Forums and discussion). A new child should use `nav_order: 6` or higher.

## Adding a new child page to Resources

The current highest child `nav_order` in Resources is **9** (Useful links). A new child should use `nav_order: 10` or higher.

## Adding a new child page to Guides

The current highest child `nav_order` in Guides is **10** (Checklists). A new child should use `nav_order: 11` or higher.

## Adding a new child page to Events

The current highest child `nav_order` in Events is **2** (Archive). A new child should use `nav_order: 3` or higher.
