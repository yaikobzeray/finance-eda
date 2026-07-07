# Finance EDA — Loan Dataset Analysis

> Exploratory data analysis on a loan dataset: missing value detection, type inspection, and a modular feature-engineering pipeline — part of an ML engineering learning roadmap.

## Description

This notebook-first project performs exploratory data analysis on a loan CSV dataset to understand its structure, data quality, and key variables before modelling. The repo also contains modular Python source (`src/`) with separate cleaning, feature engineering, and pipeline scripts — demonstrating the separation of EDA from production code. Intended as a learning milestone toward applied ML engineering, not a complete model.

<!-- TODO: add chart/output screenshot at docs/screenshot.png -->
<!-- ![Loan EDA Output](docs/screenshot.png) -->

## Tech Stack

- **Language:** Python 3
- **Analysis:** pandas, numpy
- **Visualisation:** matplotlib
- **Notebook:** Jupyter (`.ipynb`)
- **Dependency management:** pip + `requirements.txt`

## Key Features

- 📊 **Shape & type inspection** — `.dtypes`, `.shape`, null-value summary
- 🧹 **Cleaning module** (`src/cleaning.py`) — reusable cleaning functions, importable separately from the notebook
- ⚙️ **Feature engineering module** (`src/features.py`) — feature construction logic decoupled from exploration
- 🔄 **Pipeline** (`src/pipeline.py`) — composable cleaning + feature steps
- 📁 **Structured layout** — `data/raw/`, `notebooks/`, `src/` separation follows ML project conventions

## Project Structure

```
finance-eda/
├── data/
│   └── raw/loan.csv            # Raw loan dataset
├── notebooks/
│   └── 01_exploration.ipynb    # Main EDA notebook
├── src/
│   ├── cleaning.py             # Data cleaning functions
│   ├── features.py             # Feature engineering
│   └── pipeline.py             # End-to-end pipeline composition
├── requirements.txt
└── README.md
```

## Setup & Run

```bash
# Create and activate virtual environment
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook notebooks/01_exploration.ipynb
```

## Roadmap

This repo is step 1 of an ML learning sequence:
1. ✅ EDA & cleaning (this repo)
2. ⬜ Feature selection + baseline model (scikit-learn)
3. ⬜ Model serving with FastAPI
4. ⬜ Docker + deployment
