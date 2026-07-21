# ML102 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track.

## Week 1 — Data Quality Foundations: Missing Data, Duplicates & Outliers

1. Why does the *reason* data is missing (MCAR/MAR/MNAR) matter for choosing how to handle it?
2. What information does a "was this value missing" indicator column preserve that pure imputation destroys?
3. Why isn't an outlier automatically something you should remove?

## Week 2 — Encoding Categorical Variables

4. Why is one-hot encoding a genuinely ordered categorical variable a mistake?
5. What specific leakage risk does target/mean encoding introduce, and how do you prevent it?
6. Why does one-hot encoding become a problem with high-cardinality categorical features?

## Week 3 — Scaling, Transforming & Discretizing Numeric Features

7. Why do distance-based models need feature scaling while tree-based models don't?
8. What does a log transform actually do to a right-skewed feature's distribution?
9. Why does robust scaling use median and IQR instead of mean and standard deviation?

## Week 4 — Feature Construction: Interactions, Datetime & Text Basics

10. What's the risk of generating every possible pairwise interaction term instead of a deliberate few?
11. Why does an hour-of-day feature need cyclical (sine/cosine) encoding instead of raw numeric encoding?
12. Why is bag-of-words/TF-IDF described as a "floor" for text features rather than real NLP feature learning?

## Week 5 — Feature Selection: Filter, Wrapper & Embedded Methods

13. Why can filter methods miss features that only matter in combination with others?
14. Why is RFE more expensive than a filter method, and when is that cost worth paying?
15. How does feature selection differ fundamentally from PCA, even though both reduce feature count?

## Week 6 — Data Leakage: The Silent Model Killer

16. What single diagnostic question catches most target leakage?
17. What do imputation leakage, scaling leakage, and target-encoding leakage from earlier weeks all have in common?
18. Why can a plain random train/test split cause temporal leakage on time-ordered data?

## Week 7 — Building Robust Pipelines & Course Integration

19. Why does wrapping preprocessing in a scikit-learn `Pipeline` make leakage-free cross-validation practical rather than just cleaner code?
20. What specific problem does `ColumnTransformer` solve that manual column slicing doesn't?
21. What does "train/serve consistency" mean, and why does saving the fitted pipeline object (not just the code) matter for it?

## Full-Course Gut Check

22. Given a new, genuinely messy tabular dataset, describe — out loud, without notes — the full feature engineering pipeline you'd build end to end: how you'd handle missing data, encode categoricals, scale/transform numerics, select features, and structure it all inside a single leakage-free `Pipeline`. If you can do this comfortably and explain *why* at each step, ML102 is done.
