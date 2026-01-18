# desk-quant-toolkit

[![CI](https://github.com/mengden-quant/desk-quant-toolkit/actions/workflows/ci.yml/badge.svg)](https://github.com/mengden-quant/desk-quant-toolkit/actions/workflows/ci.yml)

Sell-side desk quant mini-projects focused on pricing, Greeks, calibration diagnostics, and production-style tooling.
(Primary focus: Monte Carlo pricing & Greeks)

## What’s inside
This repo contains small, reproducible desk-quant mini-projects:
- clean Python package layout (`src/`)
- tests (`pytest`)
- linting (`ruff`)
- CI via GitHub Actions
- reproducible experiments (seeded runs + configs)
- benchmark tables: accuracy (SE/CI) vs runtime

## Projects

### DQT01 — Monte Carlo Greeks in practice
- Scope: European vanilla + digital options under BSM.
- Greeks: delta / vega via pathwise, likelihood ratio, and bump-and-revalue.
- Variance reduction: CRN for bump; control variates / antithetic (where applicable).
- Diagnostics: confidence intervals, convergence checks, bump-size stability, sign/monotonicity sanity checks.
- Project README: `projects/01-mc-greeks/README.md`
- Demo notebook (optional): `projects/01-mc-greeks/notebooks/01_results.ipynb`

## Quickstart
Install:
```bash
poetry install
```

Run quality checks (same as CI):
```bash
poetry run ruff check .
poetry run pytest
```

Run the main experiment:
```bash
poetry run python projects/01-mc-greeks/scripts/run_experiment.py
```

## Repo structure
- `src/deskquant/` — package code
- `tests/` — unit tests
- `projects/` — per-module mini-projects (docs + notebooks + scripts)

## Links
- LinkedIn: https://www.linkedin.com/in/alexey-mengden
