# Venue profile: IEEE Computer Society journal (compsoc)

Notes distilled for IEEEtran **Computer Society** journal mode (`compsoc`). Confirm against the current IEEE author kit for the target transactions journal before submission.

## Document class

```latex
\documentclass[10pt,journal,compsoc]{IEEEtran}
```

## Citations

Computer Society journals often list citations **without compressed ranges**:

```latex
\ifCLASSOPTIONcompsoc
  \usepackage[nocompress]{cite}
\else
  \usepackage{cite}
\fi
```

## Title / abstract block

Use compsoc title-abstract helpers as in the official `bare_jrnl_compsoc.tex` pattern (e.g. `\IEEEtitleabstractindextext`, `\IEEEraisesectionheading` for the first section). Prefer **pdfLaTeX** when using `\IEEEPARstart` drop caps.

## Typical build

```text
pdflatex <main>
bibtex <main>
pdflatex <main>
pdflatex <main>
```

## Supplementary / appendix

Follow the venue’s current rules for separate supplementary files vs appendix in the same PDF. Keep cross-references via `\externaldocument` only when the project already uses that pattern.

## Kit links

- Environment: [../environment.md](../environment.md)
- Contract §0 venue field should name compsoc / IEEEtran explicitly
