# Installing Postmately MCP

Postmately is a remote MCP server (Streamable HTTP). Nothing to install or build.

- URL: `https://api.postmately.com/mcp`
- Auth: OAuth 2.1 (discovery at `https://api.postmately.com/.well-known/oauth-protected-resource/mcp`, dynamic client
  registration and Client ID Metadata Documents supported). Clients without OAuth can send an API key from Postmately
  Settings, API as `Authorization: Bearer <key>`.

Example config:

```json
{
  "mcpServers": {
    "postmately": { "type": "streamableHttp", "url": "https://api.postmately.com/mcp" }
  }
}
```

After connecting, call `list_channels` to see the user's connected social channels and `get_credits` for the balance.
Every post should be created as a draft (`create_post` with `when: "draft"`) until the user approves it.
