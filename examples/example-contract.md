# Filled contract example — AuroraSleep (fictional)

**Synthetic example only.** Names, design axis, task labels, cohort figures, and
ethics IDs are invented for structure demonstration. New papers: copy
[../modules/contract/contract-template.md](../modules/contract/contract-template.md).

Companion modules: `modules/polish.md`, `modules/citation.md`.

---

## §0 Metadata

| Field | Value |
|-------|--------|
| Paper working title | AuroraSleep: A Multimodal Overnight Dataset for Stage-Aware Wearable Monitoring |
| Venue / template | IEEE Sensors Journal; `\documentclass[journal]{IEEEtran}` |
| Main manuscript path | `manuscript/main.tex` |
| Style anchor section | Introduction |
| Kit polish module | `manuscript-writing-kit` → `modules/polish.md` |

---

## §1 Core story and claim scope

### Primary design axis

**Axis of monitoring burden:** clinic polysomnography → home wearable overnight →
daytime brief nap probe.

### Unit hierarchy

| Order | Abstract unit | Concrete implementation | Primary output |
|-------|---------------|-------------------------|----------------|
| 1 | Clinic Reference | attended PSG night | scored sleep stages |
| 2 | Home Overnight | consumer-band + contact mic | wearable signals + audio |
| 3 | Nap Probe | 40-min afternoon nap | short-window features |

**Group:** Home Overnight + Nap Probe = **ambulatory monitoring**
(vs Clinic Reference).

### Resource-level vs instance-level

| Term | Applies to | Instance tasks |
|------|------------|----------------|
| ambulatory-first | AuroraSleep resource, design framing, related-work contrast | only if contract extends |
| clinic-anchored | legacy PSG corpora, literature | only if contract extends |

### Goal (field positioning)

Support sleep-stage models that transfer from clinic anchors to lower-burden
home settings without treating wearable nights as drop-in PSG substitutes.

### Non-headline guardrails

Title/abstract lead stay on design/transfer framing rather than leaderboard
scores, sensor-count alone, or generic cross-device claims.

### Empirical claim rule

Conceptual: sleep architecture, arousal, monitoring burden.

Empirical: name signal (EEG channel set, PPG, actigraphy), label (AASM stage),
prediction variable, or reported metric (macro-F1, κ).

---

## §2 Terminology registry

### Experimental hierarchy

- **Experiment / dataset:** AuroraSleep
- **Task:** Clinic Reference, Home Overnight, Nap Probe — prefer “task” over
  collapsing synonyms such as “protocol”
- **Trial, block, session:** per Methods; preparatory segments below

### Preparatory segments (below task level)

- Sensor fitting and impedance check before Clinic Reference
- Band pairing and diary briefing before Home Overnight

Refer naturally ("fitting check," "pairing"). Do not elevate them to task level.

### Naming table

| Abstract | Concrete | Short | Table abbrev |
|----------|----------|-------|--------------|
| Clinic Reference | attended PSG night | Clinic | Clin. |
| Home Overnight | consumer-band night | Home | Home |
| Nap Probe | 40-min afternoon nap | Nap | Nap |

### First-mention rule

- Body: `Clinic Reference (attended PSG night)` first per section; then
  `the Clinic task` / group `the two ambulatory monitoring tasks`
- Figures/tables: Clinic / Home / Nap on axes; parenthetical concrete gloss in
  caption on first float occurrence only

### Capitalization

Abstract: title case for three monitoring types. Body: sentence case when generic
(`clinic reference night`).

### Adjacent-term distinctions

| A | B | Rule |
|---|---|------|
| AASM stage label | model prediction | Keep distinct; “target” only after the label variable is explicit |
| self-report sleep diary | PSG stage | Diary is subjective; not ground truth for stage metrics |
| cohort descriptor | site stratum | “community adults” vs “Site A / Site B” stratification labels |
| wearable | PSG | Do not equate channel semantics across devices |

### Agency

Sleep stages are scored or predicted; devices record signals. Participants
undergo monitoring nights; the dataset does not “produce” stages.

### Contrasts

Prefer **clinic reference vs ambulatory monitoring**, or name all three levels.
Reserve ambulatory-first / clinic-anchored for resource-level comparison.

---

## §3 Paper-specific facts

### Cohort

N=120 released adults; two collection sites; ethics approval ID
**IRB-EX-2024-0000** (placeholder); ESS screen <16.

### Acquisition

PSG 6 EEG + EOG/EMG on Clinic nights; PPG + 3-axis actigraphy + contact mic on
Home nights; same wearable montage on Nap Probe.

### Release inventory

Public: de-identified wearable streams; stage labels for Clinic nights; code;
data dictionary.

Controlled: raw PSG EDF; identifiable audio (Home).

### Omissions in manuscript body

Directory layouts, filenames, and internal paths stay in data documentation /
supplement as appropriate.

---

## §4 Citation policy

- BibTeX + `IEEEtran`
- Claim-specific cites only
- Reviews/surveys for broad framing; primary sources for methods and dataset facts
- `references.bib` entries include publisher abstract when project policy requires it
