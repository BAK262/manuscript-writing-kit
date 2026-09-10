# Manuscript Writing Kit

[![English](https://img.shields.io/badge/lang-English-0b57d0)](README.md)
[![简体中文](https://img.shields.io/badge/lang-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-c41e3a)](README_zh.md)

Skill pack and playbook for LaTeX + BibTeX academic writing with a coding agent: environment, bootstrap, writing contract, multi-pass section work, polish, citation (optional Zotero), and literature-table checks.

**Version:** 1.1.2 · [CHANGELOG](CHANGELOG.md) · [License](LICENSE) · Agent entry: [SKILL.md](SKILL.md)

## Install

```bash
git clone https://github.com/BAK262/manuscript-writing-kit.git
cd manuscript-writing-kit
```

Register the folder with your agent host. Keep the directory name `manuscript-writing-kit` and the root file `SKILL.md`.

**Cursor-style personal skills directory — Windows (PowerShell):**

```powershell
$src = "C:\path\to\manuscript-writing-kit"   # your clone path
$dst = "$env:USERPROFILE\.cursor\skills\manuscript-writing-kit"
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.cursor\skills" | Out-Null
cmd /c mklink /J "$dst" "$src"
```

**macOS / Linux:**

```bash
mkdir -p ~/.cursor/skills
ln -s /path/to/manuscript-writing-kit ~/.cursor/skills/manuscript-writing-kit
```

Copying the clone into the skills directory works the same way. For other agent products, follow that product’s skill or plugin docs.

Updates:

```bash
cd /path/to/manuscript-writing-kit
git pull
```

## Workstation

| Layer | Suggestion |
|-------|------------|
| Edit & build | IDE + extensions: **Visual Studio Code** or a variant such as **Cursor**; LaTeX build/preview extension; local TeX (`pdflatex` / `bibtex` or your project engine) |
| Chat editing | Any agent that can read and edit the project; load this pack in the session (e.g. `/manuscript-writing-kit`, or your host’s equivalent) |

Paths in the modules are project-root relative unless contract §0 says otherwise.

## Getting started

1. Load this pack in the agent session.  
2. Point the agent at your main `.tex`.  
3. Paste **one** template from [prompts/request-templates.md](prompts/request-templates.md).

| Situation | Template |
|-----------|----------|
| New paper | New paper bootstrap |
| Draft in progress; abstract still provisional | Small-range **Mode A**; freeze the abstract yourself, then fill contract §1–§4 |
| Abstract frozen; restructure a section | **Mode B** (list edits → confirm → apply) |
| Abstract frozen; wording only | **Mode A** |
| Citations | Citation pass |
| Local argument feels off | Logic-chain reset, then a second message for Mode A |

Before writing passes: the IDE builds a PDF; `manuscript/WRITING_CONTRACT.md` exists with **§0** filled. Set up Zotero when you start a citation pass ([modules/environment.md](modules/environment.md)).

### Modes

| Mode | Meaning | Default |
|------|---------|---------|
| **A** | Wording only; keep each paragraph’s point | Prefer this when unsure |
| **B** | May reorder or merge; list edits and wait for confirmation | |
| **C** | Larger rewrite; ask explicitly before changing scientific meaning | |

### Main path

```text
Environment → Scaffold + contract §0 → First draft
  → Freeze abstract → Contract §1–§4
  → Per section: Mode B (confirm) → Mode A → Cites / tables
  → Pre-submission audit
```

Details: [modules/bootstrap.md](modules/bootstrap.md), [modules/collaboration.md](modules/collaboration.md).

### Glossary

| Term | Meaning |
|------|---------|
| Freeze abstract | You finalize the abstract; body and floats follow it |
| Writing contract | What this paper may claim and how it names things (`WRITING_CONTRACT.md`) |
| Style anchor | Prose sample for polish (often settled Introduction + earlier text) |
| Mode A / B / C | See above |
| Cite brief | Inline `【cite: …】` with your search constraints |
| Narrative authority | The frozen abstract leads |

### Example request

```text
Mode B on @main.tex Related Work.
Style anchor: abstract + Introduction.
List structural edits first; apply after confirmation.
```

## Optional companions

| Need | You may also load | Or stay in this pack |
|------|-------------------|----------------------|
| Cover / submission letter | e.g. `nature-writing` | Write the letter in LaTeX |
| Nature-leaning English | e.g. `nature-polishing` | [modules/polish.md](modules/polish.md) |

## Layout

| Path | Role |
|------|------|
| `SKILL.md` | Agent router (intent → modules) |
| `modules/` | Environment, bootstrap, collaboration, contract, polish, citation, Zotero, table verify, venue |
| `examples/` | Synthetic filled examples |
| `prompts/request-templates.md` | Request skeletons |

## Files in your paper project

| Artifact | Typical location |
|----------|------------------|
| Main `.tex` | `manuscript/` (or contract §0) |
| Writing contract | `manuscript/WRITING_CONTRACT.md` |
| Frozen abstract | `\begin{abstract}...\end{abstract}` |

Blank template: [modules/contract/contract-template.md](modules/contract/contract-template.md).  
Filled illustration: [examples/example-contract.md](examples/example-contract.md) (synthetic names and ethics ID).
