# Bootstrap chronology

How a paper enters steady-state governance. Order matters.

## Stages

```text
1. Environment ready (Cursor + LaTeX; Zotero later OK)
2. Scaffold (venue class, skeleton, figure/table slots) + contract §0
3. First draft (body + rough abstract; story provisional)
4. Author freezes abstract (human narrative seed)  ← hard gate
5. Contract §1–§4 filled / synced to frozen abstract
6. Multi-pass section work (B confirm → A → citation/tables)
7. Pre-submission sync + audit
```

## Agent hard gate

| Before step 4 (abstract not frozen) | After step 4 (user states abstract is frozen) |
|-------------------------------------|-----------------------------------------------|
| Help with environment, scaffold, §0, drafting | Fill/sync §1–§4; run polish/citation under modes |
| **Do not** finalize §1 story, contribution hierarchy, §2 registry, or §3 facts as the paper’s SSOT | Body and floats track the frozen abstract |

If unclear whether the abstract is frozen, **ask once** before writing §1–§4.

## Stage notes

### 1–2. Scaffold

- Venue template (see [venue/](venue/) or project class file).
- Main `.tex`, `references.bib`, copy [contract/contract-template.md](contract/contract-template.md) → `manuscript/WRITING_CONTRACT.md`; fill **§0** (paths, venue, style anchor, compatible kit version).
- Confirm compile ([environment.md](environment.md)). Opening checklist: Cursor + PDF builds + §0 — Zotero optional until citation pass.

### 3. First draft

- Provisional claims and placeholders (`【cite:…】`, `【待扩写】`, `【待补充】`).
- Draft abstract is **not** narrative authority yet.

### 4. Freeze abstract (human)

- Author sets story, wording, and claim ceiling.
- Then: conflict → revise body, then contract.

### 5. Contract sync

- §1–§4 match frozen abstract ([module.md](contract/module.md)).
- Point `.tex` header at project contract + kit.

### 6–7. Steady-state

- [collaboration.md](collaboration.md), [polish.md](polish.md), [citation.md](citation.md), [table-verify.md](table-verify.md).
- Pre-submission: audit checklist + clean PDF.
