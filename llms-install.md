# Installing the CatchMyCall MCP server

CatchMyCall is a **hosted remote MCP server**. There is nothing to download, build or run locally.

- Endpoint: `https://mcp.catchmycall.ai/mcp`
- Transport: streamable HTTP
- Authentication: OAuth 2.1 (PKCE, dynamic client registration). No API key.

## Steps

1. Add the server to the MCP client's configuration as a remote (URL) server:

   ```json
   {
     "mcpServers": {
       "catchmycall": {
         "url": "https://mcp.catchmycall.ai/mcp"
       }
     }
   }
   ```

   Clients that need an explicit transport type should use `"type": "streamableHttp"` (or `"http"`) with the same URL.

2. On first use the client receives `401` with a `WWW-Authenticate` header pointing at
   `https://mcp.catchmycall.ai/.well-known/oauth-protected-resource`, registers itself, and opens the
   CatchMyCall sign-in page in the browser. The user signs in there and approves the permissions; nothing
   needs to be pasted back.

3. After approval the tools appear (calls, WhatsApp, contacts, leads, campaigns, billing). Tools that
   change something describe the action and ask the user to confirm first.

## Requirements

- A CatchMyCall account: https://app.catchmycall.ai
- Docs: https://app.catchmycall.ai/docs/connector · Support: support@catchmycall.ai
