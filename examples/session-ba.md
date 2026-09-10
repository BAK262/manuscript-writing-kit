# Example: Mode B → Mode A session skeleton

Synthetic dialogue. Replace paths/section names with yours.

## Message 1 — organize (Mode B)

**User:**

```text
/manuscript-writing-kit Mode B on @manuscript/main.tex §Related Work.
Style anchor: frozen abstract + Introduction.
First list proposed structural edits; wait for confirmation.
```

**Agent (stops after plan):**

```text
Loaded: collaboration, polish, project contract. Mode B. Confirm gate: waiting.

Proposed:
1. Merge ¶2–¶3 (both define ambulatory vs clinic).
2. Move dataset-table lead-in to end of ¶1.
3. Drop repeated “home overnight” definition in ¶4 (backward ref only).
```

**User:** `OK except keep ¶4 definition once more for table caption cross-ref.`

**Agent:** applies 1–2 and adjusted 3; reports diffs.

## Message 2 — polish (Mode A)

**User:**

```text
Same range, Mode A. Keep paragraph main points. Style anchor unchanged.
```

**Agent:** wording/rhythm/terminology only; no reorder; lists typo/LaTeX fixes.

## Logic-chain interrupt (when story feels wrong)

**User:**

```text
Logic chain for §Related Work:
1. Clinic PSG corpora established stage labels.
2. Home wearables lowered burden but changed signal semantics.
3. Gap: paired clinic–home designs under one release.
Mode B to this chain; confirm extras.
```

Then send a **separate** Mode A message (unless using the documented combined exception).
