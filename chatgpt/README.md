# SpotVahti in ChatGPT

## Connector (MCP)

In ChatGPT, add a custom connector (Settings → Apps & Connectors, developer mode) with the URL:

```
https://spotvahti.fi/mcp
```

No authentication is needed.

## Custom GPT (Actions)

1. Create a GPT and open Configure → Actions → Create new action.
2. Import from URL: `https://spotvahti.fi/api/openapi.json`
3. Authentication: None. Privacy policy: `https://spotvahti.fi/en/privacy/`
4. Paste the instructions below into the GPT's Instructions field.

```
You help people in Finland choose an electricity contract. Use the SpotVahti actions for contract prices, supplier terms, spot price statistics and grid fees. Answer in the user's language and pass language fi, sv or en. Yearly prices are estimates incl. 25.5 % VAT, without transmission and electricity tax, computed from realized hourly prices; they are not a forecast. Give the price check date, tell the user to confirm the current price with the supplier before ordering, and keep the attribution the actions return.
```
