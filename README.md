# Genetic Algorithm–Optimized Fuzzy Tipper

A notebook project that uses a genetic algorithm to tune a fuzzy inference system for predicting tip amounts from service and food quality signals.

---

## Overview

This project combines **fuzzy logic** and **evolutionary optimization**. A fuzzy “tipper” system is built as a two-stage inference pipeline:

1. Infer **food quality** and **service quality** from input features (e.g., temperature, flavor, attentiveness).
2. Infer the final **tip** from the intermediate quality scores.

A **genetic algorithm (GA)** is then used to optimize the parameters of the membership functions (triangular shapes) across all variables, with the objective of reducing prediction error.

---

## What the Project Does

* Loads and clips input features, and scales tip targets
* Builds a multi-stage fuzzy inference system (food quality → service quality → tip)
* Represents membership function parameters as a GA chromosome
* Evaluates solutions using mean absolute error (MAE)
* Evolves membership parameters with selection/crossover/mutation to improve performance over a baseline

---

## Tools Used

* Python
* Jupyter Notebook
* NumPy, Pandas
* scikit-fuzzy (fuzzy variables, rules, and inference)
* EasyGA (genetic algorithm implementation)

---

## Files

```
ga_fuzzy_tipper_optimization.ipynb   # Fuzzy system + GA tuning experiments
```

---

## Notes

* The GA optimizes membership function placement/shape (not the fuzzy rule base).
* The notebook reports baseline vs GA-tuned performance to quantify the effect of optimization.
* Designed as an experimental workflow for studying fuzzy systems and evolutionary search.
