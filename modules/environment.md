# Environment prerequisites

Checklist for LaTeX manuscripts with this kit. Prefer an **IDE + extensions** (Visual Studio Code or a variant such as Cursor) plus a local TeX distribution. Agent chat may be any host that can read/edit the project and load this pack.

## IDE and build

- [ ] Project opened at the **repository root** (paths in docs are root-relative unless contract §0 says otherwise).
- [ ] LaTeX extension installed (commonly **LaTeX Workshop** or equivalent): build, preview, SyncTeX.
- [ ] TeX distribution on PATH (`pdflatex`, `bibtex` or `biber` as required; `xelatex`/`lualatex` if the project uses them).

## Typical compile loop (pdfLaTeX + BibTeX)

From the directory that holds the main `.tex` (often `manuscript/`):

```text
pdflatex <main>
bibtex <main>
pdflatex <main>
pdflatex <main>
```

Confirm the engine in the manuscript header or project README. IEEE IEEEtran drop-caps often need **pdfLaTeX**.

## Project layout conventions

| Item | Convention |
|------|------------|
| Manuscript tree | `manuscript/` (or path in contract §0) |
| Writing contract | `manuscript/WRITING_CONTRACT.md` or `.tex` header pointer |
| Bibliography | Discover from `\bibliography{}` / `\addbibresource{}` |
| Tables / figures | Often `manuscript/tables/`, `manuscript/figures/` |
| Citation temp | e.g. `manuscript/.citation-workflow/<range-id>/` |
| Table-verify scratch | e.g. `temp/dataset_verify_<slug>.md` |

Use **project-root relative** paths in agent instructions.

## Zotero MCP (citation pool)

Configure when running [citation.md](citation.md) with the Zotero pool. See [zotero.md](zotero.md).

## Skill pack location

- This repository (or a local clone) registered with the agent host.
- For hosts that use a personal skills directory (e.g. `~/.cursor/skills/manuscript-writing-kit/`), see [README.md](../README.md).
- Per-paper contract instance lives in the project.
