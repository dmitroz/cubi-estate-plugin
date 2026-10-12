# Cubi Estate

Search more than 2.2 million homes for sale and rent across 17 European countries, in English, Portuguese, Spanish, French, German, Dutch or Russian, without leaving your conversation with Claude.

Covered countries: Portugal, Spain, Italy, France, Germany, Belgium, Austria, Finland, Cyprus, Croatia, Slovakia, Malta, Greece, Czech Republic, Poland, Netherlands and Bulgaria.

This plugin connects Claude to the [Cubi Estate](https://www.cubi.estate) connector and adds skills that teach Claude how to use it well: which search to run, how to show results with their original links, how to read an asking-price comparison honestly, and how to help you reach an agent without sharing anyone's contact details.

## What you can ask

- *"Find a 2-bedroom apartment in Porto under €400,000 with a balcony."*
- *"Show me the full details and photos of the second one."*
- *"Is this villa's asking price high compared with similar homes nearby?"*
- *"How can I contact the agent for this listing?"*
- *"How many new listings did Spain add this week, and are prices dropping?"*

## What's inside

| Skill | What it does |
|---|---|
| `find-homes` | Picks the fast structured filter or the free-text search, shows results with their listing links exactly as returned, and opens a listing's full details. |
| `check-asking-price` | Compares a listing's asking price with comparable active listings in the same city, and says plainly that it is not a valuation. |
| `contact-agent` | Lists the ways to reach the agent through Cubi's consented contact flow, with suggested questions the listing does not answer, and the link to start. Nothing is sent until you follow the link and confirm there. |
| `market-pulse` | Reads Cubi's aggregate statistics: new and removed listings, price drops, and environmental data coverage such as flood risk. |

All of the plugin's tools are **read-only**: they search and read listing data and never change anything. Agents' phone numbers and email addresses are never returned.

## Setup

After you add the plugin, connect **Cubi Estate** on the plugin's **Connectors** tab. No account or sign-in is needed: anonymous use is rate-limited, with a daily budget that ordinary conversational use will not reach. Clients that support it may instead connect per user with OAuth.

## Data and privacy

The plugin itself stores nothing and runs no code on your computer: it is a set of instructions for Claude plus the address of Cubi Estate's connector.

**What is sent, and where.** When Claude uses a Cubi tool, the request goes to Cubi Estate's server at `https://mcp.cubi.estate/mcp`, the same server as the Cubi Estate connector, and nowhere else. The server answers from Cubi's own index of listings, built in advance; it does not fetch the listing sites while you ask. Each tool call is logged with the tool name, its arguments (including your search text), the listings returned, timing, status, your IP address and User-Agent, and the OAuth client id for signed-in use. Free-text search queries and network addresses are removed after 7 days, and the whole record is deleted after 14 days; encrypted database backups may keep copies for up to about two weeks longer, used only to recover from failures. Logs are used only to run and secure the service. Full details: [cubi.estate privacy policy](https://www.cubi.estate/privacy-policy).

**Links you choose to follow.** Results show links: a listing's page on cubi.estate or on the original listing site, and, for contacting an agent, a link to a Cubi chat about that home on cubi.estate (sign-in required). Claude never opens these for you. Questions or requests you send from that chat are relayed to the agent by Cubi's team through Cubi's consented contact flow, only after you confirm them there; agents' own contact details are never shared.

## Coverage

Listings are gathered from public property portals and agencies in the covered countries. Each result links to the original listing and says when its data last changed. Prices are the sellers' asking prices, and availability, prices and descriptions can change: check them at the source before making any decision.

## Support

Questions or problems: write to support@cubi.estate or open an issue in this repository.
