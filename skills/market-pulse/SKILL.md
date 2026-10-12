---
name: market-pulse
description: Describe how a European property market is moving. Use when the user asks how much new inventory is coming onto the market, whether prices are dropping, how many homes are listed in a country, or how widespread flood risk, noise or other environmental factors are in Cubi Estate's listings.
---

# Read the market from Cubi's aggregate statistics

These tools return counts only, never individual listings.

## Choose the tool

- **`corpus_stats`**: active listings in total and by country, plus a day-by-day series of new listings, deactivated listings and detected price drops (with the average drop size). Use `days` for the window (1–90) and `country` with a full country name, such as "Portugal", to narrow it.
- **`get_daily_new_listing_stats`**: new listings for today, yesterday and the last 7 full days, by country, split into sale and rent, plus the sources adding the most.
- **`data_layer_stats`**: how many active listings carry each environmental layer (noise, air quality, greenery, coast, flood, drive time), the flood-risk split, and each country's share of listings in a high-risk river floodplain.

## Present it

- Lead with the number that answers the question, then the trend over the window.
- Counts describe **Cubi's own listings**, gathered from the sources it covers. They are not official market statistics or national totals, and a jump can come from a source being added or removed. Say this once when it matters to the answer.
- A day with an unusually low count may be a source that did not report; do not read it as a market event.
- Flood figures are modelled floodplain exposure, not a statement about any particular home.
