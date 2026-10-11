# 🐋 Sperm Whale Coda Communication Analysis

## Acoustic Structure, Turn-Taking, and Sequential Response Patterns

This repository contains an independent computational research project investigating structure in sperm whale communication.

The study examines two related questions:

1. How reliably can selected sperm whale coda types be distinguished from their rhythm and tempo?
2. Does the type of coda produced by one whale depend on the coda immediately produced by another whale during social exchanges?

The analysis combines acoustic feature representation, unsupervised clustering, supervised classification, dialogue timing analysis, and permutation testing.

---

## Research Overview

Sperm whales communicate using short sequences of clicks known as **codas**.

This project focuses on four 5-click coda types:

- `1+1+3`
- `2+3`
- `5R1`
- `5R2`

Each coda was represented using:

- four normalized inter-click intervals (rhythm)
- total coda duration (tempo)

The analysis then extended from individual codas to temporally ordered dialogue events between whales.

---

## Key Results

- Four selected coda types showed reproducible acoustic differences in rhythm and tempo.
- Grouped cross-validation produced a mean balanced classification accuracy of approximately **0.997**.
- Speaker-change transitions occurred after substantially shorter gaps than same-speaker continuations.
- Cross-speaker response coda type was associated with the preceding coda type more strongly than expected from local whale repertoires alone.
- The observed mutual information was approximately **0.195**, compared with a permutation-null mean of approximately **0.120**.
- The permutation test produced **p ≈ 0.0002**.
- The strongest enriched transitions were concentrated within the **5R coda family**, particularly:
  - `5R1 → 5R2`
  - `5R2 → 5R1`
  - `5R2 → 5R2`

These results do **not** establish the semantic meaning of individual codas. Instead, they identify reproducible interaction patterns that may help guide future behavioral studies of sperm whale communication.

---

## Methods

The project includes:

- normalized inter-click interval analysis
- coda-duration analysis
- K-means clustering
- silhouette score
- Adjusted Rand Index (ARI)
- Normalized Mutual Information (NMI)
- logistic regression classification
- Stratified Group K-Fold cross-validation
- turn-taking timing analysis
- Wilcoxon signed-rank testing
- mutual-information permutation testing
- Benjamini-Hochberg FDR correction
- robustness analysis across response windows, recordings, and whale-pair contexts

---

## Repository Structure

- `Phase_2_Sperm_Whale_Codas_RESEARCH.ipynb` — main research notebook
- `figures/` — figures used in the research paper
- `whale_acoustics.ipynb` — earlier pilot study using whale audio recordings
- `whale_clustering_results.csv` — results from the earlier pilot analysis

---

## Data

The Phase 2 analysis uses two publicly available datasets:

- `DominicaCodas.csv`
- `sperm-whale-dialogues.csv`

Both are available in the official companion repository for:

Sharma et al. (2024), *Contextual and Combinatorial Structure in Sperm Whale Vocalisations*.

Dataset and original code:
https://github.com/pratyushasharma/sw-combinatoriality

No new acoustic recordings were collected for this study.

---

## Figures

The `figures/` directory contains the main visualizations used in the research paper:

1. Duration distributions of selected coda types
2. Mean rhythmic profiles
3. Clustering performance
4. Turn-taking timing distributions
5. Permutation test for sequential dependence
6. Cross-speaker coda transition probabilities

---

## Limitations

The dialogue coda labels were predicted rather than manually annotated, and the sequential analysis focused on only four selected 5-click coda types.

Non-random sequential association should not be interpreted as semantic translation. Behavioral and social context would be required to investigate the communicative function of individual codas.

---

## Author

**Mansur Gapar**  
Independent Research Project, 2026
