# ML Course — Environment Setup

This repository is the starting point for the **ML Seminar** at FU Berlin (Bachelor). It provides a reproducible Python environment and ready-to-use templates so you can focus on the course content rather than setup.

## Repository structure

```
ml-setup/
├── pyproject.toml       # Python dependencies
├── quarto_intro/        # Quarto templates (report, slides) and citation example
│   ├── report.qmd       # Report rendered to HTML and PDF
│   ├── slides_revealjs.qmd   # Browser-based slides (RevealJS)
│   ├── slides_beamer.qmd     # PDF slides (LaTeX Beamer)
│   └── references.bib   # BibTeX reference file
└── jupyter_demo/        # Minimal Jupyter notebook demo
    └── demo.ipynb
```

The environment is managed with [uv](https://docs.astral.sh/uv/) and pinned in `uv.lock` to ensure everyone runs the exact same package versions.

## Prerequisites

Install `uv` (fast Python package manager):

```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## Installation

1. Click **"Use this template"** → **"Create a new repository"** on GitHub to create your own copy.
2. Clone your new repository and install the environment:

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
uv sync
```

This will automatically:
- Download and install Python 3.13 (if not already available)
- Create a virtual environment in `.venv/`
- Install all pinned dependencies from `uv.lock`

## Running Jupyter

```bash
uv run jupyter lab
```

## Initializing the Jupyter Kernel

If Jupyter does not automatically detect the environment, register it manually as a kernel:

```bash
uv run python -m ipykernel install --user --name ml-setup --display-name "ML Course"
```

Then restart Jupyter Lab and select **ML Course** from the kernel menu.

## Packages included

| Package | Purpose |
|---|---|
| `numpy` | Numerical computing |
| `pandas` | Data manipulation |
| `scikit-learn` | Machine learning |
| `matplotlib` | Plotting |
| `torch` | Deep learning (PyTorch) |
| `statsmodels` | Statistical models |
| `jupyter` / `ipykernel` | Notebook environment |

## Updating the environment

If the course materials are updated and you need to sync the latest dependencies:

```bash
git pull
uv sync
```
