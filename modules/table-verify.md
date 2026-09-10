# Resource comparison table verify

End-to-end verify for literature-backed comparison tables: policy → per-row evidence → integrate → clean up.

## When to use

- Add/edit resource or dataset comparison rows.
- Strict check against abstracts / primary docs.
- Update LaTeX + `.bib` and remove scratch files.

## Paths (discover)

| Item | Typical location |
|------|------------------|
| Main manuscript | User scope or contract §0 |
| Master `.bib` | Beside `.tex` or from `\bibliography{}` / `\addbibresource{}` |
| Table bodies | e.g. `manuscript/tables/*.tex` |
| Scratch | `temp/dataset_verify_<slug>.md` |

## Step 1 — Policy and table scope

1. Open target `.tex`; read contract / header citation policy / Related Work rules.  
2. Identify exact table: path, caption, column semantics (legend codes constrain “correct”).  
3. Build per-row worklist (cite key or “this work” + verbatim cells).

## Step 2 — Per-resource verification

For each row:

1. Load `.bib` entry (title, venue, **abstract**, authors, DOI).  
2. If abstract cannot support a cell → primary sources (publisher PDF, official dataset page). Prefer first-party evidence.  
3. Write `temp/dataset_verify_<slug>.md`: claim-by-claim verdict + evidence + recommended cell/BibTeX fixes.

**Parallelism:** one subagent per resource when many rows; sequential OK for small tables. If subagents unavailable, run sequential inline and note that in the report.

## Step 3 — Integrate

1. Read all scratch reports for this pass.  
2. Update table (and caption/legend if codes change). Honor **contract terminology**.  
3. Update master `.bib`; keep policy fields (e.g. `abstract`).  
4. Compile as the project requires.

Weak evidence → soften cell or qualify legend.

## Step 4 — Clean up

After integration (or user confirmation): delete this pass’s `temp/dataset_verify_*.md`. Leave other `temp/` files.

## Quality checklist

- [ ] Step 1: policy and column semantics explicit  
- [ ] Step 2: one report per resource; disputed cells evidenced  
- [ ] Step 3: table, caption, `.bib` aligned; project builds  
- [ ] Step 4: scratch reports removed  

## Compact codes

New legend tokens when needed; keep rows one-line-friendly; re-run Steps 2–3 for new resources only.
