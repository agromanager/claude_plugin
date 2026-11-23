# Agromanager Claude plugins

Marketplace-repo met de Claude plugin die verbinding maakt met de
Agromanager MCP-server (`https://mcp.agromanager.eu/mcp`).

## Vereisten (eenmalig, serverkant)

Bij de OAuth-provider (`sso.agromanager.eu`) moet een publieke
OAuth-client `claude-plugin-prod` geregistreerd staan met:

- Grant types: `authorization_code`, `refresh_token`
- Response types: `code`
- PKCE (S256) verplicht, geen client secret
- Redirect URI's:
  - `http://localhost:8080/callback` (Claude Code)
  - `https://claude.ai/api/mcp/auth_callback` (claude.ai / Desktop / Cowork)
- Scopes: `openid profile email am_environments`

## Installeren — Claude Code

```
/plugin marketplace add agromanager/claude_plugin
/plugin install agromanager-mcp@agromanager-plugins
```

Of lokaal, vóór publicatie op GitHub:

```
/plugin marketplace add ./claude_plugin
/plugin install agromanager-mcp@agromanager-plugins
```

Na installatie: `/mcp` uitvoeren om in te loggen en de beschikbare tools te
zien.

## Installeren — claude.ai / Claude Desktop / Cowork

1. Customize → Plugins → deze marketplace toevoegen (`https://github.com/agromanager/claude_plugin`)
2. Plugin `agromanager-mcp` installeren
3. Op het Connectors-tabblad verschijnt de Agromanager-server; daar inloggen

## Valideren tijdens ontwikkeling

```
claude plugin validate ./plugins/agromanager-mcp
```
