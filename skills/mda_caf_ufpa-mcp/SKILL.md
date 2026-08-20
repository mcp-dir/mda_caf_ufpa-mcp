---
name: mda_caf_ufpa-mcp
description: Skill da REST API do MDA CAF: Unidade Familiar de Produção Agrária (UFPA) na MCP.AI: 1 endpoint em /api/mda_caf_ufpa. MDA CAF: Unidade Familiar de Produção Agrária (UFPA), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# MDA CAF: Unidade Familiar de Produção Agrária (UFPA) — REST API skill

Você tem acesso à **MDA CAF: Unidade Familiar de Produção Agrária (UFPA)** REST API na MCP.AI.

> MDA CAF: Unidade Familiar de Produção Agrária (UFPA), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/mda_caf_ufpa
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/mda_caf_ufpa/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"cpf":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/mda_caf_ufpa/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `mda_caf_ufpa_consultar`

MDA CAF: Unidade Familiar de Produção Agrária (UFPA), consulta em fonte oficial. _(POST /api/mda_caf_ufpa/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf` | string | Sim | Parâmetro de consulta "cpf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_mda_caf_ufpa` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
