# Resource comparison table verify

End-to-end verify for **literature-backed** comparison tables (datasets, corpora, related resources): align with manuscript policy, check **each resource row**, merge into table + master `.bib`, then remove scratch reports.

## When to use

- Adding or editing rows in a resource / dataset comparison table.
- Strict check of table claims against abstracts, papers, or official documentation.
- After verification: update LaTeX + BibTeX and clean temp files.

## Paths (discover; conventions)

| Item | Typical location |
|------|------------------|
| Main manuscript | User scope or contract §0 (often under `manuscript/`) |
| Master bibliography | Beside `.tex` or from `\bibliography{}` / `\addbibresource{}` |
| Table bodies | e.g. `manuscript/tables/*.tex` |
| Scratch outputs | `temp/dataset_verify_<resource-slug>.md` (one file per row) |

Use **project-root relative** paths in agent instructions.

## Step 1 — Policy and table scope

1. Open target `.tex`; read writing/citation policy (contract, header comments, Related Work rules).
2. Identify the **exact table**: path, caption intent, column semantics (codes in the legend constrain “correct”).
3. Build a **per-row worklist**: each resource = cite key or “this work” row with verbatim cells/codes to check.

## Step 3 — Per-resource verification

For each row:

1. Load the `.bib` entry: title, venue, **abstract**, authors, DOI.
2. If the abstract cannot support a cell, consult **primary sources** (publisher PDF, dataset landing page, official docs). Prefer first-party evidence.
3. Write `temp/dataset_verify_<slug>.md`.

Each report includes: cite key + DOI/URL; claim-by-claim verdict (accurate / inaccurate / clarify) + evidence; recommended cell text/code; BibTeX fixes if needed.

**Parallelism:** one subagent per resource when many rows; sequential loop is fine for small tables.

## Step 4 — Integrate

1. Read all `temp/dataset_verify_*.md` for this pass.
2. Update table body (and caption/legend if codes change). Honor **contract terminology**.
3. Update master `.bib` when reports flag metadata; keep policy fields (e.g. `abstract`).
4. Compile (`pdflatex`/`xelatex` + `bibtex` as the project requires).

If evidence is weak: soften the cell or qualify the legend.

## Step 7 — Clean up

After integration (or user confirmation): delete this pass’s `temp/dataset_verify_*.md`. Leave other `temp/` content untouched.

## Quality checklist

- [ ] Step 1: policy and column semantics explicit
- [ ] Step 3: one report per resource; disputed cells evidenced
- [ ] Step 4: table, caption, `.bib` aligned; project builds
- [ ] Step 7: scratch reports removed

## Compact codes

When columns use single-letter codes + caption legend: add legend lines for new tokens; keep rows one-line-friendly in `tabular`/`tabularx`; re-run Steps 3–4 for new resources only.
