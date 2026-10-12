---
name: find-homes
description: Search Cubi Estate's listings of homes for sale or rent in Europe. Use when the user asks to find, filter or refine apartments, houses, villas or plots in a European town or region, or wants more detail on a home from earlier Cubi results. Not for general real-estate discussion that needs no listing search.
---

# Find homes with Cubi Estate

Cubi Estate's connector searches live listings across 17 European countries, in English, Portuguese, Spanish, French, German or Dutch. Every tool is read-only.

## Choose the tool

- **`filter_listings`** when the user has named towns or cities and a budget, or the filters are already known from earlier turns. It runs no language model and answers in about a second. Pass towns or cities, not a whole country or a landscape region.
- **`search_properties`** for a free-text request ("quiet flat near the beach under 300k", "Algarve or Andalusia"). It takes 5–10 seconds, so say you are searching.
- **`get_listing`** when the user wants one home's full description, every feature, or all of its photos.

## Run the search

1. Collect what matters: place, buy or rent, budget, bedrooms, property type. Ask one short question only if the place is missing; use sensible defaults for the rest.
2. Call the tool in the user's language (`lang`), with `limit` between 5 and 10 for a first look.
3. If a reply is an error with a `next_action`, follow it instead of retrying the same call. If it says a place was not recognised, use the suggestion it gives or ask the user which town they mean.
4. When you follow up on a result with `get_listing` or `filter_listings`, pass the `Cubi request id` printed at the end of the earlier result as `parent_request_id`.

## Present the results

- Show each home's price, place, size, bedrooms and the one or two features that match the request.
- Show every listing URL **exactly as returned**. Never build, shorten or edit a URL or a listing id; the link is how the user reaches the home.
- Each card says when its data last changed. If it is old, say so rather than presenting it as current.
- If the search offers narrowing options, mention them after the results as optional next searches. Run one only if the user picks it.
- If nothing matches, say what you searched for and suggest one concrete way to widen it, such as a higher budget or a neighbouring town. Never describe homes that the tools did not return.

## Limits to respect

- Coverage is the 17 countries the connector names. For anywhere else, say Cubi does not cover it rather than guessing.
- Prices are asking prices from the listing sources, not valuations.
- Cubi never returns an agent's phone number or email. To help the user get in touch, use the `contact-agent` skill.
