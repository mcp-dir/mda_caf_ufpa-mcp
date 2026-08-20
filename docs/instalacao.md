# Instalação detalhada

MDA CAF: Unidade Familiar de Produção Agrária (UFPA) é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_mda_caf_ufpa`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_mda_caf_ufpa` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_mda_caf_ufpa` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_mda_caf_ufpa` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.mda_caf_ufpa` (ou `servers.mda_caf_ufpa` no VS Code) do config do cliente e reinicie.
