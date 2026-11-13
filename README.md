# CatchMyCall plugin for Cursor

Connects Cursor to [CatchMyCall](https://app.catchmycall.ai) through its hosted MCP server,
`https://mcp.catchmycall.ai/mcp`. This repository holds only the plugin manifest; the server is
operated by Teeoff Technologies Private Limited.

## What it can do

Read call records, contacts, leads, campaigns, templates and billing for your organisation, and,
with the permissions you grant, place a call, send a WhatsApp message, and create or update
contacts, leads and campaigns. Write tools describe what they will do and ask you to confirm first.

## Signing in

The first time Cursor uses the server it opens a CatchMyCall sign-in page. You approve exactly
which permissions Cursor gets, for the organisation selected in the portal. No password ever
reaches Cursor or the MCP server.

## Without the plugin

Add this to `~/.cursor/mcp.json`:

```json
{ "mcpServers": { "catchmycall": { "url": "https://mcp.catchmycall.ai/mcp" } } }
```

## Links

- Documentation: https://app.catchmycall.ai/docs/connector
- Privacy policy: https://app.catchmycall.ai/privacy
- Terms: https://app.catchmycall.ai/terms
- Support: support@catchmycall.ai
- MCP Registry: `ai.catchmycall/cpaas`
