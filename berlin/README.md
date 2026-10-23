# Berlin Coworking & Flexible Office Price Index (Oct 2026), v1.1

Publisher: CoworkingView, https://coworkingview.com (Sonnenallee 279, 12057 Berlin)
License: CC-BY-4.0 https://creativecommons.org/licenses/by/4.0/
Source: CoworkingView Price Index (https://www.coworkingview.com/en/tools/price-index), as of October 2026. Licensed under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). Aggregated figures only; no endorsement by CoworkingView or any operator is implied.
The Price Index and catalogue data in this dataset are licensed CC BY 4.0. This licence covers the CoworkingView Price Index and catalogue data in this dataset: prices and price statistics, space and operator names, and descriptions written by CoworkingView. It does not cover, and this dataset does not contain: photos, logos, reviews or ratings, data obtained from Google, or any other content of coworkingview.com, its API or MCP server, which remain subject to their own terms. Names are included for identification only; no trademark rights in CoworkingView or operator names and marks are licensed.
Snapshot: 2026-10-17 (live /api/price-index, generatedAt 2026-10-17T21:45:49Z) · Version: 1.1 · Update cadence: monthly · Contact: https://coworkingview.com/en/contact

## Files
- `berlin-office-price-index-2026-10.csv`: summary stats (EUR/month, net list prices) by workspace type.
- `berlin-entry-price-distribution-2026-10.csv`: individual entry prices are not published.

## Columns
city · scope (`listed_price_per_desk` = all priced desk/office plans, normalised per desk; `entry_price` = cheapest public plan per building, NOT per desk) · workspace_type (`all`, `flex_desk`, `fix_desk`, `private_office`) · metric (median/avg/min/max/p10/p25/p75/p90, or `not_published`) · value_eur_month · sample_size (price points) · property_count (buildings) · currency · snapshot_date · source.

## Key figures
- Median per desk: **315 €** (p25 240 €, p75 453 €; 186 price points, 84 buildings)
- Fixed desk median 320 € (55 buildings) · Flex desk median 219 € (65 buildings)
- Entry price median 270 € (99 buildings). Individual entry prices are not published.
- Private office per desk: **not published** in this snapshot (the index does not publish a per-desk private office median for Berlin at this date). Entry-price rows for private_office are whole-room prices, not per desk.

## Methodology
- Universe: Berlin coworking / flexible office spaces listed on coworkingview.com: **139 listed, 84 with indexable prices**.
- Same computation as the live index at https://coworkingview.com/de/tools/price-index/berlin: medians over per-desk monthly list prices; private office prices divided by that room's own seat count (never building capacity); day/week/year prices converted to a monthly equivalent; implausible values outside the currency price band excluded; a figure is published only if at least 5 buildings stand behind it.
- Excludes virtual office / business address and meeting rooms.
- Not a transaction price index: discounts, VAT and service charges are not included. Prefer medians over averages.
- Entry by type sample sizes overlap (a building can have an entry price for several types).

## Changelog
- **v1.1 (2026-10-18):** regenerated from the full catalogue via the live /api/price-index (139 listed, 84 buildings with indexable prices, 186 price points). Figures now match the website. Added p10/p90 per desk type and entry stats by type; private office per-desk marked `not_published`; entry distribution n=99. Attribution URL now points to the Price Index hub.
- v1.0 (2026-10-17): **partial** snapshot (56 listings, 35 spaces, 76 price points). Superseded; do not cite v1.0 figures (median 325 €, fixed desk 350 €, private office 480 €, entry median 283 €).

## Citation
CoworkingView (2026). Berlin Coworking & Flexible Office Price Index, October 2026 (v1.1). https://coworkingview.com/de/tools/price-index/berlin. DOI: 10.5281/zenodo.23441028 (concept). https://creativecommons.org/licenses/by/4.0/
