# Manuscript Writing Kit (English)

Human-facing guide. Agent router: [SKILL.md](SKILL.md). 中文: [README.zh-CN.md](README.zh-CN.md) · Hub: [README.md](README.md)

**Version:** 1.1.1 · [CHANGELOG](CHANGELOG.md)

## What this is

A reusable **human + agent** playbook (and loadable skill pack) for academic manuscripts:

- Writing environment and compile conventions  
- Scaffold → author-frozen abstract → writing contract  
- Section-wise multi-pass work (structure / language / citations & tables)  
- Optional local bibliography access (Zotero)

Built for **LaTeX + BibTeX**. The paper’s story lives in **your project’s** `WRITING_CONTRACT.md`; this repo ships the framework, blank template, and synthetic examples.

## Recommended setup

| Layer | Recommendation |
|-------|----------------|
| Edit & build | **IDE + extensions**: Visual Studio Code or a variant such as **Cursor**; LaTeX build/preview extensions; a local TeX distribution |
| Chat editing | Any **agent tool** that can read/edit the repo; **load this skill pack** in the session (or reference `SKILL.md` / modules per that product) |
| Where to install | Depends on the agent host; for hosts that use a personal skills directory (e.g. Cursor), see Install below |

Workflows are not tied to one chat product. Paths in modules are project-root relative unless contract §0 says otherwise.

## Install (fork recommended)

**Fork first, then clone your fork**—so you can pull upstream kit updates and keep branches that encode your own lab practice.

1. Fork on GitHub: https://github.com/BAK262/manuscript-writing-kit  
2. Clone your fork:

```bash
git clone https://github.com/<YOUR_USER>/manuscript-writing-kit.git
cd manuscript-writing-kit
git remote add upstream https://github.com/BAK262/manuscript-writing-kit.git
```

3. Pull upstream when you want kit updates:

```bash
git fetch upstream
git merge upstream/main   # or rebase
```

4. Register the folder with your agent host (keep the name `manuscript-writing-kit` and root `SKILL.md`):

**Windows PowerShell (junction into Cursor-style skills dir):**

```powershell
$src = "C:\path\to\your\fork\manuscript-writing-kit"
$dst = "$env:USERPROFILE\.cursor\skills\manuscript-writing-kit"
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.cursor\skills" | Out-Null
cmd /c mklink /J "$dst" "$src"
```

**macOS / Linux:**

```bash
mkdir -p ~/.cursor/skills
ln -s /path/to/your/fork/manuscript-writing-kit ~/.cursor/skills/manuscript-writing-kit
```

Copying the repo into the skills directory also works. For other agent products, follow that product’s skill/plugin registration docs.

## Getting started

1. Load this pack in your agent session (e.g. `/manuscript-writing-kit` in Cursor, or the equivalent in your host).  
2. Mention / attach your main `.tex`.  
3. Paste **one** skeleton from [prompts/request-templates.md](prompts/request-templates.md).

| Situation | Template |
|-----------|----------|
| New paper | New paper bootstrap |
| Draft exists; abstract not yet author-frozen | Small-range **Mode A**; freeze the abstract yourself before contract §1–§4 |
| Abstract frozen; restructure a section | **Mode B** (list edits → you confirm → apply) |
| Abstract frozen; wording only | **Mode A** |
| Citations | Citation pass |
| Argument order feels wrong | Logic-chain reset, then a **second** message for Mode A |

**Minimum before writing passes:** IDE can build a PDF; `manuscript/WRITING_CONTRACT.md` exists with **§0** filled. Configure Zotero (or similar) when you enter a citation pass ([modules/environment.md](modules/environment.md)).

### Modes

| Mode | Meaning | If unsure |
|------|---------|-----------|
| **A** | Wording only; keep each paragraph’s point | **Start here** |
| **B** | May reorder/merge; **list edits and wait for your OK** | |
| **C** | Larger rewrite; scientific meaning changes need your ask | |

### Main path

```text
Environment ready → Scaffold + contract §0 → First draft
  → You freeze the abstract → Contract §1–§4
  → Per section: Mode B (confirm) → Mode A → Cites / tables
  → Pre-submission audit
```

Details: [modules/bootstrap.md](modules/bootstrap.md), [modules/collaboration.md](modules/collaboration.md).

### Glossary

| Term | Meaning |
|------|---------|
| Freeze abstract | You finalize the abstract; body and floats follow it |
| Writing contract | What this paper may claim and how it names things |
| Style anchor | Prose sample for polish (often settled Introduction + prior text) |
| Mode A/B/C | See table above |
| Cite brief | Inline `【cite: …】` with your search constraints |
| Narrative authority | Frozen abstract leads |

### Request example

```text
Weaker: Make Related Work nicer (structure and wording together).
Stronger: Mode B on @main.tex Related Work.
         Style anchor: abstract + Introduction. List structural edits; wait for OK.
```

## Optional companion skills

| Need | Skill you may load | With this pack alone |
|------|--------------------|----------------------|
| Cover / submission letter | e.g. `nature-writing` | Ordinary LaTeX letter |
| Nature-leaning English | e.g. `nature-polishing` | Kit `modules/polish.md` |

## Layout

| Path | Role |
|------|------|
| `SKILL.md` | Agent router (intent → modules) |
| `modules/` | Environment, bootstrap, collaboration, contract, polish, citation, Zotero, table verify, venue |
| `examples/` | Synthetic filled examples |
| `prompts/request-templates.md` | Copy-paste request skeletons |

## Per-paper artifacts

| Artifact | Typical location |
|----------|------------------|
| Main `.tex` | `manuscript/` (or contract §0) |
| Writing contract | `manuscript/WRITING_CONTRACT.md` |
| Frozen abstract | `\begin{abstract}...\end{abstract}` in the main file |

Template: `modules/contract/contract-template.md`.

## Privacy

- Core modules use discoverable paths and config placeholders.  
- `examples/example-contract.md` uses a fictional dataset and ethics ID.  
- Keep personal MCP install paths on your machine.

## License

MIT — [LICENSE](LICENSE)
