# Installing the AlphaGrowth MCP server

AlphaGrowth is a hosted, remote MCP server. There is nothing to clone, build or run, and no API key.

Add this entry to the client's MCP settings (for Cline, `cline_mcp_settings.json`):

```json
{
  "mcpServers": {
    "alphagrowth": {
      "type": "streamableHttp",
      "url": "https://alphagrowth.io/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

Then check it works by calling the `find_projects` tool with `{"query": "uniswap"}`; it returns matching projects and their slugs.

All tools are read-only. Calls are rate-limited per IP address.
