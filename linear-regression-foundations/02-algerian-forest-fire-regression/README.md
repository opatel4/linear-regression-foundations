# Algerian Forest Fire Regression

An end-to-end regression project that predicts the **Fire Weather Index (FWI)** from meteorological measurements and related fire-weather indicators collected in Algeria's Bejaia and Sidi-Bel Abbes regions.

## Workflow

### 1. Exploratory Data Analysis and Feature Engineering

`01_eda_and_feature_engineering.ipynb` performs:

- Raw-data loading and structural inspection
- Region labeling
- Missing-value and data-type checks
- Column-name cleanup
- Fire versus non-fire class preparation
- Distribution and correlation analysis
- Exploratory visualizations
- Export of the cleaned dataset

### 2. Model Training

`02_model_training.ipynb` performs:

- Train/test splitting
- Correlation-based multicollinearity filtering
- Removal of highly correlated `BUI` and `DC` features
- Standard scaling
- Linear Regression
- Lasso and LassoCV
- Ridge and RidgeCV
- Elastic Net and ElasticNetCV

## Notebook Results

The included notebook reports the following test-set results:

| Model | MAE | R² |
|---|---:|---:|
| Linear Regression | 0.547 | 0.985 |
| Lasso | 1.133 | 0.949 |
| LassoCV | 0.620 | 0.982 |
| Ridge | 0.564 | 0.984 |
| RidgeCV | 0.564 | 0.984 |
| Elastic Net | 1.882 | 0.875 |
| ElasticNetCV | 0.658 | 0.981 |

These are results from one 75/25 split with `random_state=42`; they should be treated as project results rather than independent production validation.

## Files

```text
01_eda_and_feature_engineering.ipynb
02_model_training.ipynb
algerian_forest_fires_raw.csv
algerian_forest_fires_cleaned.csv
models/
├── ridge.pkl
└── scaler.pkl
requirements.txt
```

## Setup

```bash
python -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Run `01_eda_and_feature_engineering.ipynb` before `02_model_training.ipynb` when reproducing the full workflow from raw data.

## Model Artifacts

- `models/scaler.pkl`: fitted `StandardScaler`
- `models/ridge.pkl`: fitted Ridge regression model

The artifacts identify scikit-learn version **1.2.0**. Loading pickle files can execute code, so only load artifacts you trust.

## Limitations

- The dataset is small and covers only June–September 2012.
- The evaluation uses one random holdout split rather than repeated or temporal validation.
- Strong R² values may partly reflect the use of variables that are components of, or closely related to, FWI.
- A production version should add a reproducible training script, pipeline object, schema validation, and broader out-of-sample testing.
