# Existing tools to evaluate

"Ver o que ha no mercado (nada de codigo)" - survey only, no implementation yet.
All links checked and returning HTTP 200 on 2025-10-07; versions are the latest on
PyPI at that date.

Legend for the last column: **GA** = genetic algorithm, **GP** = genetic programming,
**SHAP** = Shapley-value based.

| Tool | What it does | Link | Selection method |
|---|---|---|---|
| **sklearn-genetic-opt** (v0.13.3) | scikit-learn compatible GA search; `GAFeatureSelectionCV` evolves the feature subset mask with cross-validated fitness, `GASearchCV` does hyperparameter tuning. Built on top of DEAP. | <https://github.com/rodrigo-arenas/Sklearn-genetic-opt> | **GA** |
| **powershap** (v0.1.0.1) | Wrapper that selects features by testing whether a feature's SHAP importance is statistically significantly above that of an injected random feature, using power analysis to pick the number of iterations. Reference implementation of `verhaeghe2023powershap`. | <https://github.com/predict-idlab/powershap> | **SHAP** |
| **shap-selection** (v0.1.6) | Small utility that ranks and filters features by their SHAP values across models. Written by Wilson E. Marcilio-Jr - it is the reference implementation of `marcilio2020explanations`. | <https://github.com/wilsonjr/SHAP_FSelection> | **SHAP** |
| **BorutaShap** (v1.0.17) | Boruta all-relevant wrapper, but comparing each real feature against shadow (permuted) features using SHAP importance instead of the usual tree importance. | <https://github.com/Ekeany/Boruta-Shap> | **SHAP** (Boruta wrapper) |
| **TPOT** (v1.1.0) | AutoML that uses genetic programming to evolve whole scikit-learn pipelines; feature selection appears as selector operators inside the evolved pipeline rather than as a standalone goal. | <https://github.com/EpistasisLab/tpot> · docs <https://epistasislab.github.io/tpot/> | **GP** (pipeline-level) |
| **gplearn** (v0.4.3) | GP for symbolic regression/classification with a scikit-learn API. `SymbolicTransformer` evolves new features (feature *construction*), which implicitly selects the inputs it uses. Closest off-the-shelf match to GP symbolic regression work like `chen2017feature` / `wang2025improving`. | <https://github.com/trevorstephens/gplearn> · docs <https://gplearn.readthedocs.io/en/stable/> | **GP** (construction, selection as side effect) |
| **DEAP** (v1.4.4) | General evolutionary computation framework (GA, GP, ES, multi-objective). Not a feature-selection tool itself - it is the library you would build a custom GP/GA feature selector on, and what SLUG (`rodrigues2024slug`) and sklearn-genetic-opt build on. | <https://github.com/DEAP/deap> · docs <https://deap.readthedocs.io/en/master/> | **GA + GP** (framework) |

## Observations for the thesis

- **The gap is visible in this table.** Every ready-made tool is either
  GA/GP-based *or* SHAP-based - none combines evolutionary feature selection with
  Shapley-value guidance inside the search. `wang2025improving` does it in a
  research prototype as a two-stage pipeline, not as a released tool.
- **No LIME-based feature selector exists off the shelf.** LIME is used for
  per-instance explanation; turning it into a selection criterion would be
  original work.
- **DEAP is the likely implementation base** if the thesis builds a custom
  selector, since both SLUG and sklearn-genetic-opt already sit on it.
- **powershap and BorutaShap are the baselines to beat** on the SHAP side;
  `GAFeatureSelectionCV` on the GA side.

## Note

`sklearn-genetic-opt` previously documented itself on Read the Docs, but
`sklearn-genetic-opt.readthedocs.io` now returns 404. Use the GitHub README and
the PyPI page (<https://pypi.org/project/sklearn-genetic-opt/>) instead.
