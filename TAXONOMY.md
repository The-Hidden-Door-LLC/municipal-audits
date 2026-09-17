# Taxonomy

This repository classifies municipal audits two ways. Both are required on every case.

## 1. Place — Census FIPS

Path shape:

```
cases/US/{ST}/{ss-ppppp-slug}/
```

- `{ST}` — USPS state abbreviation (`TN`)
- `{ss}` — Census state FIPS (`47` for Tennessee)
- `{ppppp}` — Census place FIPS (zero-padded to 5)
- `{slug}` — lowercase kebab name of the municipality

Example: Bartlett, Tennessee → `cases/US/TN/47-03440-bartlett/`

Counties use county FIPS in place of place FIPS and a `-county` suffix on the slug when needed.

## 2. Function — Census of Governments (COG) function codes

Functional classification follows the U.S. Census Bureau *Census of Governments* expenditure function codes (government finance statistics). A case may carry multiple function codes; the primary code is listed first in `CASE.md`.

| Code | Function |
|------|----------|
| 01 | Financial administration |
| 02 | Central staff services |
| 03 | General public buildings |
| 04 | Judicial and legal |
| 05 | Other governmental administration |
| 12 | Police protection |
| 14 | Fire protection |
| 15 | Corrections |
| 16 | Protective inspection and regulation |
| 20 | Highways (streets) |
| 21 | Toll highways |
| 22 | Airports |
| 23 | Parking facilities |
| 24 | Sea and inland port facilities |
| 25 | Other transportation |
| 26 | Water transport and terminals |
| 29 | Transit |
| 32 | Health |
| 36 | Hospitals |
| 39 | Own hospitals |
| 44 | Municipal electric power |
| 45 | Municipal gas supply |
| 50 | Public welfare |
| 52 | Housing and community development |
| 55 | Sewerage |
| 56 | Solid waste management |
| 59 | Other natural resources |
| 61 | Parks and recreation |
| 62 | Housing and community development (alternate listings) |
| 79 | Other education |
| 80 | Libraries |
| 81 | Protective inspection (local variants) |
| 87 | General government NEC / central garage & fleet when so budgeted |
| 89 | Other and unallocable |
| 90 | Liquor stores |
| 91 | Water supply |
| 92 | Electric power |
| 93 | Gas supply |
| 94 | Transit utilities |

**Fleet / vehicle maintenance** is tagged with the function code under which the municipality budgets it (often `20` Highways, `12` Police, `14` Fire, `56` Solid waste, and/or `87` / central garage). Cases also carry THD topic tags (below).

Index mirrors live under `functions/{code}-{slug}/README.md` and link back to cases.

## 3. THD topic tags

Investigation lens, not Census. Stored in `CASE.md` front matter as `topics:`.

| Tag | Meaning |
|-----|---------|
| `open-books` | Macro budgets vs payment-level publication |
| `fleet-payees` | Who is paid to maintain municipal fleet |
| `records-access` | TPRA / FOIA friction, portals, fees, residency gates |
| `contracts` | Contract / PO / award transparency |
| `procurement` | Bid / RFP publication and award disclosure |

## 4. Aletheia

Source of truth for each case is an Aletheia Protocol evidence record (`*.aletheia.md`) under `evidence/`. Renditions under `renditions/` are replaceable views. The record speaks; the Assistant does not own it.

Protocol: https://github.com/KarstenEvans/aletheia-protocol
