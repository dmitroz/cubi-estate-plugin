---
name: check-asking-price
description: Compare a home's asking price with similar homes nearby. Use when the user asks whether a listing is expensive, cheap, overpriced or a good deal, or how its price compares with the local market, for a home found through Cubi Estate.
---

# Check an asking price against comparable homes

1. Make sure you have the listing's id exactly as a Cubi result printed it (for example `remax:12345`). If the user only describes a home, find it first with the `find-homes` skill. Never invent an id.
2. Call `compare_asking_prices` with that id and the user's language.
3. Report where the asking price sits against the range (below, within or above), the range itself (25th to 75th percentile) and how many comparable listings it rests on.

## Say what it is, and what it is not

- This compares **asking prices of active listings in the same city**. It is not a valuation, not a sale-price estimate, and not financial or real-estate advice. Say so in one plain sentence every time.
- Do not turn "below", "within" or "above" into a verdict: never call a home a good deal, fairly priced or a bargain, and never recommend buying, offering or walking away.
- With only a handful of comparables, say the comparison is thin.
- When the tool returns no range because too few comparables exist, say that. Do not estimate one yourself.
- Comparables can differ in condition, view, floor or exact location. Point out anything in the listing that could explain a price above or below the range, and suggest an independent valuation before any purchase decision.
