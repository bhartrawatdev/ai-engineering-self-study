# MA102 — Main Project: Gradient Descent Visualizer + Linear Regression From Scratch

This is the standalone spec for MA102's Main Project (also summarized in `MA102.md`). Use this file as your working checklist while building.

## Description

A tool that both visualizes gradient descent behavior on a real loss surface and uses it to fit a linear regression model from scratch, with no ML libraries. This project exists to prove the calculus and optimization concepts from this course aren't just formulas you can recite — you've watched the algorithm converge (or fail to) with your own eyes, on your own implementation.

## Requirements

- [ ] Implement gradient descent from scratch (NumPy only, no scikit-learn/statsmodels for the fitting itself) to fit `y = mx + b` to a synthetic, slightly noisy dataset by minimizing mean squared error.
- [ ] Track and plot the loss value at every iteration (the loss-over-time curve).
- [ ] Visualize the fitted line's evolution over training — a plot showing the regression line at several checkpoints (early, middle, converged) overlaid on the data.
- [ ] Visualize the gradient descent path on a contour plot of the loss surface (loss as a function of `m` and `b`), showing the trajectory from initialization to convergence.
- [ ] Run and compare at least 3 different learning rates, clearly showing (via loss curves) one that diverges, one that converges slowly, and one that converges well.

## Suggested File Layout

```
gradient-descent-visualizer/
├── gradient_descent.py   ← the core algorithm, loss function, gradient computation
├── main.py                 ← generates data, runs experiments, produces plots
├── outputs/                 ← saved plots (loss curves, line evolution, contour path)
├── requirements.txt
└── README.md                 ← how to run it + your explanation of the learning rate comparison
```

## Stretch Goals

- [ ] Implement mini-batch gradient descent as an alternative and compare its loss curve's noisiness to full-batch gradient descent on the same data.
- [ ] Extend to a simple 2-feature linear regression (`y = m1*x1 + m2*x2 + b`) and visualize the loss surface as a 3D plot instead of 2D.
- [ ] Compare your from-scratch fitted `m` and `b` against scikit-learn's `LinearRegression` on the same dataset to confirm they closely match.

## What "Done" Looks Like

- The full pipeline runs end-to-end on synthetic data you generate, with no external ML libraries used for the actual fitting.
- Clear, labeled plots exist for: the loss curve across learning rates, the fitted line's evolution, and the gradient descent path on the loss surface's contour plot.
- You can explain, without notes, why the chosen "good" learning rate works better than the too-high and too-low ones, referencing the actual plots.
- Code is organized into functions across at least two files, pushed to this repo's `Projects/` folder with a README containing the key plots.

## Notes on Generating Test Data

Generate synthetic data yourself: pick a "true" `m` and `b`, generate `x` values over a reasonable range, compute `y = m*x + b`, and add a small amount of random Gaussian noise. Knowing the true `m` and `b` in advance lets you directly verify how close your from-scratch fit gets to the real answer, which plain real-world data wouldn't give you.
