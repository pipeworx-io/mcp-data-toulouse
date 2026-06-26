# mcp-data-toulouse

Toulouse Métropole Open Data (data.toulouse-metropole.fr) — OpenDataSoft MCP.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 1118+ live data sources.

## Tools

| Tool | Description |
|------|-------------|
| `search_datasets` | Search Toulouse Métropole Open Data for datasets by keyword (mobility, urban services, culture & environment). Returns dataset_ids (pass to query/dataset_info), titles, themes and record counts. |
| `dataset_info` | Get metadata for one Toulouse Métropole Open Data dataset (fields/schema, themes, record count) — call before query to learn the column names. |
| `query` | Query records from a Toulouse Métropole Open Data dataset with ODSQL. Filter (where), aggregate (group_by/select), sort (order_by), paginate (limit/offset). |

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "data-toulouse": {
      "url": "https://gateway.pipeworx.io/data-toulouse/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 1118+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Data Toulouse data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [All tools and guides](https://github.com/pipeworx-io/examples)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
