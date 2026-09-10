# Manuscript Writing Contract — Template

Copy this file into your project and fill every `【】` section. Delete instructional lines in `<!-- -->` when done.

**Bootstrap note:** Fill §0 early. Fill §1–§4 after the author freezes the abstract (see kit `modules/bootstrap.md`). Until then, treat draft abstract text as provisional.

---

## §0 Metadata

| Field | Value |
|-------|--------|
| Paper working title | 【】 |
| Venue / template | 【e.g., IEEE journal, compsoc IEEEtran】 |
| Main manuscript path | 【e.g., manuscript/main.tex】 |
| Style anchor section | 【default: Introduction】 |
| Compatible kit version | 【e.g., 1.1.x】 |
| Citation parallelism | 【full / batched / inline】 |
| Contract version / date | 【】 |

**Narrative authority (after freeze):** `\begin{abstract}...\end{abstract}` in 【main path】

---

## §1 Core story and claim scope

<!-- Purpose: stop the agent from inventing a new storyline or headline claim. Minimum: design axis + 3 contribution bullets. -->

### Primary design axis

【One sentence: the main dimension along which conditions vary or the paper organizes its argument.】

### Unit hierarchy (conceptual → concrete)

| Order | Abstract unit | Concrete implementation | Primary output |
|-------|---------------|-------------------------|----------------|
| 1 | 【】 | 【】 | 【】 |
| 2 | 【】 | 【】 | 【】 |
| … | | | |

### Group labels for contrasts

【e.g., "Group A and B as *active X* when contrasted with C."】

### Resource-level vs instance-level terms

| Term | Applies to | Applies to instances only if |
|------|------------|------------------------------|
| 【paradigm adjective】 | 【resources, literature, design】 | 【contract says so】 |

### Contribution hierarchy (first-order)

1. 【】
2. 【】
3. 【】

### Non-headline guardrails

Keep these out of the title and abstract lead unless they *are* the paper:

- 【e.g., benchmark rank, modality count alone, generic SOTA generalization】

### Empirical claim rule

Conceptual framing may use: 【field terms】.

Empirical/modeling claims must name: 【signal, behavior, label, metric, test】.

---

## §2 Terminology registry

### Experimental hierarchy (definitions)

- **Study / experiment:** 【】
- **Task:** 【】 — preferred synonym policy: 【】
- **Session / block / trial / stage:** 【】

### Preparatory segments (below task level)

【List preparatory phases; how to refer.】

### Abstract ↔ concrete naming

| Abstract (title case in abstract) | Concrete | Short form (after definition) | Abbrev (tables only) |
|-----------------------------------|----------|-------------------------------|----------------------|
| 【】 | 【】 | 【】 | 【】 |

### First-mention rule

- **Body:** first mention per `\section`: `Abstract Name (concrete form)`
- **Subsequent:** short form or group label per §1
- **Figures/tables:** short names on axes; caption glosses concrete names on **first occurrence in that float only**

### Capitalization

【Abstract: title case for coined types. Body: sentence-case vs title case policy.】

### Adjacent-term distinctions

| Term A | Term B | Rule |
|--------|--------|------|
| 【instructed category】 | 【label / target】 | 【】 |
| 【self-report】 | 【annotation】 | 【】 |
| 【cohort descriptor】 | 【stratification label】 | 【】 |

### Agency / measurement language

- Prefer 【plain adjective】 when natural
- Imply 【measurement X】 only when design supports it
- 【Abstract construct】 is expressed by 【agents/recordings】

### Modality and domain terms

| Context | Preferred |
|---------|-----------|
| 【modality context】 | 【】 |
| 【behavior】 | 【】 |

### Term preferences

| Prefer | Instead of | Reason |
|--------|------------|--------|
| 【task】 | 【protocol】 | 【hierarchy】 |

---

## §3 Paper-specific facts (immutable)

### Cohort

【N, stratification, inclusion/exclusion, ethics IRB id】

### Acquisition (shared)

【Modalities, montage, sampling — stable facts only】

### Release inventory

Public:

- 【】

Controlled / restricted:

- 【】

### Manuscript omissions

Body omits: 【paths, filenames, archive layout】

### Access and ethics (pointers)

【Repository/DOI policy; DUA; compliance section label】

---

## §4 Citation policy

- Style: 【IEEEtran / natbib / venue】
- Framing claims → 【reviews, surveys】
- Methods and dataset facts → 【primary sources】
- Claim-specific cites only
- BibTeX: 【publisher abstract required: yes/no】

---

## §5 Revision log (optional)

| Date | Change | Sections synced |
|------|--------|-----------------|
| 【】 | 【】 | abstract, §2, Methods, … |
