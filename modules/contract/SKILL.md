---
name: manuscript-writing-contract
description: >-
  Per-paper writing contract: narrative authority, claim scope, terminology,
  facts SSOT, citation policy. Part of manuscript-writing-kit.
disable-model-invocation: true
---

# Manuscript Writing Contract

A **writing contract** is the SSOT for what a paper may claim and how it may name things. Portable across venues.

**Kit home:** parent [SKILL.md](../../SKILL.md). Blank form: [contract-template.md](contract-template.md). Filled example: [examples/example-contract.md](../../examples/example-contract.md).

## When to use

- Starting a new paper or migrating rules from a prior manuscript
- Drafting/revising abstract, Introduction, Methods, Results, or Discussion
- Auditing terminology drift, claim inflation, or abstract–body mismatch
- Before submission: consistency pass across sections, figures, and tables

## Universal principles

Apply on every paper unless the project contract explicitly overrides.

### 1. Narrative authority

After the author **freezes** the abstract (see [bootstrap.md](../bootstrap.md)), the **abstract** is the highest standard for story, wording, and claim scope.

On conflict: **revise body text** (and figures/tables) to match the abstract, then update the contract.

### 2. Guardrails, not word substitution

Rules preserve **meaning and boundaries**. If a rule makes a sentence harder to read, keep the intent and rewrite simply.

### 3. One design axis, bounded headline

Every paper should state:

- **Primary design axis** — main experimental or conceptual dimension
- **Contribution hierarchy** — first-order vs supporting
- **Non-headline items** — must not become the title claim unless that *is* the paper

**Conceptual framing** may use field-standard terms. **Empirical and modeling claims** must name the concrete signal, behavior, label, prediction variable, metric, or analysis result.

### 4. Terminology layers

| Layer | Role | Example pattern |
|-------|------|-----------------|
| Study / resource | Artifact or experiment name | Dataset X, Study Y |
| Abstract unit | Conceptual condition or task type | Clinic Reference |
| Concrete unit | Implementation in this work | attended PSG night |
| Short form | After first definition in scope | Clinic task |
| Group label | Contrast set spanning units | ambulatory monitoring tasks |

**Experimental hierarchy:** `study/experiment` > `task` > `session` > `block` > `trial` > `stage/phase`

Preparatory segments stay below task level; refer naturally without elevating them to equal-weight tasks.

**Abstract vs concrete** — first mention per major section: `Abstract Name (concrete form)`. Later: short form where unambiguous.

**Resource-level vs instance-level** — paradigm/resource adjectives apply to resources and literature framing; apply to individual tasks/trials only when the contract says so.

### 5. Adjacent terms that change meaning

List pairs readers might conflate (instructed category vs label vs target; self-report vs ground-truth; cohort descriptor vs stratification label; modality-generic vs modality-specific). Keep them distinct in the contract.

**Agency language** — task demands may require production; participants, utterances, or recordings *express* or *carry* content.

### 6. Figures and tables

- Axes/headers: **short abstract names**; abbreviations only per contract.
- Captions: gloss concrete names on **first occurrence in that float** only.

### 7. Paper-specific facts SSOT

Immutable facts: sample size, acquisition parameters, release inventory, access policy. Body must not contradict or quietly extend this list.

Omit from manuscript body (unless venue requires): archive layouts, directory trees, filenames, internal script paths — point to supplement or data docs.

### 8. Citation policy

- Every `\cite{}` supports the **specific claim** at that location.
- Broad framing → reviews or meta-analyses; methods, limitations, dataset facts → primary or technical sources.
- BibTeX: complete metadata per venue; include publisher `abstract` when the project requires it.

## Workflow: new paper (aligned with bootstrap)

Copy [contract-template.md](contract-template.md) to the project, e.g. `manuscript/WRITING_CONTRACT.md`, or a commented pointer at the top of the main `.tex`.

1. **Scaffold** — venue template, §0 metadata (paths, venue, style-anchor field).
2. **Draft body** — provisional story; abstract may still be rough.
3. **Author freezes abstract** — human-owned narrative seed (see [bootstrap.md](../bootstrap.md)).
4. **Fill §1–§4** — story, terminology, facts, citations to match the frozen abstract.
5. **Polish body** — first mention per section follows §2; empirical claims follow §1 and §3; use [collaboration.md](../collaboration.md) + [polish.md](../polish.md).
6. **Pre-submission** — sync abstract, body, and contract; run audit checklist.

**Migrating an existing manuscript:** extract internal writing rules into the contract file; leave a one-line pointer in `.tex`. See the filled example for structure.

## Audit checklist

```
Contract audit:
- [ ] Abstract matches §1 story and §3 facts; claims within results
- [ ] Every coined term in abstract appears in §2 with concrete mapping
- [ ] Task/session/block/trial/stage levels consistent
- [ ] Resource-level adjectives used only as contract allows
- [ ] Figures/tables use §2 short names; captions gloss once
- [ ] No repo paths / filenames / placeholders in submission PDF
- [ ] Citations claim-specific
- [ ] Headline contribution matches §1 hierarchy
```

## Operating modes (agent edits)

| Mode | Allowed |
|------|---------|
| **Language-only** | Wording, grammar, term consistency per contract |
| **Structure-safe** | Language-only + local paragraph merge/split |
| **Contract update** | Revise contract + propagate to abstract/body (scientific meaning needs user approval) |

**Conflict order:** (1) frozen abstract, (2) writing contract, (3) user style anchor, (4) target section draft.

## Companions in this kit

- Polish: [../polish.md](../polish.md)
- Citation: [../citation.md](../citation.md)
- Table verify: [../table-verify.md](../table-verify.md)
