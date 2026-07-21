# ML101 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track.

## Week 1 — The ML Landscape & Linear Regression

1. Why is evaluating a model on the same data it was trained on misleading?
2. What's the difference between a feature and a label?
3. Why should scikit-learn's LinearRegression give you results close to your MA102 from-scratch gradient descent implementation?

## Week 2 — Logistic Regression & Classification

4. Despite its name, why is logistic regression a classification algorithm?
5. What does the sigmoid function actually do to a linear model's raw output?
6. Geometrically, what is a decision boundary?
7. Why can accuracy alone be a misleading metric on imbalanced data?

## Week 3 — Bias-Variance Tradeoff & Regularization

8. What's the difference between a high-bias model and a high-variance model?
9. Why can't you detect overfitting from training error alone?
10. What's the practical difference between what L1 and L2 regularization do to model coefficients?
11. Why does increasing regularization strength move a model along the bias-variance tradeoff?

## Week 4 — Decision Trees & Ensemble Methods

12. Why does an unconstrained decision tree tend to overfit badly?
13. In plain terms, how does bagging (as used in random forests) reduce variance?
14. Is a random forest's feature importance the same as causal importance? Why or why not?

## Week 5 — Gradient Boosting & KNN

15. What's the core mechanistic difference between bagging and boosting?
16. Why do gradient boosting libraries treat early stopping as an important control, not an afterthought?
17. What is the "curse of dimensionality," and why does it specifically hurt KNN?

## Week 6 — Support Vector Machines

18. What does an SVM maximize when choosing a decision boundary?
19. What is a support vector, and why do most training points not qualify as one?
20. What does the kernel trick let you do without explicitly transforming your data?

## Week 7 — Unsupervised Learning: Clustering & PCA

21. What assumption does K-Means make about cluster shape, and what happens when that assumption is violated?
22. Why is choosing the "right" k for K-Means somewhat subjective?
23. Beyond visualization, why might you apply PCA before running K-Means?

## Week 8 — Model Selection

24. Why does k-fold cross-validation give a more trustworthy performance estimate than a single train/test split?
25. What's wrong with tuning hyperparameters directly against the final test set?
26. Why isn't "highest accuracy" always the right criterion for choosing a model?

## Full-Course Gut Check

27. Given a new, unfamiliar tabular classification problem, describe — out loud, without notes — how you'd approach it end to end: which 2-3 models you'd try first and why, how you'd evaluate them fairly, and what would make you choose one over another besides raw accuracy. If you can do this comfortably, ML101 is done.
