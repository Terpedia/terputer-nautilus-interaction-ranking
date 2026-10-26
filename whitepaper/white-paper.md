# Terpene–protein interaction ranking: NAuTILUS methods study

## Abstract
NAuTILUS proposes a scalable, provenance-aware workflow to prioritize terpene–protein interaction hypotheses across a curated ligand panel and tiered human pocketome. The design combines ligand and structure preparation, model-based ranking, selected-pair docking, and evidence-graph integration. The local canonical materials are a methods design and project summary; they do not contain a completed score matrix or validated interactions.

## Research question
Can computational ranking reduce a large terpene–pocket search space to a traceable, experimentally testable candidate set?

## Proposed methods
The source design describes approximately 100 terpene ligands and a pilot pocketome of roughly 1,000 proteins, expanding to 2,000–5,000 pockets. Ligand standardization includes canonical identity, stereochemistry, protonation context, conformer generation, and minimized structures. Protein inputs combine curated structures and high-confidence predicted structures with explicit pocket coordinates and accession metadata. A joint protein–ligand model proposes scores; a selected high-ranking subset proceeds to DiffDock or a cross-check docking engine. Pair records should retain ligand identity, protein accession, pocket definition, model version, structure provenance, score, uncertainty, and execution timestamp.

## Results and current status
No computational ranking or docking results are available in the packaged canonical source. Pair counts in the source are planning estimates, not observed output. Therefore this study reports a methods design only.

## Validation and limitations
Predicted affinity and docking pose scores are prioritization signals, not binding measurements. Validation should include known-ligand positive controls, negative controls, stereochemical checks, benchmark splits that prevent leakage, external affinity resources, and biochemical assays. Static structures omit conformational ensembles, membrane context, solvent dynamics, and many covalent or reactive mechanisms.

## Reproducibility
The source methods design and executive summary are preserved under `data/`; their checksums and original local paths are recorded in `data/manifest.tsv`. The notebook reports design parameters only. No biological interaction is asserted.
