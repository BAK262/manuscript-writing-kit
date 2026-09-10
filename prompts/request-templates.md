# Request templates

Copy, fill brackets, attach `/manuscript-writing-kit` (or the relevant stub name). Paths and line numbers are examples—replace from your project.

## Mode A — paragraph polish

```text
Role: academic editor for [VENUE].
Task: /manuscript-writing-kit polish, Mode A.
Scope: @[main.tex] [SECTION or Lxxx–Lyyy].
Style anchor: frozen abstract, Introduction, and settled text before this range.
Lock: keep each paragraph’s main point; language, coherence, redundancy only.
```

## Mode B — reorganize (confirm first)

```text
Role: [VENUE] domain expert.
Task: /manuscript-writing-kit polish, Mode B on @[main.tex] [SECTION].
Style anchor: abstract, Introduction, preceding settled sections.
First: list proposed structural edits. Wait for my confirmation, then apply.
```

## Logic-chain reset then polish

```text
Here is the intended logic chain for [SECTION]:
1. …
2. …
3. …
Apply this chain (Mode B), then Mode A polish. Style anchor: abstract + Introduction.
Honor contract terminology.
```

## Citation pass (body frozen)

```text
Role: [VENUE] expert with strict citation taste.
Task: citation workflow on @[main.tex] [SECTION].
Requirement: do not rewrite body prose; resolve cites / 【cite:…】 only.
Phase 2 may use subagents (sentence- or paragraph-parallel per kit rules).
```

## Citation pass (default)

```text
Use manuscript-writing-kit citation on @[main.tex] [SECTION or Lxxx–Lyyy].
Honor every 【cite:…】 brief exactly. Report sentence coverage ledger.
```

## Table verify

```text
Verify resource comparison table [path or Table N] with table-verify module.
Align cells to abstracts / primary sources; update table + .bib; remove scratch reports when done.
Honor contract terminology for cell wording.
```

## Reviewer comments (session open)

```text
Role: [VENUE] expert; follow target-journal writing expectations.
Task: revise @[main.tex] from reviewer comments.
Rules: (1) honor writing contract; (2) when editing a section, align narrative with abstract, Introduction, and settled preceding text as style anchor.
Restate these requirements, then I will send comments one by one.
```

## New paper bootstrap

```text
Start a new [VENUE] LaTeX manuscript with manuscript-writing-kit bootstrap.
Scaffold template, WRITING_CONTRACT.md §0, confirm compile. I will draft, then freeze the abstract myself before full contract §1–§4.
```
