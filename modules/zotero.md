# Zotero MCP citation

Zotero **pool** for [citation.md](citation.md). Discover tools from the live MCP schema; do not assume fixed names if the server differs.

## Prerequisites

1. Zotero 7+ running.  
2. Local API enabled (`http://localhost:23119/api/`).  
3. Cursor MCP server `zotero` configured.

## Setup

```powershell
pip install zotero-mcp-lite
```

MCP config (`%USERPROFILE%\.cursor\mcp.json` or project `.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "zotero": {
      "command": "PATH_FROM_where_zotero-mcp",
      "args": ["serve"],
      "env": {}
    }
  }
}
```

Resolve `command` via `where zotero-mcp` / `which zotero-mcp`. Restart Cursor. Verify with `zotero-mcp setup` and a green MCP panel.

## Capabilities required (map to live tools)

| Capability | Typical tools (examples — confirm schema) |
|------------|-------------------------------------------|
| Search library | e.g. `zotero_search_items` |
| Read metadata / abstract | e.g. `zotero_get_item_metadata` |
| Browse collections | e.g. `zotero_get_collections` / `…_items` |
| Export BibTeX | e.g. `bibliography_export` prompt or export tool |
| Optional full text | only if abstract insufficient |

**If schema lacks a capability:** skip that action, use `.bib` + network pools, and state the gap in the citation report. **Do not invent tool names.**

## Workflow integration

1. Parse sentence / `【cite…】` → search terms.  
2. Search → metadata shortlist → abstract vs claim.  
3. Export BibTeX → temp → parent merges with stable keys.  
4. Prefer library hits that satisfy the brief.

## Constraints

- Keep Zotero open during calls.  
- Skip note-creation on citation-only passes unless asked.  
- Rename keys to project conventions before `\cite{}`.

## Troubleshooting

MCP fail → path / reinstall · Local API error → enable setting, restart Zotero · Empty search → broaden query.
