# Instalação rápida

SEFAZ DF: ISS é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_sefaz_df_iss`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `SEFAZ DF: ISS` / `https://api.mcp.ai/p_sefaz_df_iss`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "sefaz_df_iss": { "type": "http", "url": "https://api.mcp.ai/p_sefaz_df_iss" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=sefaz_df_iss&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zZWZhel9kZl9pc3MifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "sefaz_df_iss": { "url": "https://api.mcp.ai/p_sefaz_df_iss" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=sefaz_df_iss&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_sefaz_df_iss%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "sefaz_df_iss": { "type": "http", "url": "https://api.mcp.ai/p_sefaz_df_iss" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_sefaz_df_iss
```

Dúvidas? [sefaz_df_iss@mcp.ai](mailto:sefaz_df_iss@mcp.ai)
