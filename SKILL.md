---
name: manuscript-writing-kit
description: >-
  Unified LaTeX manuscript writing pack: environment setup, bootstrap chronology,
  writing contract, human–agent multi-pass collaboration, section polish, citation
  workflow with Zotero, and resource-comparison table verify. Use when starting or
  revising an academic paper in Cursor, freezing narrative after a draft, auditing
  terminology/claims, polishing sections, resolving cite placeholders, or verifying
  literature tables. Triggers on manuscript-writing-kit, writing contract, 写作契约,
  section polish, citation workflow, dataset table verify, Zotero cite.
disable-model-invocation: true
---

# Manuscript Writing Kit

Personal skill pack for LaTeX + BibTeX manuscripts in Cursor. **One entry, load modules by intent.**

Do not improvise from memory of this file alone. **Read the listed module paths** for the current intent before editing the manuscript.

## Project artifacts (per paper)

| Artifact | Typical location |
|----------|------------------|
| Main `.tex` | From user scope or contract §0 |
| Writing contract instance | `manuscript/WRITING_CONTRACT.md` (or header pointer in `.tex`) |
| Master `.bib` | Beside `.tex` or from `\bibliography{}` / `\addbibresource{}` |
| Frozen abstract | `\begin{abstract}...\end{abstract}` in main `.tex` |

Kit supplies framework + template + example. **Paper-specific story lives in the project contract.**

## Routing protocol

1. Detect **intent** (table below). If ambiguous and it changes which modules load, ask in one short question.
2. **Always** for any manuscript edit: read [modules/contract/SKILL.md](modules/contract/SKILL.md) principles; if a project contract exists, read it; read the frozen abstract in the main `.tex`.
3. **Read** every module listed for that intent (full file).
4. State in one line which modules you loaded, then execute.

### Intent → modules

| Intent | Load |
|--------|------|
| New machine / compile / Zotero MCP broken | [modules/environment.md](modules/environment.md) |
| New paper scaffold → first draft → freeze abstract | [modules/bootstrap.md](modules/bootstrap.md), [modules/environment.md](modules/environment.md), [modules/contract/SKILL.md](modules/contract/SKILL.md), [modules/contract/contract-template.md](modules/contract/contract-template.md) |
| Fill or revise writing contract | [modules/contract/SKILL.md](modules/contract/SKILL.md), template; optional [examples/example-contract.md](examples/example-contract.md) |
| How to work section-by-section with the agent | [modules/collaboration.md](modules/collaboration.md), [prompts/request-templates.md](prompts/request-templates.md) |
| Reorganize section (Mode B) or polish prose (Mode A/C) | [modules/collaboration.md](modules/collaboration.md), [modules/polish.md](modules/polish.md), contract instance |
| Citation pass / `【cite:…】` / BibTeX | [modules/citation.md](modules/citation.md), [modules/zotero.md](modules/zotero.md), contract §4 |
| Resource / dataset comparison table verify | [modules/table-verify.md](modules/table-verify.md), contract terminology |
| IEEE Computer Society journal format | [modules/venue/ieee-compsoc-journal.md](modules/venue/ieee-compsoc-journal.md) |
| Cover letter / submission letter | Load companion skill `nature-writing` (and tone tools the user attaches) |
| Deeper Nature-leaning English polish | Load companion skill `nature-polishing` |

## Conflict order (steady-state)

After the abstract is **human-frozen**:

1. Abstract in main `.tex`
2. Project writing contract
3. User style anchor (default: finalized Introduction + already-settled preceding sections)
4. Target draft

## Module index

| Path | Role |
|------|------|
| [modules/environment.md](modules/environment.md) | Cursor, LaTeX build, paths, Zotero MCP |
| [modules/bootstrap.md](modules/bootstrap.md) | Chronology from scaffold to frozen abstract |
| [modules/collaboration.md](modules/collaboration.md) | Multi-pass section protocol, prompt grammar |
| [modules/contract/](modules/contract/) | What the paper may claim and how it names things |
| [modules/polish.md](modules/polish.md) | Modes A/B/C, prose targets, scope lock |
| [modules/citation.md](modules/citation.md) | Per-sentence cite workflow |
| [modules/zotero.md](modules/zotero.md) | Zotero MCP pool |
| [modules/table-verify.md](modules/table-verify.md) | Row-level comparison table verify |
| [modules/venue/ieee-compsoc-journal.md](modules/venue/ieee-compsoc-journal.md) | compsoc / IEEEtran notes |
| [examples/example-contract.md](examples/example-contract.md) | Filled synthetic example only |
| [prompts/request-templates.md](prompts/request-templates.md) | Copy-paste request skeletons |
