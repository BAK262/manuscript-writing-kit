# Manuscript Writing Kit

Cursor Agent skill pack for LaTeX + BibTeX academic manuscripts: environment checklist, bootstrap chronology, writing contract, human–agent multi-pass collaboration, section polish, citation workflow (with Zotero MCP), and resource-comparison table verification.

## Install

Copy or clone this repository into your Cursor personal skills directory:

```text
~/.cursor/skills/manuscript-writing-kit/
```

The folder name must match; `SKILL.md` must sit at that path.

In chat, attach or invoke: `/manuscript-writing-kit`

## Layout

| Path | Role |
|------|------|
| `SKILL.md` | Router — maps intent → modules to load |
| `modules/environment.md` | Cursor, LaTeX build, paths, Zotero MCP |
| `modules/bootstrap.md` | Scaffold → draft → freeze abstract → contract |
| `modules/collaboration.md` | Multi-pass section protocol, prompt grammar |
| `modules/contract/` | Writing-contract framework + blank template |
| `modules/polish.md` | Modes A/B/C prose polish |
| `modules/citation.md` | Per-sentence citation workflow |
| `modules/zotero.md` | Zotero MCP pool setup |
| `modules/table-verify.md` | Comparison-table row verification |
| `modules/venue/` | Optional venue notes (e.g. IEEE compsoc) |
| `examples/` | Filled contract examples (reference only) |
| `prompts/request-templates.md` | Copy-paste request skeletons |

## Per-paper artifacts

| Artifact | Typical location |
|----------|------------------|
| Main `.tex` | Project `manuscript/` (or path in contract §0) |
| Writing contract instance | `manuscript/WRITING_CONTRACT.md` |
| Frozen abstract | `\begin{abstract}...\end{abstract}` in main `.tex` |

Copy `modules/contract/contract-template.md` into the project and fill it. Use `examples/` only as structure reference.

## Privacy / redistribution

- Kit **core modules** use discoverable paths and config placeholders (no machine-specific absolute paths).
- `examples/example-contract.md` is a **synthetic** filled instance (fictional dataset and ethics ID).
- Keep MCP `command` paths local; never commit a filled `mcp.json` with personal install paths.

## License

MIT — see [LICENSE](LICENSE).
