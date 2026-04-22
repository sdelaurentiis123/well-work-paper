# well-work-paper

LaTeX source + figures for the ML4PS 2026 workshop submission:

**"Pretraining Transfer for Neural MHD Surrogates: What Generalizes, What Doesn't, and Why It Matters for Plasma Foundation Models"**

Experimental code, training logs, and raw data live in the sibling repo
[`well-work`](https://github.com/sdelaurentiis123/well-work). This repo is
self-contained for the paper build only.

## Build

```bash
pdflatex main && bibtex main && pdflatex main && pdflatex main
```

Figures are committed as PDFs so the build has no external dependencies.

## Regenerate figures

Requires the parent `well-work` repo checked out with its local
checkpoints and eval artifacts present. From the `well-work` repo root:

```bash
source mlvenv/bin/activate
python p1/paper/make_figures.py
cp p1/paper/figures/*.{pdf,png} /path/to/well-work-paper/figures/
```

## Layout

```
main.tex            # 6-page draft
references.bib      # citations
make_figures.py     # figure regeneration script (local copy)
DRAFT_STATUS.md     # submission checklist + known gaps
figures/            # 6 PDFs + 6 PNGs, paper-ready
```

## Source commit

Snapshot from `well-work@main` commit `6d56069`.
