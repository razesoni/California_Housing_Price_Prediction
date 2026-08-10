# California Housing Price Prediction

[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E.svg?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/pandas-150458.svg?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview

This project builds and benchmarks regression models to predict **median house value** for California districts using the classic 1990 California Census housing dataset. Beyond fitting a model, the goal is to demonstrate a complete, defensible data science workflow:

*   **Exploratory Data Analysis (EDA)** to understand distributions, correlations, and data quality issues
*   **Feature Engineering** to convert raw census fields into model-ready signals (e.g., income stratification, geospatial context)[cite: 1]
*   **Preprocessing Pipelines** built with `scikit-learn`'s `Pipeline` and `ColumnTransformer` to avoid data leakage and ensure reproducibility[cite: 1]
*   **Model Benchmarking** across a linear baseline and two ensemble tree methods (Random Forest, Gradient Boosting)[cite: 1]
*   **Evaluation** using MAE, MSE, RMSE, and R² to translate model performance into business-relevant insights[cite: 1]

**Dataset:** `housing.csv` — 1990 California census data at the block-group ("district") level, with features including geographic coordinates, housing age, room/bedroom counts, population, households, median income, and proximity to the ocean[cite: 1]. The target variable is `median_house_value`[cite: 1].

---

## 🛠️ Project Architecture & Workflow

```text
├── housing.csv               # Raw 1990 California Census dataset
├── housing_prediction.ipynb  # End-to-end Jupyter Notebook (EDA -> Pipeline -> Modeling)
└── README.md                 # Project documentation
