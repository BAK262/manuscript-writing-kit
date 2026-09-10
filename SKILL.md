---
name: manuscript-writing-kit
description: >-
  Unified LaTeX manuscript writing pack v1.1: environment, bootstrap, writing
  contract, multi-pass collaboration, polish, citation with Zotero, table verify.
  Use when starting or revising an academic paper in Cursor, freezing narrative
  after a draft, auditing terminology/claims, polishing sections, resolving cite
  placeholders, or verifying literature tables. Triggers on manuscript-writing-kit,
  writing contract, 写作契约, section polish, citation workflow, dataset table verify.
version: 1.1.1
disable-model-invocation: true
---

# Manuscript Writing Kit

**v1.1.1** — LaTeX + BibTeX manuscripts. **One entry; load modules by intent.**

Load this pack in the agent session (attach / `/manuscript-writing-kit` / host-equivalent). Do not improvise from memory. **Read the listed module paths** for the current intent before editing.

Human guides: [README.md](README.md) · [README.zh-CN.md](README.zh-CN.md) · [README.en.md](README.en.md)

## Steady-state daily ritual

1. Confirm this pack is loaded in the session.
2. Read frozen abstract (if frozen) + project `WRITING_CONTRACT` (if present).
3. Detect intent → load modules in the table below (full file for active pass).
4. Reply with one line: modules loaded + mode (A/B/C) + confirm-gate status.
5. Execute.

## Project artifacts (per paper)

| Artifact | Typical location |
|----------|------------------|
| Main `.tex` | User scope or contract §0 |
| Writing contract instance | `manuscript/WRITING_CONTRACT.md` |
| Master `.bib` | Beside `.tex` or `\bibliography{}` / `\addbibresource{}` |
| Frozen abstract | `\begin{abstract}...\end{abstract}` |

Kit = framework + template + examples. **Paper story lives in the project contract.**

## Routing protocol

1. Detect **intent**. If ambiguous and it changes modules, ask one short question.
2. For any manuscript edit: read [modules/contract/module.md](modules/contract/module.md) principles; project contract if present; abstract in main `.tex`.
3. **Read** every module listed for that intent.
4. State modules loaded, then execute.

### Intent → modules

| Intent | Load |
|--------|------|
| New machine / compile / Zotero | [modules/environment.md](modules/environment.md) |
| New paper → freeze abstract | [modules/bootstrap.md](modules/bootstrap.md), [modules/environment.md](modules/environment.md), [modules/contract/module.md](modules/contract/module.md), [modules/contract/contract-template.md](modules/contract/contract-template.md) |
| Fill / revise writing contract | [modules/contract/module.md](modules/contract/module.md), template; optional [examples/example-contract.md](examples/example-contract.md) |
| Section collaboration how-to | [modules/collaboration.md](modules/collaboration.md), [prompts/request-templates.md](prompts/request-templates.md) |
| Reorganize (B) or polish (A/C) | [modules/collaboration.md](modules/collaboration.md), [modules/polish.md](modules/polish.md), project contract |
| Citation / `【cite:…】` | [modules/citation.md](modules/citation.md), [modules/zotero.md](modules/zotero.md), contract §4 |
| Resource comparison table | [modules/table-verify.md](modules/table-verify.md), contract terminology |
| IEEE compsoc journal format | [modules/venue/ieee-compsoc-journal.md](modules/venue/ieee-compsoc-journal.md) |
| Cover / submission letter | Optional companion `nature-writing` (if absent: plain LaTeX letter) |
| Extra Nature-leaning English | Optional companion `nature-polishing` (if absent: kit polish only) |

## Conflict order (steady-state)

After the abstract is **human-frozen**:

1. Abstract in main `.tex`
2. Project writing contract
3. User style anchor (default: finalized Introduction + settled preceding sections)
4. Target draft

**Before freeze:** agent may help scaffold and draft; must **not** fill contract §1–§4 story/contributions as final (see [bootstrap.md](modules/bootstrap.md)).

## Modes (single vocabulary)

| Mode | Also called | Confirm gate |
|------|-------------|--------------|
| **A** | language-only | Not required |
| **B** | structure-safe | **Required** — list edits, wait for OK, then apply |
| **C** | rewrite-with-guardrails | Required for meaning-affecting changes |

Unspecified polish mode → **A**.

## Module index

| Path | Role |
|------|------|
| [modules/environment.md](modules/environment.md) | Cursor, LaTeX, Zotero |
| [modules/bootstrap.md](modules/bootstrap.md) | Chronology + freeze hard gate |
| [modules/collaboration.md](modules/collaboration.md) | Multi-pass + prompt grammar |
| [modules/contract/module.md](modules/contract/module.md) | Claim/naming SSOT framework |
| [modules/polish.md](modules/polish.md) | Prose targets, modes A/B/C |
| [modules/citation.md](modules/citation.md) | Cite workflow + parallelism tiers |
| [modules/zotero.md](modules/zotero.md) | Zotero MCP capabilities |
| [modules/table-verify.md](modules/table-verify.md) | Table row verify |
| [modules/venue/](modules/venue/) | Venue notes |
| [examples/](examples/) | Synthetic examples (`example-contract`, `cite-briefs`, `session-ba`) |
| [prompts/request-templates.md](prompts/request-templates.md) | Request skeletons |
| [CHANGELOG.md](CHANGELOG.md) | Version history |
