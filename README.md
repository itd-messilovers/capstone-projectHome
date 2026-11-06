# TI2006B persistent project repository

License: Original educational content in this example repository is licensed
under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
Code, third-party datasets, APIs, trademarks, and quoted material retain their
own licenses and terms.

Version: `v1.0`  
Status: `example`
## Project summary

- **Project question:** Which Pokémon species and types have the strongest base stats, and how do stats differ by type?
- **Intended audience:** TI2006B classmates and instructor; beginners learning a reproducible data-science workflow.
- **Data source:** Public Pokémon species, type, and base-stat tables from the community-maintained `veekun/pokedex` repository (downloaded by the notebook; no private data).
- **Expected output:** A cleaned analysis table and interactive Plotly charts in `notebooks/01-pokemon-go-analysis.ipynb`.
- **Current limitation:** This is Pokémon GO-inspired teaching data, not Pokémon GO player telemetry. It does not measure accounts, locations, captures, or battles.

## How to start

1. Open `notebooks/01-pokemon-go-analysis.ipynb` in Google Colab or Jupyter.
2. Run all cells from top to bottom (dependencies are listed in `requirements.txt`).
3. Read `notebooks/README.md` and `data/README.md` for provenance and limitations.

## Team

Organization: https://github.com/itd-messilovers
This repository is the persistent home for the project used throughout the
TI2006B workshop. Keep the repository public unless the instructor explicitly
authorizes a private alternative. A public repository allows real-time review
of commits, branches, notebooks, pull requests, and assignment evidence.

## First example: Pokémon analysis

Start with [`notebooks/01-pokemon-go-analysis.ipynb`](notebooks/01-pokemon-go-analysis.ipynb).
It downloads a small public Pokémon species/statistics dataset, creates a
tidy analysis table, and produces interactive Plotly charts. The example is
Pokémon GO-inspired, but it is not a dataset of player locations, accounts,
captures, or Niantic telemetry.

Read [`notebooks/README.md`](notebooks/README.md) before running the notebook.

## Persistent repository structure

```text
.
├── .github/workflows/       # automated checks for every push and pull request
├── data/
│   ├── raw/                 # downloaded or source data; do not commit secrets
│   ├── processed/           # reproducible derived data
│   └── README.md            # data dictionary, provenance, and limitations
├── notebooks/               # exploratory and teaching notebooks
├── reports/                 # figures, summaries, and final reports
├── src/                     # reusable Python code after notebooks stabilize
├── assignments/             # later activity or assignment evidence
├── requirements.txt         # pinned-enough teaching dependencies
├── .gitignore
└── README.md
```

## Working agreement for real-time grading

- Make one focused commit per meaningful change.
- Use a descriptive branch for substantial work, for example
  `activity-02-pokemon-analysis`.
- Keep notebooks runnable from the repository root.
- Put explanations and data provenance in Markdown, not only in code.
- Do not commit passwords, API keys, private student data, personal location
  histories, or unlicensed company data.
- Preserve the notebook outputs when they help a reviewer understand the work,
  but do not treat a rendered chart as proof that the underlying data is valid.

## Run locally

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab
```

The GitHub Actions workflow runs the notebook on pushes and pull requests.
