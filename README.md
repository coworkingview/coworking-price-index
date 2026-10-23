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
[CoworkingView](https://www.coworkingview.com/en/tools/price-index), an
independent platform to compare coworking spaces and flexible offices.

## Files

| File | One row per | Main columns |
|---|---|---|
| `price-index-cities.csv` | city | `median_per_desk_month`, `p25`, `p75`, `price_points`, `buildings_priced`, `source_url` |
| `price-index-by-type.csv` | city × workspace type | `workspace_type` (`fix_desk`, `flex_desk`, `private_office`), `median_per_month`, `p25`, `p75` |
| `price-index.json` | — | the same figures with the API's own field names and notes |

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

SPDX-License-Identifier: `CC-BY-4.0`. The full legal code is in [LICENSE](LICENSE) (the plain-text Creative Commons Attribution 4.0 International legal code).

This licence covers the CoworkingView Price Index and catalogue data in this dataset: prices and price statistics, space and operator names, and descriptions written by CoworkingView. It does not cover, and this dataset does not contain: photos, logos, reviews or ratings, data obtained from Google, or any other content of coworkingview.com, its API or MCP server, which remain subject to their own terms. Names are included for identification only; no trademark rights in CoworkingView or operator names and marks are licensed.

Attribution (October 2026 release):

> Source: CoworkingView Price Index (https://www.coworkingview.com/en/tools/price-index), as of October 2026. Licensed under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). Aggregated figures only; no endorsement by CoworkingView or any operator is implied.

> Quelle: CoworkingView Preisindex (https://www.coworkingview.com/de/tools/price-index), Stand Oktober 2026. Lizenz: CC BY 4.0. Nur aggregierte Werte; keine Billigung durch CoworkingView oder Betreiber.

> Fuente: Índice de precios de CoworkingView (https://www.coworkingview.com/es/tools/price-index), octubre de 2026. Licencia: CC BY 4.0. Solo cifras agregadas; no implica respaldo de CoworkingView ni de ningún operador.

Wikidata: [Q141749363](https://www.wikidata.org/wiki/Q141749363) (dataset), published by
[CoworkingView (Q141749338)](https://www.wikidata.org/wiki/Q141749338).

Regenerate: `node scripts/export-open-dataset.mjs` in the CoworkingView repo.

## Changelog

- 23 Oct 2026: Licence is CC BY 4.0 (SPDX `CC-BY-4.0`) with the scope in Licence and citation: the Price Index and catalogue data in this dataset (prices and price statistics, space and operator names, and descriptions written by CoworkingView). Photos, logos, reviews, ratings, data obtained from Google, and any other content of coworkingview.com, its API or MCP server are outside this licence.
