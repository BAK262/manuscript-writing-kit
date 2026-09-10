# Manuscript Writing Kit

Human–agent playbook for LaTeX + BibTeX academic writing: environment, bootstrap, writing contract, multi-pass collaboration, polish, citation (optional Zotero), and literature-table verification.

**Version:** 1.1.1 · [CHANGELOG](CHANGELOG.md) · [License (MIT)](LICENSE)

## Languages / 语言

| Language | Guide |
|----------|--------|
| **简体中文** | [README.zh-CN.md](README.zh-CN.md) |
| **English** | [README.en.md](README.en.md) |

Agent routing entry (machine-facing): [SKILL.md](SKILL.md)

## Quick install

**Recommended: fork**, then clone your fork (keeps a path for upstream updates and for branches that absorb your own lab habits).

```bash
# 1) Fork on GitHub: https://github.com/BAK262/manuscript-writing-kit
# 2) Clone your fork
git clone https://github.com/<YOUR_USER>/manuscript-writing-kit.git
cd manuscript-writing-kit

# 3) Track upstream (optional, for pulling kit updates)
git remote add upstream https://github.com/BAK262/manuscript-writing-kit.git

# 4) Make the pack visible to your agent host (pick one pattern)
#    Cursor / many VS Code–compatible skill hosts — personal skills dir:
#    Windows:  %USERPROFILE%\.cursor\skills\manuscript-writing-kit
#    macOS/Linux: ~/.cursor/skills/manuscript-writing-kit
```

**Windows (PowerShell) — junction into Cursor skills dir:**

```powershell
$src = "C:\path\to\your\fork\manuscript-writing-kit"
$dst = "$env:USERPROFILE\.cursor\skills\manuscript-writing-kit"
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.cursor\skills" | Out-Null
cmd /c mklink /J "$dst" "$src"
```

**macOS / Linux — symlink:**

```bash
mkdir -p ~/.cursor/skills
ln -s /path/to/your/fork/manuscript-writing-kit ~/.cursor/skills/manuscript-writing-kit
```

Other agent products: place or register this folder according to that product’s skill/plugin docs; keep the directory name `manuscript-writing-kit` and the root `SKILL.md`.

## Recommended workstation

Use a code IDE with LaTeX build/preview plugins—**Visual Studio Code or a variant such as Cursor**—plus a TeX distribution (`pdflatex` / `bibtex` or your project’s engine). The kit’s workflows are written for agent chat that can read/edit project files; they are portable across agent hosts that support skill packs or pasted playbooks.

## Start writing

Open the language guide above → follow **Getting started** → load this pack in your agent session → use one template from [prompts/request-templates.md](prompts/request-templates.md).
