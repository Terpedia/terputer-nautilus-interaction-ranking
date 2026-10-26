# Terpene–protein interaction ranking (NAuTILUS)

**Category:** Proteomics  
**Status:** Methods design

## Research question

Can a reproducible, provenance-aware workflow prioritize terpene–protein pairs for later docking and experimental follow-up?

## Quick start

Create the environment with `conda env create -f environment.yml`, activate it, then run `jupyter lab notebooks/analysis.ipynb`. Notebook paths are relative to the study root; start Jupyter from this directory.

## Contents

- `notebooks/analysis.ipynb` — runnable inventory/audit notebook.
- `whitepaper/white-paper.md` — evidence-bounded study report.
- `data/manifest.tsv` — provenance and checksums for packaged inputs.
- `environment.yml` — minimal reproducible Python environment.

## Evidence boundary

NAuTILUS methods design: rank terpene–protein hypotheses, then triage a subset with docking and graph evidence. No computed interaction matrix is present in this package; predictions must remain hypotheses until experimental validation.
