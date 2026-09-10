# Manuscript Writing Contract

Kit **module** (not a standalone Cursor skill). SSOT framework for what a paper may claim and how it may name things.

**Kit home:** [../../SKILL.md](../../SKILL.md) · Template: [contract-template.md](contract-template.md) · Example: [../../examples/example-contract.md](../../examples/example-contract.md)

## When to use

- Starting a new paper or migrating rules from a prior manuscript
- Drafting/revising sections under a frozen abstract
- Auditing terminology drift, claim inflation, or abstract–body mismatch
- Pre-submission consistency pass

## Universal principles

### 1. Narrative authority

After the author **freezes** the abstract ([bootstrap.md](../bootstrap.md)), the **abstract** is the highest standard for story, wording, and claim scope.

On conflict: revise body (and floats) to match the abstract, then update the contract.

### 2. Guardrails, not word substitution

Preserve meaning and boundaries. If a rule hurts readability, keep the intent and rewrite simply.

### 3. One design axis, bounded headline

State: primary design axis; contribution hierarchy; non-headline items.

Conceptual framing may use field terms. Empirical/modeling claims must name concrete signal, behavior, label, prediction variable, metric, or result.

### 4. Terminology layers

| Layer | Role | Neutral pattern |
|-------|------|-----------------|
| Study / resource | Artifact name | Dataset X, Study Y |
| Abstract unit | Conceptual condition | Condition Alpha |
| Concrete unit | What participants did | button-press block |
| Short form | After first definition | Alpha task |
| Group label | Contrast set | active-condition tasks |

**Hierarchy:** `study/experiment` > `task` > `session` > `block` > `trial` > `stage/phase`

Preparatory segments stay below task level. First mention per major section: `Abstract Name (concrete form)`.

**Resource-level vs instance-level** — paradigm adjectives apply to resources/literature unless the contract extends them to tasks/trials.

Domain-specific naming examples belong in `examples/`, not in this framework table.

### 5. Adjacent terms

List pairs readers conflate (category vs label vs target; self-report vs ground truth; cohort vs stratum; modality-generic vs specific). Keep distinct.

**Agency** — participants/recordings express or carry content; abstract constructs are not “produced.”

### 6. Figures and tables

Short abstract names on axes; gloss concrete names on first float occurrence only.

### 7. Facts SSOT

Immutable: N, acquisition, release inventory, access policy. Body must not quietly extend them. Omit repo paths/filenames from body unless venue requires.

### 8. Citation policy

Claim-specific `\cite{}`. Reviews for broad framing; primary sources for methods/dataset facts. Publisher `abstract` in `.bib` when project requires.

## Hard gate (agent)

| Abstract status | Agent may | Agent must not |
|-----------------|-----------|----------------|
| Not frozen | Scaffold; §0; provisional draft help | Fill §1–§4 as final story/contributions/terminology/facts |
| Human-frozen | Fill/sync §1–§4; polish under modes A/B/C | Weaken abstract to excuse body text |

## Workflow: new paper

1. Scaffold + **§0** only.
2. Draft body (abstract may be rough).
3. **Author freezes abstract.**
4. Fill **§1–§4** to match frozen abstract.
5. Multi-pass polish/citation ([collaboration.md](../collaboration.md)).
6. Pre-submission audit.

## Audit checklist

```
- [ ] Abstract matches §1 and §3; claims within results
- [ ] Coined abstract terms appear in §2 with concrete mapping
- [ ] Hierarchy and resource/instance rules held
- [ ] Floats use §2 short names; captions gloss once
- [ ] No repo paths/placeholders in submission PDF
- [ ] Citations claim-specific; headline matches §1 hierarchy
```

## Operating modes (map to kit A/B/C)

| Kit mode | Contract edit meaning |
|----------|----------------------|
| **A** | Language-only in manuscript; term consistency per contract |
| **B** | Structure-safe manuscript edits (**confirm gate required**) |
| **C** / explicit ask | Contract update + propagate (scientific meaning needs user approval) |

**Conflict order:** frozen abstract → writing contract → style anchor → target draft.

## Companions

[polish.md](../polish.md) · [citation.md](../citation.md) · [table-verify.md](../table-verify.md)
