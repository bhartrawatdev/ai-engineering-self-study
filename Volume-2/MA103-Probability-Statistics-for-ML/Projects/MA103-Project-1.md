# MA103 — Main Project: A/B Test Analysis Tool

This is the standalone spec for MA103's Main Project (also summarized in `MA103.md`). Use this file as your working checklist while building.

## Description

A small, reusable tool for analyzing A/B test results — simulating realistic test data, running the appropriate statistical test, and correctly interpreting and visualizing the result. This project exists to turn hypothesis testing from formulas into a tool you'd actually trust using on a real decision.

## Requirements

- [ ] Simulate synthetic A/B test data for two variants, with a configurable true difference in effect (including the ability to simulate *no* real difference, to test for false positives).
- [ ] Implement a function that runs the appropriate statistical test given the data type (two-sample t-test for continuous metrics, chi-squared or z-test for proportions).
- [ ] Compute and report: the p-value, a 95% confidence interval for the difference between groups, and the observed effect size.
- [ ] Visualize the two groups' distributions (or sampling distributions of their means/proportions) side by side, clearly showing overlap or separation.
- [ ] Write a plain-language interpretation function that produces a correct, appropriately-hedged summary sentence from the statistical results — avoiding common p-value/confidence-interval misinterpretations.

## Suggested File Layout

```
ab-test-analyzer/
├── simulate.py            ← generates synthetic A/B test data
├── analyze.py               ← runs the appropriate statistical test, computes CI/effect size
├── interpret.py               ← plain-language interpretation of results
├── visualize.py                 ← distribution comparison plots
├── main.py                        ← ties it together, runs an example analysis
├── outputs/                         ← saved example plots
├── requirements.txt
└── README.md                         ← how to run it + example output/interpretation
```

## Stretch Goals

- [ ] Run a "false positive rate" simulation: repeatedly generate A/B tests with no true difference, run your tool on each, and empirically confirm roughly 5% incorrectly report p < 0.05 — a direct demonstration of Type I error.
- [ ] Add a simple power analysis component: given a desired effect size and significance level, estimate the sample size needed to reliably detect it.
- [ ] Extend to more than 2 variants (A/B/C testing) using an appropriate multi-group test (e.g. ANOVA), noting why running multiple pairwise t-tests instead would inflate the false positive rate.

## What "Done" Looks Like

- The tool correctly identifies a real, simulated difference as statistically significant in most runs, and correctly fails to find significance in most runs where there's no true difference.
- The plain-language interpretation output is accurate and doesn't misstate what the p-value or confidence interval actually claims.
- You can explain, without notes, why the false-positive-rate stretch goal (or a manual equivalent) demonstrates Type I error concretely rather than abstractly.
- Code is organized into functions across multiple files, pushed to this repo's `Projects/` folder with a README including example output and interpretation.

## Notes on Simulating Data

Build the simulation so the "true" underlying difference is a parameter you control (e.g., `simulate_ab_test(true_diff=0.05, n=1000)`). Knowing the ground truth is what lets you actually verify your tool works correctly — real A/B test data never comes with a "true difference" you can check your answer against, so this synthetic control is the whole point during development.
