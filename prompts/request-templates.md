# Request templates

Attach `/manuscript-writing-kit` and `@` your main `.tex`. Fill brackets.

## Bad → better

```text
Bad:    把这一节改好看一点（结构和用词一起随便改）。
Better: Mode B on @[main.tex] [SECTION]. Style anchor: abstract + Introduction.
        First list structural edits; wait for my OK. (Then a second message: Mode A.)
```

## Mode A — paragraph polish

```text
Role: academic editor for [VENUE].
Task: /manuscript-writing-kit polish, Mode A.
Scope: @[main.tex] [SECTION or Lxxx–Lyyy].
Style anchor: frozen abstract, Introduction, and settled text before this range.
Lock: keep each paragraph’s main point; language only.
```

## Mode B — reorganize (confirm required)

```text
Role: [VENUE] domain expert.
Task: /manuscript-writing-kit polish, Mode B on @[main.tex] [SECTION].
Style anchor: abstract, Introduction, preceding settled sections.
Required: list proposed structural edits first. Wait for my confirmation, then apply.
```

## Logic-chain reset (Mode B only)

```text
Logic chain for [SECTION]:
1. …
2. …
3. …
Apply with Mode B. List any edits beyond this chain and wait for OK.
Style anchor: abstract + Introduction. Honor contract terminology.
```

## Logic-chain then Mode A — combined exception

Use only when you explicitly want one turn. Prefer two messages (B, then A).

```text
EXCEPTION combined pass: apply this logic chain with Mode B (confirm structural extras), then Mode A polish on the same range.
Chain:
1. …
2. …
3. …
Style anchor: abstract + Introduction.
```

## Citation pass (body frozen)

```text
Role: [VENUE] expert.
Task: citation on @[main.tex] [SECTION].
Do not rewrite body; resolve cites / 【cite:…】 only.
Parallelism: full | batched | inline (default: full if subagents work, else inline).
```

## Citation pass (default)

```text
manuscript-writing-kit citation on @[main.tex] [SECTION or Lxxx–Lyyy].
Honor every 【cite:…】 brief. Report ledger + parallelism tier.
```

## Table verify

```text
table-verify on [table path or Table N].
Update table + .bib; remove scratch reports when done. Honor contract terminology.
```

## Reviewer comments (session open)

```text
Role: [VENUE] expert.
Revise @[main.tex] from reviewer comments.
Rules: writing contract; style anchor = abstract + Introduction + settled preceding text.
Restate these requirements; I will send comments one by one.
```

## New paper bootstrap

```text
manuscript-writing-kit bootstrap for [VENUE].
Scaffold, WRITING_CONTRACT.md §0, confirm compile.
I will draft and freeze the abstract myself before §1–§4.
```

## Existing draft, abstract not frozen

```text
Mode A only on @[main.tex] [small range].
Do not fill WRITING_CONTRACT §1–§4 yet; abstract is not frozen.
```
