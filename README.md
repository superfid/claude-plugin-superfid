# Superfid for Claude

Superfid helps businesses manage inventory faster and more accurately with RFID.

RFID로 재고를 더 빠르고 정확하게 관리할 수 있도록 돕는 서비스입니다.

![Superfid character](assets/character-bg-white-rounded.png)

This Claude plugin bundles:

- A Superfid product and usage skill
- A production remote MCP connector at `https://api.superfid.io/mcp`
- The Superfid character image used for the companion package assets

## Authentication

The connector uses Superfid OAuth with the `workspace:read` scope. No API token is bundled in this package. Users authenticate their own Superfid account when Claude asks to connect.

## Use in Claude

For Claude on the web or Claude Desktop, add the plugin ZIP through the available custom plugin upload flow, then enable the plugin. If the bundled connector is not exposed on the current Claude surface, add the same URL manually under `Customize → Connectors → Add custom connector`:

`https://api.superfid.io/mcp`

For Claude Code, validate and load the plugin locally:

```bash
claude plugin validate /path/to/superfid
claude --plugin-dir /path/to/superfid
```

The connector provides read-only workspace tools. It does not write, scan, delete, or administer Superfid data.
