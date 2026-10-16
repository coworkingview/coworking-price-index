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

CC BY 4.0. Credit "CoworkingView" with a link:

> Source: CoworkingView — Coworking Price Index,
> https://coworkingview.com/en/tools/price-index. CC BY 4.0.

Live data with the same terms: `https://coworkingview.com/api/price-index`
(JSON) and the MCP server `https://mcp.coworkingview.com/mcp`.

Regenerate: `node scripts/export-open-dataset.mjs` in the CoworkingView repo.
