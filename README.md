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


## Terpedia access

The optional client in `src/terpedia_access.py` calls the Terpedia Knowledge API at `/v1/tabular/search`. It reads `TERPEDIA_KNOWLEDGE_API_KEY` and `TERPEDIA_KB_API_URL` from the process environment and sends the key in the `x-knowledge-key` header. Copy `.env.example` as a configuration reference, then provide the real key through a local secret manager, Codespaces secret, or authorized GitHub Actions secret. Never commit `.env` or print the key in notebook output.
