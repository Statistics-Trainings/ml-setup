# Quarto Introduction

[Quarto](https://quarto.org/) is an open-source publishing system built on Pandoc. It lets you combine prose, code, and output into polished documents, slides, and websites — all from a single `.qmd` file.

## Prerequisites

Install Quarto from [quarto.org/docs/get-started](https://quarto.org/docs/get-started/). The Python packages needed for code execution are already included in the course environment.

## Templates in this folder

| File | Output format | Description |
|---|---|---|
| `report.qmd` | HTML + PDF | Self-contained report with figures and tables |
| `slides_revealjs.qmd` | RevealJS (HTML) | Interactive browser-based slides |
| `slides_beamer.qmd` | PDF (LaTeX Beamer) | Classic academic PDF slides |

## Rendering

First, navigate to this directory:

```bash
cd quarto_intro
```

Then run any of the following to preview or render the quarto files to the specified output:

```bash
# RevealJS slides (HTML)
uv run quarto preview slides_revealjs.qmd
uv run quarto render slides_revealjs.qmd

# Beamer slides (PDF)
uv run quarto preview slides_beamer.qmd
uv run quarto render slides_beamer.qmd

# Report (renders both HTML and PDF)
uv run quarto preview report.qmd
uv run quarto render report.qmd

# Specify output format
uv run quarto render report.qmd --to html
uv run quarto render report.qmd --to pdf


# render all files in this directory
uv run quarto render .
```

> **Beamer slides** require a LaTeX installation (e.g. [TinyTeX](https://yihui.org/tinytex/)):
> ```bash
> uv run quarto install tinytex
> ```
