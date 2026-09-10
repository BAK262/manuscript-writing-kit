# Bootstrap chronology

How a paper enters the kit’s steady-state governance. Order matters.

## Stages

```text
1. Environment ready (Cursor + LaTeX + optional Zotero)
2. Scaffold (venue class, chapter skeleton, figure/table slots)
3. First draft (body + rough abstract; story still provisional)
4. Author freezes abstract (human narrative seed)
5. Contract §1–§4 filled / synced to frozen abstract
6. Multi-pass section work (collaboration + polish + citation + tables)
7. Pre-submission sync (abstract ↔ body ↔ contract) + audit
```

## Stage notes

### 1–2. Scaffold

- Pick venue template (e.g. IEEEtran compsoc). See [venue/ieee-compsoc-journal.md](venue/ieee-compsoc-journal.md) when relevant.
- Create main `.tex`, preamble, appendix if needed, `references.bib`.
- Copy [contract/contract-template.md](contract/contract-template.md) → project `manuscript/WRITING_CONTRACT.md`; fill **§0** (paths, venue, style-anchor field).
- Confirm compile loop works ([environment.md](environment.md)).

### 3. First draft

- Write sections with provisional claims and placeholders (`【cite:…】`, `【待扩写】`, `【待补充】` as needed).
- Abstract may exist as a draft; it is **not yet** narrative authority.

### 4. Freeze abstract (human)

- Author rewrites the abstract into the story, wording, and claim ceiling they want.
- After this point, body and figures/tables track the abstract; conflict → revise body, then contract.

### 5. Contract sync

- Fill §1 story, §2 terminology, §3 facts, §4 citations to match the frozen abstract ([contract/SKILL.md](contract/SKILL.md)).
- Point `.tex` header comments at the project contract and kit framework.

### 6–7. Steady-state

- Use [collaboration.md](collaboration.md) for section multi-pass work.
- Use [polish.md](polish.md), [citation.md](citation.md), [table-verify.md](table-verify.md) as separate passes.
- Before submission: contract audit checklist + compile clean PDF.
