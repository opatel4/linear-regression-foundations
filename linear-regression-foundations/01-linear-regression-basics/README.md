# Linear Regression Basics

This introductory project demonstrates the core workflow for simple and multiple linear regression.

## Notebooks

### `01_simple_linear_regression.ipynb`

Uses a small height-and-weight dataset to demonstrate:

- Data inspection and visualization
- Simple linear regression
- Train/test splitting
- Feature scaling
- Prediction and residual analysis
- MAE, MSE, RMSE, and R² evaluation

### `02_multiple_linear_regression.ipynb`

Uses scikit-learn's California Housing dataset to demonstrate:

- Multiple predictor variables
- Correlation analysis
- Standardization
- Multiple linear regression
- Model evaluation and prediction
- Model serialization with Python pickle

## Files

```text
01_simple_linear_regression.ipynb
02_multiple_linear_regression.ipynb
height-weight.csv
requirements.txt
```

## Setup

```bash
python -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Run the notebooks in numerical order.
