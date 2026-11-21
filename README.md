# SpotVahti for AI assistants

Public, read-only MCP server and plugins for [SpotVahti](https://spotvahti.fi), an independent Finnish electricity contract comparison.

**MCP endpoint:** `https://spotvahti.fi/mcp` (Streamable HTTP, no sign-in)
**REST/OpenAPI:** `https://spotvahti.fi/api/openapi.json`
**Docs:** https://spotvahti.fi/en/ai/ · [suomeksi](https://spotvahti.fi/ai/) · [på svenska](https://spotvahti.fi/sv/ai/)

## Tools

| Tool | What it answers |
| --- | --- |
| `compare_electricity_contracts` | Cheapest Finnish contracts by yearly cost for a consumption, home type and postal code |
| `get_contract` | Terms and yearly cost of one contract |
| `get_supplier` | All contracts of a supplier |
| `get_spot_price_statistics` | Realized spot price averages by month, year and hour of day |
| `get_network_fees` | Grid transmission fees of Finnish network companies |

All tools are read-only and return the data source and price check date.

## Install

- **Claude Code:** `/plugin marketplace add synthentica/spotvahti-ai`, then `/plugin install spotvahti@spotvahti-ai`
- **Claude (web/desktop):** Settings → Connectors → Add custom connector → `https://spotvahti.fi/mcp`
- **ChatGPT:** add a custom connector with `https://spotvahti.fi/mcp`, or build a Custom GPT with the OpenAPI actions, see [chatgpt/README.md](chatgpt/README.md)
- **Gemini CLI:** `gemini extensions install https://github.com/synthentica/spotvahti-ai`
- **Any MCP client:** add `https://spotvahti.fi/mcp` as a remote (HTTP) server

## Data and licences

Contract data: SpotVahti (checked on suppliers' websites) and Energiavirasto / Sähkönhinta-palvelu, CC BY 4.0, modified (own verified prices added, fields combined). Spot prices: Ember, CC BY 4.0, original source Nord Pool. Prices are estimates; confirm with the supplier before ordering.

Privacy: the server stores no personal data. See https://spotvahti.fi/en/privacy/#ai-assistants · Contact: info@spotvahti.fi

Code in this repository: MIT licence.
