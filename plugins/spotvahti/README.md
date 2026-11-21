# SpotVahti plugin

Compare Finnish electricity contracts inside Claude. The plugin connects to the public SpotVahti MCP server
(`https://spotvahti.fi/mcp`, read-only, no sign-in) and adds a skill that walks through choosing a contract:
yearly consumption or home type, optional postal code for local suppliers, the cheapest spot, fixed and hybrid
contracts by estimated yearly cost, supplier terms, realized spot price statistics and grid transmission fees.

Install in Claude Code:

    /plugin install spotvahti --marketplace synthentica/spotvahti-ai

Ask for example: "Mikä on halvin pörssisähkösopimus omakotitaloon, jossa on maalämpö?" or
"Which fixed-price electricity contract is cheapest for 5 000 kWh a year in Tampere?"

Prices include VAT 25.5 % but exclude transmission and electricity tax. Always confirm the price with the supplier.
Data: SpotVahti and Energiavirasto / Sähkönhinta-palvelu (CC BY 4.0, modified); spot prices Ember (CC BY 4.0).

Privacy: https://spotvahti.fi/en/privacy/ · Docs: https://spotvahti.fi/en/ai/ · Contact: info@spotvahti.fi
