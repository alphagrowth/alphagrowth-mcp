<img src="logo.png" alt="AlphaGrowth" width="72" />

# AlphaGrowth MCP server

Free crypto data for AI agents. No API key, no sign-up.

Project metrics (TVL, market cap, price, fees, revenue, users), community growth, funding rounds and investors, chains, DeFi yield pools, token unlock calendars and DAO treasuries, from [AlphaGrowth](https://alphagrowth.io). Every result carries a source block to cite.

- **Endpoint:** `https://alphagrowth.io/mcp` (remote, Streamable HTTP, no auth)
- **Tools:** 37, all read-only
- **Docs:** https://alphagrowth.io/mcp-server
- **Official MCP Registry:** `io.alphagrowth/data`

This repository holds the server's public listing files. The server itself is hosted by AlphaGrowth; there is nothing to install or run.

## Add it to your client

**Cursor:** [Add to Cursor](https://cursor.com/en/install-mcp?name=alphagrowth&config=eyJ1cmwiOiJodHRwczovL2FscGhhZ3Jvd3RoLmlvL21jcCJ9)

**VS Code:** [Add to VS Code](https://vscode.dev/redirect/mcp/install?name=alphagrowth&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Falphagrowth.io%2Fmcp%22%7D)

**Claude Code:**

```sh
claude mcp add --transport http alphagrowth https://alphagrowth.io/mcp
```

**Claude:** Settings → Connectors → Add custom connector, then paste `https://alphagrowth.io/mcp`.

**Hermes Agent:**

```sh
hermes plugins install alphagrowth --enable
```

The plugin adds the server and three skills: crypto project research, DeFi market scan and crypto funding research. Start a new session after installing. Before the catalog listing, install from this repository with `hermes plugins install alphagrowth/alphagrowth-mcp --enable`.

**Gemini CLI:**

```sh
gemini extensions install https://github.com/alphagrowth/alphagrowth-mcp
```

**Any other MCP client:**

```json
{
  "mcpServers": {
    "alphagrowth": {
      "url": "https://alphagrowth.io/mcp"
    }
  }
}
```

## Try asking

- Which DeFi projects on Base have the most TVL?
- What are the largest crypto funding rounds this month, and who led them?
- Which stablecoin pools pay the highest yield with over $10M TVL?
- What token unlocks are coming up in the next 30 days?
- How big is Uniswap's DAO treasury, and what does it hold?

## Tools

| Tool | What it does |
|---|---|
| `find_projects` | Find projects |
| `project_metrics` | Project metrics |
| `project_tvl_history` | Project TVL history |
| `forks` | Protocol forks |
| `project_community` | Project community growth |
| `rank_projects` | Project rankings |
| `categories` | Project categories |
| `upcoming_projects` | Upcoming crypto projects |
| `upcoming_tges` | Upcoming token launches (TGEs) |
| `project_funding` | Project funding |
| `recent_funding_rounds` | Recent funding rounds |
| `top_investors` | Top investors |
| `investor_profile` | Investor profile |
| `chains` | Chains |
| `chain_metrics` | Chain metrics |
| `fees` | Fees and revenue |
| `fees_history` | Fees and revenue history |
| `chain_fees` | Fees on a chain |
| `volumes` | DEX, options and aggregator volumes |
| `volume_history` | Volume history |
| `token_prices` | Token prices |
| `token_price_history` | Token price history |
| `stablecoins` | Stablecoins |
| `stablecoin_chains` | Stablecoin supply by chain |
| `stablecoin_history` | Stablecoin supply history |
| `treasury_companies` | Treasury companies |
| `yield_pools` | DeFi yield pools |
| `yield_pool` | DeFi yield pool |
| `token_unlocks` | Token unlock calendar |
| `grants` | Crypto grants and hackathons |
| `spaces` | Crypto X Spaces |
| `space` | Crypto X Space transcript |
| `dao_treasuries` | DAO treasuries |
| `dao_treasury_snapshot` | DAO treasuries snapshot |
| `dao_treasury_history` | DAO treasury history |
| `dao_holdings_history` | DAO token holdings history |
| `dao_treasury` | DAO treasury |

The live list, with each tool's inputs, is at https://alphagrowth.io/mcp-server.

## For developers

- [llms.txt](https://alphagrowth.io/llms.txt): a guide to the server and the API for language models
- [OpenAPI](https://alphagrowth.io/openapi.json): the REST API at `/api/v1`, which serves the same data
- [Server card](https://alphagrowth.io/.well-known/mcp/server-card.json)

## Data and privacy

Every tool is read-only and the server is hosted by AlphaGrowth: this repository has no code that runs on your machine, only the server address, the skills and listing files, and it stores nothing locally. Each tool call is an HTTPS request to `alphagrowth.io`, and what the tools return joins your conversation, so it reaches the model provider your client uses.

We log each call to learn how the data is used: the tool and its arguments, the client's name and version, the user agent, the IP address and an approximate location (country, city and postal area, from Cloudflare). After 30 days the arguments and location are deleted and the IP is replaced by a keyed hash; the records are deleted after 180 days. Calls are rate-limited per IP.

[Privacy policy](https://alphagrowth.io/privacy-policy) · [Your privacy choices](https://alphagrowth.io/privacy-choices) · Contact: marketing@alphagrowth.io

## License

The files in this repository are MIT licensed. Use of the server and its data is governed by AlphaGrowth's terms.
