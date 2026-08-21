---
name: querido_diario-mcp
description: Skill da REST API do Querido Diário (municipal) na MCP.AI: 1 endpoint em /api/querido_diario. Busca em diários oficiais MUNICIPAIS de milhares de prefeituras (Querido Diário / Open Knowledge Brasil) por termo ou nome, licitações, nomeações, contratos. Complementa o DJEN (judicial) na esfera municipal. Grátis, sem credencial. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Querido Diário (municipal) — REST API skill

Você tem acesso à **Querido Diário (municipal)** REST API na MCP.AI.

> Busca em diários oficiais MUNICIPAIS de milhares de prefeituras (Querido Diário / Open Knowledge Brasil) por termo ou nome, licitações, nomeações, contratos. Complementa o DJEN (judicial) na esfera municipal. Grátis, sem credencial.

## Base URL

```
https://api.mcp.ai/api/querido_diario
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
curl -X POST https://api.mcp.ai/api/querido_diario/buscar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"termo":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/querido_diario/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `querido_diario_buscar`

Busca em diários oficiais MUNICIPAIS (milhares de prefeituras) por termo/nome — útil pra menções fora do Judiciário: licitações, nomeações, contratos, sanções municipais. _(POST /api/querido_diario/buscar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `termo` | string | Sim | Termo/nome a buscar (ex.: "Fulano de Tal" ou "licitação saúde"). |
| `territory_ids` | string[] | Não | Códigos IBGE de municípios a restringir (vazio = todos). |
| `data_inicio` | string | Não | Publicado desde (AAAA-MM-DD). |
| `data_fim` | string | Não | Publicado até (AAAA-MM-DD). |
| `size` | integer | Não | Resultados (default 10, máx 50). |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_querido_diario` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
