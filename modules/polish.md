# Manuscript polish

Process + scholarly prose targets. **Content rules** live in the project writing contract and frozen abstract.

**Kit:** [../SKILL.md](../SKILL.md) · Contract: [contract/SKILL.md](contract/SKILL.md) · Collaboration: [collaboration.md](collaboration.md)

## Division of labor

| Concern | Owner |
|---------|--------|
| Story, terms, facts, cite policy | Project `WRITING_CONTRACT` + [contract/SKILL.md](contract/SKILL.md) |
| Narrative authority | Frozen `\begin{abstract}...\end{abstract}` in main `.tex` (path from contract §0 / user scope) |
| Modes, scope lock, style anchor, prose targets | **This module** |
| Per-sentence cites / BibTeX | [citation.md](citation.md) |
| Resource comparison tables | [table-verify.md](table-verify.md) |

Every run: read frozen abstract + project contract (and kit contract principles). Conflict → abstract, then contract.

## When to use

- Edit the main manuscript or companion tables/appendix for the same paper.
- Tighten prose to contract + venue register.
- Section- or range-level refine; structural change only in Mode B/C.

## Operating modes

Unspecified → **Mode A**.

| Mode | Allowed |
|------|---------|
| **A — language-only** | Wording, grammar, rhythm, connectors, term consistency per contract, register, local redundancy cuts |
| **B — structure-safe** | Mode A + local paragraph merge/split; sentence reorder for coherence (confirm gate recommended) |
| **C — rewrite-with-guardrails** | Larger rewrite for clarity/compliance; scientific meaning changes need user request; report major rewrites |

Mode A keeps claim polarity/strength, section order, paragraph roles, and claim–citation binding (rebind only on factual mismatch).

## Scope lock

- Keep section/subsection order and each paragraph’s narrative role (unless Mode B/C + user OK).
- Leave `【待补充】` / `【待扩写】` unless the user asks to fill.
- Prose vs contract → **contract wins**; flag trade-offs.

## Source hierarchy

1. Frozen abstract in main `.tex`
2. Project writing contract
3. User **style anchor** (default: finalized Introduction + settled preceding sections)
4. Target draft

## Prose targets

Match the style anchor: scholarly venue-neutral diction, evidence-forward cadence.

- **Formal register:** precise quantifiers and method nouns; skip fillers, vague hype, idioms, rhetorical questions, chatty asides. Mirror anchor *we* / impersonal balance.
- **Concision:** one idea per sentence; cut pleonasm and synonym stacks; skip restating claims already licensed by backward reference.
- **Academic cadence:** declarative; hedge where contract/anchor require; vary openings; standard section moves; lean verbs over stacked nominalizations.
- **Controlled repetition:** for precision or licensed backward ref only.
- **Logical connectors:** only where the argument needs them.
- **Spelling / LaTeX / punctuation:** fix and list in the reply.
- **Ambiguity:** rewrite dual readings; if intent unclear, propose two candidates.

## Citation touch during polish

- Mode A: no move/add/remove `\cite{}` unless factual mismatch.
- Full cite audit → [citation.md](citation.md).

## Claim alignment

Empirical and baseline prose must match contract §1/§3 and any analysis workflows the manuscript cites (discover names from the project, e.g. validation entry points). Treat documented baselines as **reuse entry points** unless the contract headlines a full benchmark study.

## Execution checklist

1. Resolve main `.tex` + contract paths; read abstract + contract.
2. Confirm mode (default A) + style anchor.
3. Audit target vs contract (terminology, claims, facts, body omits repo paths).
4. Prose pass per targets.
5. Edit within mode + scope lock.
6. Report structural or compliance-driven edits.
