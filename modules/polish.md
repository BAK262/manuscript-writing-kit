# Manuscript polish

Process + scholarly prose targets. **Content rules** = project writing contract + frozen abstract.

**Kit:** [../SKILL.md](../SKILL.md) · [contract/module.md](contract/module.md) · [collaboration.md](collaboration.md)

## Division of labor

| Concern | Owner |
|---------|--------|
| Story, terms, facts, cite policy | Project `WRITING_CONTRACT` + contract module |
| Narrative authority | Frozen abstract in main `.tex` |
| Modes, scope lock, style anchor, prose | **This module** |
| Cites / tables | [citation.md](citation.md) / [table-verify.md](table-verify.md) |

Every run: read frozen abstract + project contract. Conflict → abstract, then contract.

## Operating modes

Unspecified → **Mode A**.

| Mode | Allowed | Confirm gate |
|------|---------|--------------|
| **A — language-only** | Wording, grammar, rhythm, connectors, term consistency, register, local redundancy | Not required |
| **B — structure-safe** | Mode A + local paragraph merge/split; sentence reorder for coherence | **Required:** list proposed edits → wait for user OK → then apply |
| **C — rewrite-with-guardrails** | Larger rewrite for clarity/compliance | Meaning changes need user request; report major rewrites; confirm before applying |

Mode A keeps claim polarity/strength, section order, paragraph roles, and claim–citation binding (rebind only on factual mismatch).

## Scope lock

- Keep section/subsection order and paragraph roles unless Mode B/C **after** confirmation.
- Leave `【待补充】` / `【待扩写】` unless user asks to fill.
- Prose vs contract → **contract wins**; flag trade-offs.

## Source hierarchy

1. Frozen abstract  
2. Project writing contract  
3. Style anchor (default: Introduction + settled preceding sections)  
4. Target draft  

## Prose targets

Scholarly venue-neutral diction; evidence-forward cadence; formal register; concision; lean verbs; controlled repetition; connectors only when needed; fix spelling/LaTeX/punctuation and list them; resolve dual readings or propose two candidates.

## Citation touch during polish

- Mode A: no move/add/remove `\cite{}` unless factual mismatch.
- Full cite audit → [citation.md](citation.md).

## Claim alignment

Empirical and baseline prose must match contract §1/§3. Discover analysis or result names **from the project contract and manuscript**—do not assume a fixed workflow basename. Treat documented baselines as reuse entry points unless the contract headlines a full benchmark study.

## Execution checklist

1. Resolve paths; read abstract + contract.  
2. Confirm mode (default A) + style anchor.  
3. If Mode B or C: **output proposed edits and stop until user confirms** (unless user already approved a listed plan in-thread).  
4. Audit target vs contract.  
5. Apply prose within mode + scope lock.  
6. Report structural or compliance-driven edits.
