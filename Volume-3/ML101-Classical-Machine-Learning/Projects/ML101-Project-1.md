# ML101 — Main Project: Tabular Classification Model Comparison

This is the standalone spec for ML101's Main Project (also summarized in `ML101.md`). Use this file as your working checklist while building.

## Description

A rigorous, end-to-end comparison of multiple classical ML models on a real (not synthetic) tabular classification dataset, using proper methodology throughout — cross-validation, no test-set leakage, and a genuine, reasoned model recommendation at the end. This is the kind of analysis you'd actually present to justify a model choice in a real setting, not a toy exercise.

## Requirements

- [ ] Use a real, publicly available tabular dataset (UCI Machine Learning Repository, Kaggle, etc.) with a genuine classification target.
- [ ] Perform basic exploratory data analysis and necessary preprocessing (missing values, categorical encoding).
- [ ] Fit and fairly compare at least 4 model types: logistic regression, random forest, gradient boosting (XGBoost/LightGBM), and at least one of SVM or KNN.
- [ ] Use k-fold cross-validation for the comparison; the held-out test set is touched only once, at the very end.
- [ ] Tune the best-performing model's hyperparameters using `GridSearchCV` or `RandomizedSearchCV`.
- [ ] Report results beyond just accuracy — at minimum, a confusion matrix with brief interpretation.
- [ ] Log this project's model comparisons using the CS105 ML Experiment Tracker.
- [ ] Write a README summarizing the dataset, methodology, and a real, justified model recommendation (not just "highest accuracy").

## Suggested File Layout

```
tabular-model-comparison/
├── data/                     ← raw dataset (or a script that downloads it)
├── preprocessing.py            ← EDA + cleaning + encoding
├── models.py                     ← model definitions, cross-validation comparison
├── tuning.py                       ← hyperparameter search for the winning model
├── evaluate.py                       ← confusion matrix, final test-set evaluation
├── main.py                             ← ties it together
├── outputs/                             ← saved plots, comparison tables
├── requirements.txt
└── README.md                             ← dataset, methodology, recommendation
```

## Stretch Goals

- [ ] Extract and visualize feature importances from tree-based models, checking alignment with domain intuition.
- [ ] Repeat the comparison after applying PCA for dimensionality reduction; note any change in performance or training time.
- [ ] Add a naive baseline (always predict majority class) to the comparison table for context.

## What "Done" Looks Like

- The full comparison runs end-to-end on real data, with cross-validation used correctly and no test-set leakage into model selection.
- Results are logged in the CS105 experiment tracker with real hyperparameters and metrics recorded, not just printed and discarded.
- You can justify your final model recommendation out loud, referencing specific tradeoffs (accuracy vs. interpretability vs. cost).
- Code is organized into modules, pushed to this repo's `Projects/` folder with a README containing the full comparison and recommendation.

## Notes on Choosing a Dataset

Pick something with a real, interpretable classification question — customer churn, loan default, disease diagnosis, etc. — rather than an already heavily-cleaned "toy" dataset like Iris; a dataset that requires at least some real preprocessing decisions (missing values, mixed categorical/numeric features) makes the comparison far more representative of real work.
