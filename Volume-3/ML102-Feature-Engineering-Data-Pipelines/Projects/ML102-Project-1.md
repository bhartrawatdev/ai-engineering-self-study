# ML102 — Main Project: Leakage-Free Feature Engineering Pipeline

This is the standalone spec for ML102's Main Project (also summarized in `ML102.md`). Use this file as your working checklist while building.

## Description

Take an intentionally messy, real (not pre-cleaned) tabular dataset and build a single, leakage-free scikit-learn pipeline that handles every stage of feature engineering from raw data to model-ready input, then use it to fairly improve on an ML101-style baseline model. This is the project where "I understand feature engineering" has to survive contact with genuinely messy data and a skeptical leakage audit.

## Requirements

- [ ] Use a real, publicly available tabular dataset with genuine messiness: missing values, mixed numeric/categorical columns, at least one high-cardinality categorical, and at least one skewed numeric feature.
- [ ] Build a single `Pipeline` + `ColumnTransformer` object handling: missing-value imputation (with at least one missing-indicator column), categorical encoding (including a leakage-safe target encoding for the high-cardinality feature), numeric scaling/transformation, and at least 2 domain-driven constructed features.
- [ ] Apply a feature selection step (filter, wrapper, or embedded method) inside the same pipeline.
- [ ] Fit an ML101 classifier (e.g., logistic regression or gradient boosting) at the end of the pipeline, and evaluate with correct k-fold cross-validation of the *entire* pipeline, not just the model.
- [ ] Compare against a "naive" baseline (simple mean imputation, no encoding thought, no constructed features), quantifying the improvement.
- [ ] Log results in the CS105 ML Experiment Tracker.
- [ ] Write a README documenting every preprocessing decision and why it was made, with an explicit leakage-audit section.

## Suggested File Layout

```
leakage-free-feature-pipeline/
├── data/                       ← raw dataset (or a script that downloads it)
├── pipeline.py                 ← Pipeline + ColumnTransformer definition
├── baseline.py                 ← naive baseline for comparison
├── feature_selection.py        ← feature selection step
├── evaluate.py                 ← cross-validation, comparison, leakage checks
├── save_reload_check.py        ← joblib save/reload verification (stretch goal)
├── main.py                     ← ties it together
├── outputs/                    ← saved plots, comparison tables, saved pipeline
├── requirements.txt
└── README.md                   ← decisions, leakage audit, results
```

## Stretch Goals

- [ ] Save the final fitted pipeline with `joblib`, reload it in a separate script, and confirm it reproduces identical predictions on held-out data.
- [ ] Add a deliberately leaky version of the pipeline alongside the correct one, and document the (likely inflated) performance difference as a demonstration.
- [ ] Repeat the comparison using PCA as an alternative to your explicit feature selection step, and note the interpretability/performance tradeoff.

## What "Done" Looks Like

- The entire feature engineering process lives inside one `Pipeline`/`ColumnTransformer` object, with zero manual leakage-prevention code outside it.
- Cross-validated performance is reported for both the engineered pipeline and the naive baseline, with a clear, quantified improvement.
- The README's leakage-audit section could convince a skeptical reviewer that no leakage exists anywhere in the pipeline.
- Results are logged in the CS105 experiment tracker, code is organized into modules, and everything is pushed to this repo's `Projects/` folder.

## Notes on Choosing a Dataset

Pick something genuinely messy rather than a pre-cleaned classroom dataset — housing prices with missing inspection fields, loan applications with a high-cardinality "employer" or "zip code" column, or similar. The messiness is the point: a dataset that's already clean gives you nothing real to engineer.
