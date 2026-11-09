<img src="logo.png" alt="AlphaGrowth" width="72" />

# AlphaGrowth MCP server

Free crypto data for AI agents. No API key, no sign-up.

Project metrics (TVL, market cap, price, fees, revenue, users), community growth, funding rounds and investors, chains, DeFi yield pools, token unlock calendars and DAO treasuries, from [AlphaGrowth](https://alphagrowth.io). Every result carries a source block to cite.

- **Endpoint:** `https://alphagrowth.io/mcp` (remote, Streamable HTTP, no auth)
- **Tools:** 27, all read-only
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

## License

The files in this repository are MIT licensed. Use of the server and its data is governed by AlphaGrowth's terms.
