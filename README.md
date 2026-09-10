# Manuscript Writing Kit

Cursor Agent skill pack for LaTeX + BibTeX academic manuscripts: environment checklist, bootstrap chronology, writing contract, human–agent multi-pass collaboration, section polish, citation workflow (with Zotero MCP), and resource-comparison table verification.

**Version:** 1.1.0 · [CHANGELOG](CHANGELOG.md)

## Monday morning (do this first)

This skill has `disable-model-invocation: true`. **You must attach it** (`/manuscript-writing-kit`) or the agent will not load the kit.

1. Install (clone or copy) into `~/.cursor/skills/manuscript-writing-kit/`.
2. Open chat; type `/manuscript-writing-kit` (or attach the skill).
3. `@` your main `.tex`.
4. Paste **one** template from [prompts/request-templates.md](prompts/request-templates.md):

| Your situation | Paste |
|----------------|--------|
| Brand-new paper | **New paper bootstrap** |
| Have a draft; abstract not frozen yet | Keep drafting; use **Mode A** only on small ranges; freeze abstract yourself before filling contract §1–§4 |
| Abstract frozen; reorganize a section | **Mode B** (agent lists edits → you confirm → apply) |
| Abstract frozen; wording only | **Mode A** |
| Add / fix cites | **Citation pass** |
| Afraid the story drifted | **Logic-chain reset** (then Mode A in a **second** message) |

**Minimum setup before writing passes:** Cursor + PDF compiles + `manuscript/WRITING_CONTRACT.md` with **§0** filled. Configure Zotero MCP only when you start a citation pass ([modules/environment.md](modules/environment.md)).

### Modes in three lines

| Mode | Meaning | Default if unsure |
|------|---------|-------------------|
| **A** | Wording only; keep each paragraph’s main point | **Use this** |
| **B** | May reorder/merge paragraphs; **MUST list edits and wait for your OK** | |
| **C** | Larger rewrite under guardrails; meaning changes need your ask | |

### Main path (bootstrap → steady-state)

```text
Environment → Scaffold + contract §0 → First draft
  → You freeze abstract → Contract §1–§4
  → Per section: Mode B (confirm) → Mode A → Citation / tables
  → Pre-submission audit
```

Detail: [modules/bootstrap.md](modules/bootstrap.md), [modules/collaboration.md](modules/collaboration.md).

### Glossary (EN → 含义)

| Term | Meaning |
|------|---------|
| Freeze abstract | 你亲自定稿摘要；之后正文跟摘要走 |
| Writing contract | 本篇可说什么、怎么命名的 SSOT（`WRITING_CONTRACT.md`） |
| Style anchor | 润色时对齐的文风样本（通常已定稿 Introduction + 前文） |
| Mode A / B / C | 见上表 |
| Cite brief | 正文里 `【cite: …】`，作者给检索约束，agent 不得擅自改宽/改窄 |
| Narrative authority | 冻结后的摘要说了算 |

### Bad → better request

```text
Bad:  把 Related Work 改好看一点（结构和用词一起改）。
Better: /manuscript-writing-kit Mode B on @main.tex Related Work.
        Style anchor: abstract + Introduction. First list edits; wait for OK.
```

## Install

```text
~/.cursor/skills/manuscript-writing-kit/
```

Folder name must match; root `SKILL.md` at that path. Repo: https://github.com/BAK262/manuscript-writing-kit

## Companion skills (optional)

| Need | Skill | If missing |
|------|--------|------------|
| Cover / submission letter | `nature-writing` (+ tone tools you attach) | Draft letter in plain LaTeX without that skill |
| Extra Nature-leaning English | `nature-polishing` | Stay on kit `modules/polish.md` |

## Layout

| Path | Role |
|------|------|
| `SKILL.md` | Router — intent → modules |
| `modules/environment.md` | Cursor, LaTeX, paths, Zotero MCP |
| `modules/bootstrap.md` | Scaffold → draft → freeze abstract → contract |
| `modules/collaboration.md` | Multi-pass protocol, prompt grammar |
| `modules/contract/` | Contract framework + blank template |
| `modules/polish.md` | Modes A/B/C |
| `modules/citation.md` | Per-sentence citation |
| `modules/zotero.md` | Zotero MCP pool |
| `modules/table-verify.md` | Comparison-table verify |
| `modules/venue/` | Optional venue notes |
| `examples/` | Synthetic filled examples |
| `prompts/request-templates.md` | Copy-paste skeletons |

## Per-paper artifacts

| Artifact | Typical location |
|----------|------------------|
| Main `.tex` | `manuscript/` (or contract §0) |
| Writing contract | `manuscript/WRITING_CONTRACT.md` |
| Frozen abstract | `\begin{abstract}...\end{abstract}` |

Copy `modules/contract/contract-template.md` into the project. Use `examples/` as structure reference only.

## Privacy

- Core modules use discoverable paths and config placeholders.
- `examples/example-contract.md` is synthetic (fictional dataset / ethics ID).
- Never commit a filled personal `mcp.json`.

## License

MIT — see [LICENSE](LICENSE).
