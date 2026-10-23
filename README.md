---
license: cc-by-4.0
pretty_name: Coworking Price Index
language:
  - en
tags:
  - coworking
  - flexible-office
  - real-estate
  - prices
  - europe
size_categories:
  - n<1K
---

# Coworking Price Index

Monthly prices of coworking desks and private offices in European cities,
taken from the prices the operators themselves publish. Maintained by
[CoworkingView](https://coworkingview.com/en/tools/price-index), an
independent platform to compare coworking spaces and flexible offices.

## Files

| File | One row per | Main columns |
|---|---|---|
| `price-index-cities.csv` | city | `median_per_desk_month`, `p25`, `p75`, `price_points`, `buildings_priced`, `source_url` |
| `price-index-by-type.csv` | city × workspace type | `workspace_type` (`fix_desk`, `flex_desk`, `private_office`), `median_per_month`, `p25`, `p75` |
| `price-index.json` | — | the same figures with the API's own field names and notes |
| `berlin/berlin-office-price-index-2026-10.csv` | Berlin × workspace type × metric | median, avg, min, max, p10–p90, `sample_size`, `property_count` (v1.1, see `berlin/README.md`) |
| `berlin/berlin-entry-price-distribution-2026-10.csv` | — | placeholder: individual entry prices are not published |

`berlin/` is the detailed Berlin snapshot (October 2026, v1.1) with its own
methodology, changelog and DOI: see [`berlin/README.md`](berlin/README.md).

Prices are per desk per month in the city's currency (EUR, GBP). A private
office price is normalised per desk.

## Method

- Source: prices published by the operators on their own websites, collected
  per listing on CoworkingView. No survey and no asking prices from brokers.
- A figure is published only when at least 5 price points stand behind it.
  Cities and types below that floor are left out, not estimated.
- Each city's live page explains the figure and lists the spaces behind it:
  see `source_url`.

## Licence and citation

The Price Index and catalogue data in this repository are licensed
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (full text in
`LICENSE`). The licence covers the CoworkingView Price Index and catalogue
data in these files: prices and price statistics, space and operator names,
and descriptions written by CoworkingView. It does not cover, and these files
do not contain: photos, logos, reviews or ratings, data obtained from Google,
or any other content of coworkingview.com, its API or MCP server, which remain
subject to their own terms (coworkingview.com/en/terms, section 9). Names are
included for identification only; no trademark rights are licensed.

Attribution — credit "CoworkingView" with a link:

> Source: CoworkingView — Coworking Price Index,
> https://coworkingview.com/en/tools/price-index. CC BY 4.0.

Cite the Berlin snapshot as:

> CoworkingView (2026). Berlin Coworking & Flexible Office Price Index,
> October 2026 (v1.1). https://coworkingview.com/de/tools/price-index/berlin.
> DOI: 10.5281/zenodo.23441028. CC BY 4.0.

The live figures are on the website, and also served by
`https://coworkingview.com/api/price-index` (JSON) and the MCP server
`https://mcp.coworkingview.com/mcp`; those two services are governed by the
CoworkingView Terms, not by this licence.

Wikidata: [Q141749363](https://www.wikidata.org/wiki/Q141749363) (dataset), published by
[CoworkingView (Q141749338)](https://www.wikidata.org/wiki/Q141749338).

Regenerate: `node scripts/export-open-dataset.mjs` in the CoworkingView repo.
