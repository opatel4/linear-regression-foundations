# Regression Modeling

A progressive collection of regression projects, beginning with core linear-regression concepts and advancing to an end-to-end machine-learning workflow for predicting the Fire Weather Index (FWI).

## Projects

### 1. Linear Regression Basics

Introduces simple and multiple linear regression through:

- Height prediction from weight data
- California housing-value prediction
- Train/test splitting and feature scaling
- Model evaluation with MAE, MSE, RMSE, and R²

[Open the project](./01-linear-regression-basics)

### 2. Algerian Forest Fire Regression

Builds a more complete machine-learning workflow using weather and fire-index data from two Algerian regions:

- Data cleaning and regional labeling
- Exploratory data analysis and visualization
- Feature engineering and correlation analysis
- Multicollinearity filtering
- Standardization
- Linear, Lasso, Ridge, and Elastic Net regression
- Cross-validated regularization models
- Serialized Ridge model and fitted scaler

[Open the project](./02-algerian-forest-fire-regression)

## Repository Structure

```text
.
├── 01-linear-regression-basics/
│   ├── 01_simple_linear_regression.ipynb
│   ├── 02_multiple_linear_regression.ipynb
│   ├── height-weight.csv
│   ├── README.md
│   └── requirements.txt
├── 02-algerian-forest-fire-regression/
│   ├── 01_eda_and_feature_engineering.ipynb
│   ├── 02_model_training.ipynb
│   ├── algerian_forest_fires_raw.csv
│   ├── algerian_forest_fires_cleaned.csv
│   ├── models/
│   │   ├── ridge.pkl
│   │   └── scaler.pkl
│   ├── README.md
│   └── requirements.txt
└── README.md
```

## Running a Project

Create a separate environment for the project you want to run, install its requirements, and launch Jupyter:

```bash
cd 01-linear-regression-basics  # or the second project
python -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

## Notes

- Run each notebook from within its own project directory so relative dataset paths resolve correctly.
- The serialized `.pkl` files were created with scikit-learn 1.2.0. Only load model artifacts from trusted sources.
- Reported metrics are notebook results from the included data split and should not be interpreted as external production validation.

## Author

**Om Patel**  
Quantitative Finance student at Stevens Institute of Technology
