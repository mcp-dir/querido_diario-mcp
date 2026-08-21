# Querido Diário (municipal)

### Querido Diário (municipal) for Claude, ChatGPT and AI agents

Searches MUNICIPAL official gazettes from thousands of city halls (Querido Diário / Open Knowledge Brasil) by term or name, procurements, appointments, contracts. Complements DJEN (judicial) at the municipal level. Free, no credentials.

- 📊 **1 tool**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Querido Diário (municipal)`, URL `https://api.mcp.ai/p_querido_diario`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=querido_diario&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9xdWVyaWRvX2RpYXJpbyJ9)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=querido_diario&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_querido_diario%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_querido_diario
```

---

## 1 tool

| Tool | Description |
|---|---|
| `querido_diario_buscar` | Busca em diários oficiais MUNICIPAIS (milhares de prefeituras) por termo/nome — útil pra menções fora do Judiciário: licitações, nomeações, contratos, sanções municipais. |

---

## Pricing

Free.

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_querido_diario` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
