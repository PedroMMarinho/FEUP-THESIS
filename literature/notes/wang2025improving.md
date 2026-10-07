# Improving Generalization of Genetic Programming for High-Dimensional Symbolic Regression with Shapley Value Based Feature Selection

- **Citekey:** `wang2025improving`
- **Authors:** Wang, Chunyu; Chen, Qi; Xue, Bing; Zhang, Mengjie
- **Year:** 2025
- **Venue:** Data Science and Engineering, 10(2), 196-211 (journal)
- **DOI:** [10.1007/s41019-024-00270-x](https://doi.org/10.1007/s41019-024-00270-x)
- **PDF:** `literature/papers/04-gp-with-xai/2025_Wang_GP-Shapley-FS.pdf`
- **Theme:** `04-gp-with-xai`
- **Open access:** yes (gold, CC-BY published version)
- **Read status:** to-read

> Fields below mirror the analysis columns in `literature/matrix.csv`.
> Keep both in sync when you finish reading.

## Task type
regression

## Datasets / scenario
10 high-dimensional regression datasets (2 synthetic, 8 real-world)

## Application domain


## Method summary
two-stage: GP runs + Shapley values rank features, keep top log2(D), then standard GPSR

## Advantages
better generalization than standard GP and other GP-FS methods on most datasets, more compact models

## Limitations
higher computational cost (Shapley computation), separate stage rather than integrated

## What it does not solve


## Future work
integrate Shapley into the evolutionary process, cheaper surrogate models, extend to classification

## Relevance to my thesis


## Key quotes / figures to cite


## Ideas for my thesis

