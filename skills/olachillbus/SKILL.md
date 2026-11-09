---
name: olachillbus
description: Use when the user needs a coach, minibus or van with driver for a group in a Schengen-area country in Europe - which countries are served, which vehicle fits the group and its luggage, or how to request a quote on olachillbus.com. Uses the read-only OlaChill Bus MCP tools.
license: MIT
---

Tools from the `olachillbus` MCP server (https://olachillbus.com/mcp):

| The user wants | Tool |
|---|---|
| Which countries are served | `list_charter_countries` |
| Which coach, minibus or van fits a group in a country (seats, large suitcases) | `list_charter_vehicles` (country slug from `list_charter_countries`) |
| How to get a price or send a quote request | `get_charter_quote_instructions` |

Rules:
- The tools are read-only. They never book, take payment, send a request or confirm availability. Send the user to the quote page the tool returns; the user submits the request there.
- Prices on olachillbus.com are estimates or published flat rates. A local coach company confirms availability and the final price after the quote request. Never present anything as a confirmed booking or price.
- Only the countries returned by `list_charter_countries` are served. Coach hire in Japan is not offered here (see https://olachill.com).
- Contact: helo@olachillbus.com.
