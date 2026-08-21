# Querido Diário (municipal)

### Querido Diário (municipal) para Claude, ChatGPT e agentes de IA

Busca em diários oficiais MUNICIPAIS de milhares de prefeituras (Querido Diário / Open Knowledge Brasil) por termo ou nome, licitações, nomeações, contratos. Complementa o DJEN (judicial) na esfera municipal. Grátis, sem credencial.

- 📊 **1 ferramenta**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `Querido Diário (municipal)` e **URL** `https://api.mcp.ai/p_querido_diario`.

### Cursor

[➕ Instalar Querido Diário (municipal) no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=querido_diario&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9xdWVyaWRvX2RpYXJpbyJ9)

### VS Code (Copilot Chat)

[➕ Instalar Querido Diário (municipal) no VS Code](vscode:mcp/install?name=querido_diario&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_querido_diario%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_querido_diario
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Busque "Fulano de Tal" nos diários municipais
Menções a licitação de saúde nos diários municipais recentes
Esse nome aparece em algum diário de prefeitura?
```

---

## 1 ferramenta disponível

| Tool | Descrição |
|---|---|
| `querido_diario_buscar` | Busca em diários oficiais MUNICIPAIS (milhares de prefeituras) por termo/nome — útil pra menções fora do Judiciário: licitações, nomeações, contratos, sanções municipais. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: Open Knowledge Brasil — Querido Diário, o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_querido_diario`.


---

## Suporte

- 📧 [querido_diario@mcp.ai](mailto:querido_diario@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/querido_diario-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_querido_diario` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
