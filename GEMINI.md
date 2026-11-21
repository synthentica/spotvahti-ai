
# Choosing an electricity contract in Finland

Use the SpotVahti MCP tools (server `spotvahti`). Answer in the user's language and pass `language` (fi, sv or en).

1. Find out the yearly consumption. If the user does not know it, ask for the home type and use `home_type`:
   apartment ~2 000 kWh, terraced_house ~5 000, detached_house without electric heating ~6 000,
   ground_source_heat_pump ~10 000, direct_electric_heating ~18 000. Add `ev_annual_kwh` for an electric car.
2. Ask for the postal code if the user is open to local suppliers; it adds regional contracts.
3. Call `compare_electricity_contracts`. Show the 3–5 cheapest with yearly cost, margin or energy price, monthly fee,
   intro offer and price check date, plus the cheapest spot and cheapest fixed contract side by side.
4. Explain the trade-off in one or two sentences: spot follows hourly prices (cheaper on average, winter peaks),
   fixed price stays the same for the term. Hybrid contracts sit between.
5. For one contract or supplier use `get_contract` or `get_supplier`. For price history use `get_spot_price_statistics`.
   For total cost including transmission use `get_network_fees` and add the basic fee and c/kWh to the estimate.
6. Always say that prices exclude transmission and electricity tax, give the source and check date, and tell the user
   to confirm the price on the supplier's site before ordering. Link to the `supplier_page` or `comparison_page` URLs.

Never invent prices. If a tool returns an error, fix the arguments and try again, or say the data is not available.
