<p align="center">
  <img src="assets/logo.png" alt="Apper" width="96">
</p>

# Apper for Cursor

Build and update complete applications in [Apper](https://apper.io) from Cursor.

Describe what you want, then create, update, publish, and preview it — configure its
database, security and permissions, and add server-side integrations, without setting
up a separate development stack.

## Install

The Apper connector is a remote MCP server. There is nothing to download or run
locally — Cursor connects to it over HTTPS.

**1. Open your Cursor MCP configuration.**

- To make Apper available in every project, edit `~/.cursor/mcp.json`
- To enable it for one project only, create `.cursor/mcp.json` in that project

**2. Add the Apper server:**

```json
{
  "mcpServers": {
    "apper": {
      "type": "http",
      "url": "https://mcp.apper.io/v1/connect"
    }
  }
}
```

If you already have other servers configured, add the `"apper"` entry alongside them
rather than replacing the file.

**3. Restart Cursor**, then open **Settings → MCP** and confirm `apper` is listed.

**4. Sign in.** The first time Apper is used, Cursor opens a browser to sign in to your
Apper account. No API key or client ID is needed — authentication is OAuth 2.0 and is
negotiated automatically.

## Using it

Once connected, ask Cursor's agent in plain language:

> Build a CRM app for my sales team to manage leads, contacts, deals, and tasks.

> Show me the Apper apps in my account.

> Set the dashboard heading in my CRM app to "Sales CRM" and show me the preview.

Apper creates and builds the app, then returns a preview URL — along with login
credentials when the app requires them.

## What you can do

- Search, create, and preview apps and websites
- Read and write project files, and run builds
- Inspect and update the database schema
- Configure row-level security and permissions
- Manage edge functions, environment keys, and secrets

Full tool documentation:
[apper.io/learn/docs/mcp/apper-mcp-connector](https://apper.io/learn/docs/mcp/apper-mcp-connector)

## Troubleshooting

**`apper` does not appear in Settings → MCP.** Check that `mcp.json` is valid JSON —
a trailing comma or missing brace will cause Cursor to skip the file silently. Restart
Cursor after any change.

**The sign-in window does not open.** Make sure your browser is not blocking the popup,
and that your network allows `https://mcp.apper.io`.

**Tools are listed but calls fail.** Your session may have expired. Disable and
re-enable the server in Settings → MCP to sign in again.

## Other clients

- **Claude Code** and the MCP Registry listing — [apperhq/mcp](https://github.com/apperhq/mcp)
- **ChatGPT** — [Apper for ChatGPT](https://apper.io/learn/docs/mcp/apper-for-chatgpt)

## Links

- [Apper](https://apper.io)
- [Documentation](https://apper.io/learn/docs/mcp/apper-mcp-connector)
- [Support](mailto:support@integrately.com)

## License

[Apache 2.0](LICENSE)
