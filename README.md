# SF Rent

**Know before you sign.** Type in a San Francisco address and see what the city knows about the building before you sign a lease. Free, and it all comes from public records.

Live at **[sfrent.jonbobrow.com](https://sfrent.jonbobrow.com)**. A sibling of [NYC Rent](https://nycrent.jonbobrow.com).

## What it checks

| Check | Source (DataSF) |
| --- | --- |
| **Rent control**: likely covered, eviction rules only, state cap, or no cap, from the building's age and type, plus what units here rent for | Assessor secured roll, Rent Board housing inventory and allowable increases |
| **Code violations**: open DBI notices of violation, fire violations, director's hearings and City Attorney referrals | DBI notices of violation and complaints, Fire Department violations |
| **Repairs**: heat, hot water, mold, leaks, paint and other housing complaints in the past 2 years | DBI complaints, 311 |
| **Bedbugs and pests** at the address | 311 (Health Department), DBI complaints |
| **Evictions and buyouts**: eviction notices on the block by year and reason (owner move-in, Ellis Act…), buyouts at the address | Rent Board eviction notices and buyout agreements |
| **Rent Board petitions** on the block, including capital improvement passthroughs | Rent Board petitions |
| **Earthquake safety**: soft-story retrofit status, liquefaction and landslide zones | Soft-story program, state seismic hazard zones |
| **Legal units**: tax roll vs. the city's address list vs. the Rent Board, plus illegal-unit complaints | Assessor, Enterprise Addressing System, DBI |
| **Flood risk**: 100-year storm flood zone, sea level rise, street flooding reports | SFPUC flood maps, BCDC sea level rise, 311 |
| **Construction nearby**: new buildings, demolition, excavation, retrofits, added units, big renovations, night work | DBI building permits, night noise permits |
| **Noise** and **car break-ins** within 150 m | 311, police incident reports |
| **The property**: use, sale date, assessed value, owner-occupied, historic status, zoning, parking permit area | Assessor, Planning historic status, SFMTA RPP parcels |

Plus an apartment view (DBI complaints and notices that name the unit, and whether the unit is in the city's address list), California and San Francisco renter rights, questions to ask the landlord, and a copyable summary and shareable link.

Comparisons use a random sample of 213 San Francisco buildings with three or more units (88 for the block checks), drawn in October 2026.

## Oakland and Berkeley (partial report)

Oakland and Berkeley addresses get a partial report, because neither city publishes the building records San Francisco does (code violations, permits, eviction notices, a soft-story list). What's public:

| Check | Oakland | Berkeley |
| --- | --- | --- |
| Complaints about the address | OAK 311 code enforcement reports | 311 housing inspection requests |
| Illegal dumping, pests nearby | OAK 311 | Berkeley 311 |
| Car break-ins | CrimeWatch, within 150 m | Police cases, on the block |
| Noise | — (not published by location) | Police noise calls on the block + 311 |
| Earthquake | State Alquist-Priolo fault, liquefaction and landslide zones | same |
| Wildfire | CAL FIRE 2025 fire hazard severity zones | same |
| Flood | State tsunami area, 311 storm drain flooding | State tsunami area |
| Rent rules | Rent Adjustment Program rules and 2.3% cap | Rent Board rules, 1.0% AGA, link to the Rent Registry lookup |

Each East Bay report ends with **Help the city track more**: a list of what's missing and a ready-to-send note asking the councilmember and mayor to publish it. Addresses are found with Esri's World Geocoder. Comparisons use 90 random Oakland parcels and 90 random Berkeley apartment buildings.

## How it works

One static `index.html`. The browser queries DataSF's Socrata API (`data.sf.gov`) directly; addresses come from the city's Enterprise Addressing System. There's no server and nothing is stored except recent lookups in your own browser.

The header's watercolor Victorians (an Italianate, a Queen Anne and an Edwardian over a garage) step down a hill, and the street tree follows the season.

## Caveats

- Rent control is an estimate from year built and building type. Only the Rent Board can say for sure.
- Rent Board eviction notices and petitions are published by street block, not building.
- San Francisco doesn't publish owner names in its open data.
- A few yearly figures are written into the page: the state AB 1482 cap (8.8%, Aug 2026 – Jul 2027), deposit interest (4.2%, Mar 2026 – Feb 2027) and the screening fee cap ($65.86 in 2026). Update them each year.
- A clean record is a good sign, not a guarantee.

## Share image and video

`og/og-image.html` and `og/og-video.html` render the link preview (`og/render.sh`, `og/render-video.sh`). Bump the `?v=` on the meta tags after re-rendering.

Made by [Jon Bobrow](https://apps.jonbobrow.com).
