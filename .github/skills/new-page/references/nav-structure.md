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

## Community section (`community/`)

| File | Title | nav_order |
| --- | --- | --- |
| `community/discord.md` | Discord | 1 |
| `community/newsletter.md` | Newsletter | 2 |
| `community/facebook.md` | Facebook group | 3 |

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

## Adding a new top-level page

The current highest top-level `nav_order` is **5** (Resources). A new top-level page should use `nav_order: 6` or higher.

## Adding a new child page to Operations

The current highest child `nav_order` in Operations is **7** (Live radar). A new child should use `nav_order: 8` or higher.

## Adding a new child page to Community

The current highest child `nav_order` in Community is **3** (Facebook group). A new child should use `nav_order: 4` or higher.

## Adding a new child page to Resources

The current highest child `nav_order` in Resources is **3** (Support VFO). A new child should use `nav_order: 4` or higher.
