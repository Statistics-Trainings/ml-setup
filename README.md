# ML Seminar — Environment Setup

This repository contains the Python environment specification for the **ML Seminar Course** at FU Berlin (Summer Term 2026). Use it to install a ready-to-go environment with all required packages via [uv](https://docs.astral.sh/uv/).

## Prerequisites

Install `uv` (fast Python package manager):

```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## Installation

Clone this repository and install the environment:

```bash
git clone https://github.com/PhilippBach/ml-setup.git
cd ml-setup
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
