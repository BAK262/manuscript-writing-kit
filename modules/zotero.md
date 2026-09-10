# Zotero MCP citation

Query the local Zotero library via MCP for manuscript citations—search, metadata/abstracts, BibTeX export. Used as the **Zotero pool** in [citation.md](citation.md).

## Prerequisites

1. **Zotero 7+** running on the same machine as Cursor.
2. **Local API enabled**: Zotero → Settings → Advanced → allow other apps on this computer (`http://localhost:23119/api/`).
3. **MCP server `zotero`** configured in Cursor (below).

## Setup

### Install (once per Python env)

```powershell
pip install zotero-mcp-lite
```

Entry point: `zotero-mcp serve` ([zotero-mcp-lite](https://pypi.org/project/zotero-mcp-lite/) on PyPI).

### Cursor MCP config

Global: `%USERPROFILE%\.cursor\mcp.json`. Optional project: `.cursor/mcp.json`.

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

Set `command` to the absolute path from `where zotero-mcp` (Windows) or `which zotero-mcp` (Unix). **Restart Cursor** after editing.

### Verify

- `zotero-mcp setup` — Zotero found, Local API working.
- Cursor MCP panel: `zotero` connected.

## MCP tools

Read live schemas before calling. Primary tools:

| Tool | Use |
|------|-----|
| `zotero_search_items` | Keyword / topic search |
| `zotero_get_item_metadata` | Authors, year, abstract, DOI, tags |
| `zotero_get_collections` / `zotero_get_collection_items` | Curated folders |
| `zotero_search_annotations` | PDF highlights vs claims |

**MCP prompt** `bibliography_export(item_keys)` — APA / IEEE / **BibTeX**; prefer when merging into the project master `.bib`.

Optional: `zotero_get_item_fulltext` when abstract is insufficient.

## Workflow integration

Equal weight with master `.bib` and network search in [citation.md](citation.md):

1. Parse sentence or `【cite…】` brief → search terms.
2. `zotero_search_items` (+ collections if brief names a folder).
3. `zotero_get_item_metadata` on shortlist → abstract vs claim.
4. Export BibTeX → temp pack → parent merges with stable keys.
5. Prefer library hits that satisfy the brief; network fills gaps / refreshes metadata.

## Constraints

- Keep Zotero open during MCP calls.
- Skip `zotero_create_note` on citation-only passes unless the user asks.
- Rename exported keys to match project conventions before `\cite{key}`.

## Troubleshooting

| Symptom | Fix |
|---------|-----|
| MCP `zotero` failed | Check `command` path; `pip install -U zotero-mcp-lite` |
| Local API error | Enable setting; restart Zotero |
| Empty search | Broaden query; confirm item is in the library |
