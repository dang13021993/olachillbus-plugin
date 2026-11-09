# OlaChill Bus

Coaches, minibuses and vans with a professional driver for groups in the Schengen area of Europe. Use it to see which countries are served, which vehicle fits a group, and how to request a quote on [olachillbus.com](https://olachillbus.com).

This package contains configuration only. It connects your assistant to the public, read-only MCP server at `https://olachillbus.com/mcp` (Streamable HTTP, no sign-in, no API key). The server exposes three tools:

| Tool | What it does |
|---|---|
| `list_charter_countries` | Countries currently served (Schengen area) |
| `list_charter_vehicles` | Vehicle classes in a country: seats, recommended group size, large suitcases |
| `get_charter_quote_instructions` | Where to request a quote and which trip details it needs |

The tools are read-only. They do not send requests, book, take payment or confirm availability. Prices on olachillbus.com are estimates ("from" a stated amount) or published flat rates, confirmed by a local coach company after a quote request.

## Install

| Client | Command |
|---|---|
| Claude Code | `/plugin marketplace add dang13021993/olachillbus-plugin` then `/plugin install olachillbus@olachillbus` |
| Gemini CLI | `gemini extensions install https://github.com/dang13021993/olachillbus-plugin` |
| Qwen Code | `qwen extensions install dang13021993/olachillbus-plugin` |
| Kimi Code | `/plugins install https://github.com/dang13021993/olachillbus-plugin` |
| DeepSeek Harness | `dsh plugin --profile <profile> add github:dang13021993/olachillbus-plugin` |
| Any MCP client | Streamable HTTP URL `https://olachillbus.com/mcp` |

## Example prompts

- "Which countries can I hire a coach with driver in through OlaChill Bus?"
- "We are 42 people in France. Which coach fits us and our suitcases?"
- "How do I ask for a quote for a coach from Paris to Brussels on 12 May?"

Coach hire in Japan is not offered here; see https://olachill.com.

## Contact

helo@olachillbus.com · https://olachillbus.com · License: MIT.
