# Human–agent collaboration

Quality lives in **how** each section is worked, not only in contract rules.

## Multi-pass per section

Work **one section (or smaller range) at a time**. Typical spiral:

| Pass | Lead | Mode | Goal |
|------|------|------|------|
| 0 Skeleton | Human | — | Paragraph roles and section outline |
| 1 Organize | Human + agent | **B** (structure-safe) | Paragraph order, inter-paragraph logic, cut redundancy; **list proposed edits → user confirms → apply** |
| 2 Paragraph polish | Agent + human review | **A** (language-only) | Line/subsection scope; register, rhythm, terminology; **keep each paragraph’s main point** |
| 3 Evidence | Citation / table-verify | separate skills | Cites or table cells; may freeze body prose (“insert cites only”) |
| 4 Logic reset | **Human** | — | If the section feels wrong: restate the logic chain in own words, then re-enter pass 1–2 |

Keep **organize** and **paragraph polish** as separate requests. Mixing them in one prompt invites uncontrolled rewrites.

## Logic-chain reset (quality gate)

When prose is smooth but wrong, or empty:

1. Author writes a plain-language chain: paragraph 1 does X → 2 does Y → 3 does Z.
2. Agent edits to that chain (Mode B or C as specified), using the frozen abstract + contract as global bounds.
3. Then Mode A polish.

Global story = frozen abstract + contract. **Local argument** = this human logic chain.

## Prompt grammar (eight principles)

Every high-quality request should set:

1. **Role** — domain expert / academic editor for the venue.
2. **Scope** — file + section / subsection / line range (`L245–L251`). Narrower is better.
3. **Skill + mode** — e.g. kit polish Mode A or B; or citation with “body frozen”.
4. **Style anchor** — frozen abstract + Introduction + **already-settled preceding sections** (optionally adjacent paragraphs).
5. **Intent lock** — preserve paragraph main points unless Mode B/C + confirmation.
6. **Confirmation gate** — Mode B / large edits: summarize planned changes; wait for OK.
7. **Session discipline** — complex revision: agent restates requirements; then comments one-by-one.
8. **Author briefs** — honor `【cite: …】` clauses exactly (counts, mandatory works, fallbacks, conditional no-cite).

Copy-paste skeletons: [../prompts/request-templates.md](../prompts/request-templates.md).

## Placeholders

| Marker | Owner | Pass |
|--------|-------|------|
| `【cite: …】` / `【cite：…】` | Citation module | Evidence pass |
| `【待扩写】`, `【待补充】`, etc. | Human / polish only if asked | Content; polish Mode A leaves them unless user asks to fill |

## Reviewer-comment session pattern

1. User states standing rules (contract, style anchor = abstract + intro + prior settled text).
2. Agent **restates** those rules.
3. User sends comments **one at a time**; agent applies within scope and mode; confirms before structural moves.

## Division of labor (quick)

| Concern | Module |
|---------|--------|
| What may be claimed / named | Contract |
| How to collaborate | This file |
| How prose should sound | [polish.md](polish.md) |
| Sentence-level cites | [citation.md](citation.md) |
| Comparison table rows | [table-verify.md](table-verify.md) |
