# agromanager-mcp

Connects Claude to the Agromanager MCP server at
`https://mcp.agromanager.eu/mcp`, giving Claude access to Agromanager
tools (projects, employees, invoices, time entries, and more) through the
Model Context Protocol.

## Install

```
/plugin install agromanager-mcp --marketplace agromanager/claude_plugin
```

## Setup

Install this plugin, then run `/mcp` (Claude Code) or open the Connectors
tab (claude.ai / Claude Desktop / Cowork) and sign in with your Agromanager
account. Authentication uses OAuth 2.0 with PKCE against Agromanager's own
identity provider — no API keys or secrets are stored in this plugin.

See the repository root README for full installation instructions.
