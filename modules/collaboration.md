# Human–agent collaboration

Quality lives in **how** each section is worked.

## Multi-pass per section

One section (or smaller range) at a time:

| Pass | Lead | Mode | Goal |
|------|------|------|------|
| 0 Skeleton | Human | — | Paragraph roles |
| 1 Organize | Human + agent | **B** | Order/logic/redundancy; **list edits → user confirms → apply** |
| 2 Polish | Agent + human | **A** | Wording; keep paragraph main points |
| 3 Evidence | Citation / table-verify | separate | Cites or table cells |
| 4 Logic reset | **Human** | — | Restate logic chain; re-enter 1–2 |

**Default:** send organize (B) and polish (A) as **separate messages**.

**Exception (only):** user explicitly pastes the combined “Logic-chain reset then polish” template and accepts B-then-A in one turn — still **confirm structural edits before applying** if anything beyond the stated chain is proposed.

## Logic-chain reset

When prose is smooth but wrong:

1. Author writes plain chain: ¶1 does X → ¶2 does Y → ¶3 does Z.  
2. Agent applies chain (Mode B, confirm gate).  
3. Separate Mode A polish (unless user invoked the combined exception above).

Global story = frozen abstract + contract. Local argument = this chain.

## Prompt grammar

1. Role · 2. Scope (file + section/lines) · 3. Skill + mode · 4. Style anchor · 5. Intent lock · 6. **Confirm gate for B/C (mandatory)** · 7. Restate rules on complex revision · 8. Honor `【cite:…】` briefs exactly.

Templates: [../prompts/request-templates.md](../prompts/request-templates.md).

## When you fear losing the story

Paste the logic-chain template; insist Mode B lists edits first; remember **frozen abstract wins**.

## Placeholders

| Marker | Pass |
|--------|------|
| `【cite: …】` | Citation |
| `【待扩写】` / `【待补充】` | Content; Mode A leaves unless asked |

## Reviewer-comment session

1. User states rules. 2. Agent restates. 3. Comments one-by-one; confirm before structural moves.

## Division of labor

Contract · this file · [polish.md](polish.md) · [citation.md](citation.md) · [table-verify.md](table-verify.md)
