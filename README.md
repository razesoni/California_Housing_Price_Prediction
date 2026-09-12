# California Housing Price Prediction

A regression benchmark predicting median house value for California census block groups. This project demonstrates exploratory analysis, missing-value handling, categorical encoding, and comparison of linear and tree-based models.

## Method

1. Inspect the included `housing.csv` dataset and visualize distributions, correlations, and geographic patterns.
2. Split features and target into an 80/20 train/test split with `random_state=42`.
3. Fit median imputation and scaling on training numeric columns only; one-hot encode ocean proximity with unknown-category handling.
4. Compare Linear Regression, Random Forest (200 trees), and Gradient Boosting on the same held-out test set.
5. Export predictions alongside actual values and compare MAE, RMSE, and R².

The notebook creates an income category for visualization. The current split is random, **not income-stratified**.

## Recorded baseline results

These are the previously recorded notebook results, not a fresh benchmark of the current environment.

| Model | MAE | RMSE | R² |
| --- | ---: | ---: | ---: |
| Linear Regression | 50,670.49 | 70,059.19 | 0.6254 |
| Random Forest | 31,465.25 | 48,781.91 | 0.8184 |
| Gradient Boosting | 38,278.15 | 55,903.12 | 0.7615 |

Random Forest has the lowest recorded test error. Currency values refer to the historical dataset, not present-day property valuations.

## Run

Use a separate Python environment. From the repository root:

```bash
python -m pip install -r requirements.txt
python -m jupyterlab California_Housing_Price_Prediction.ipynb
```

Restart the kernel and run all cells in order. The final training cells overwrite the three model prediction CSVs.

## Files

- `California_Housing_Price_Prediction.ipynb`: analysis, preprocessing, training and evaluation
- `housing.csv`: input dataset
- `*_output.csv`: recorded test predictions

## Limitations and next steps

The data represents 1990 census observations and has a capped target. A random geographic split may overestimate generalization to new regions. EDA currently examines the full dataset; reserve a fresh holdout before further tuning. Add spatial validation, cross-validation on training data, residual analysis, and an exported full preprocessing/model pipeline before serving predictions. No deployment or production monitoring is claimed.

Dataset provenance and redistribution terms should be verified against the original source before republishing the data.
