# Environment prerequisites

Checklist for writing LaTeX manuscripts with this kit in **Cursor** (VS Code–compatible).

## IDE

- [ ] Cursor installed; project opened at the **repository / dataset root** (paths in docs and skills are root-relative).
- [ ] LaTeX extension installed (commonly **LaTeX Workshop** or equivalent): build, preview, SyncTeX jump.
- [ ] TeX distribution on PATH (`pdflatex`, `bibtex` or `biber` as the project requires; `xelatex`/`lualatex` if the project uses them).

## Typical compile loop (pdfLaTeX + BibTeX)

From the directory that holds the main `.tex` (often `manuscript/`):

```text
pdflatex <main>
bibtex <main>
pdflatex <main>
pdflatex <main>
```

Confirm the project’s actual engine in the manuscript header or README. IEEE IEEEtran drop-caps often need **pdfLaTeX**.

## Project layout conventions

| Item | Convention |
|------|------------|
| Manuscript tree | `manuscript/` (or path in contract §0) |
| Writing contract | `manuscript/WRITING_CONTRACT.md` or `.tex` header pointer |
| Bibliography | Discover from `\bibliography{}` / `\addbibresource{}` |
| Tables / figures | Often `manuscript/tables/`, `manuscript/figures/` |
| Citation temp | e.g. `manuscript/.citation-workflow/<range-id>/` |
| Table-verify scratch | e.g. `temp/dataset_verify_<slug>.md` |

Use **project-root relative** paths in agent instructions. Discover absolute paths only at runtime on the local machine.

## Zotero MCP (citation pool)

Required when running [citation.md](citation.md) with the Zotero pool.

1. Zotero 7+ running; **Local API** enabled: Settings → Advanced → allow other apps (`http://localhost:23119/api/`).
2. Install CLI once: `pip install zotero-mcp-lite` (entry: `zotero-mcp serve`).
3. Cursor MCP config (`%USERPROFILE%\.cursor\mcp.json` or project `.cursor/mcp.json`):

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

Resolve `command` with `where zotero-mcp` (Windows) or `which zotero-mcp` (Unix). Restart Cursor after edits.

4. Verify: `zotero-mcp setup`; MCP panel shows `zotero` connected. Details: [zotero.md](zotero.md).

## Agent skills

- This pack: `~/.cursor/skills/manuscript-writing-kit/`
- Per-paper contract instance in the project (not only the kit template)
