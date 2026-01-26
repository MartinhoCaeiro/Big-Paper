# Big-Paper

English README for the repository that hosts a short legal analysis of the 22 June 2021 Court of Justice of the European Union ruling on cases C‑682/18 (YouTube/Google) and C‑683/18 (Cyando/Uploaded), authored for the Master's in Information Security Engineering at Instituto Politécnico de Beja.

## Contents
- [LaTeX Report/Relatorio.tex](LaTeX%20Report/Relatorio.tex) — main LaTeX source in Portuguese.
- [LaTeX Report/Recursos/referencias.bib](LaTeX%20Report/Recursos/referencias.bib) — bibliography used by `biber`.
- Generated artifacts (`.aux`, `.bbl`, `.bcf`, `.blg`, `.fdb_latexmk`, `.fls`, `.run.xml`) are kept here for convenience but can be regenerated.

## What the paper covers (brief)
- Summarizes the underlying facts and questions referred by the German Federal Court about platform liability for user-uploaded copyrighted works.
- Explains the Court’s interpretation of “communication to the public” and intermediary injunctions under Directives 2001/29/CE and 2000/31/CE.
- Discusses safe-harbor conditions, knowledge standards, and the absence of a general monitoring duty.
- Contrasts the pre-2019 regime with the newer framework introduced by Directive 2019/790, noting its non-retroactive effect on the cases.

## Building the PDF
You need a LaTeX distribution with `latexmk`, `biber`, and the packages imported in the preamble (babel, biblatex with APA style, csquotes, amsmath, karnaugh-map, siunitx, etc.). On most systems, a full TeX Live or MiKTeX install suffices.

Recommended command (from the repository root):

```sh
latexmk -pdf -interaction=nonstopmode -shell-escape -output-directory="LaTeX Report" "LaTeX Report/Relatorio.tex"
```

If you prefer manual steps:

```sh
pdflatex "LaTeX Report/Relatorio.tex"
biber "LaTeX Report/Relatorio"
pdflatex "LaTeX Report/Relatorio.tex"
pdflatex "LaTeX Report/Relatorio.tex"
```

## How to read or edit
- The document is written in Portuguese. Section headings and structure are straightforward if you wish to translate or extend it.
- Bibliographic entries live in the `.bib` file; rerun `biber` after edits.
- Output PDF is emitted to `LaTeX Report/` by default.

## License
- This repository is licensed under the GPL 3.0 License.
