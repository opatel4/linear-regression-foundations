# Linear Regression Foundations

Educational Jupyter notebooks demonstrating simple and multiple linear regression workflows with Python and scikit-learn.

## Contents

### Simple Linear Regression

`simple_linear_regression.ipynb` uses a small height-and-weight dataset to demonstrate:

- Exploratory visualization
- Train/test splitting
- Feature standardization
- Fitting a `LinearRegression` model
- Interpreting the coefficient and intercept
- Generating predictions
- Evaluating model performance

### Multiple Linear Regression

`multiple_linear_regression.ipynb` uses scikit-learn's California Housing dataset to demonstrate:

- Dataset exploration and descriptive statistics
- Correlation analysis and visualization
- Preparing multiple predictor variables
- Train/test splitting and feature scaling
- Fitting a multiple linear regression model
- Prediction and evaluation

## Repository Structure

```text
.
├── simple_linear_regression.ipynb
├── multiple_linear_regression.ipynb
├── height-weight.csv
├── requirements.txt
└── README.md
```

## Getting Started

1. Clone the repository.
2. Create and activate a Python virtual environment.
3. Install the dependencies:

```bash
pip install -r requirements.txt
```

4. Start Jupyter Notebook:

```bash
jupyter notebook
```

5. Open either notebook and run the cells in order.

## Technologies

- Python
- pandas
- NumPy
- Matplotlib
- seaborn
- scikit-learn
- Jupyter Notebook

## Project Status

This repository contains foundational machine-learning exercises prepared as part of my progression from introductory regression concepts toward more advanced quantitative-finance and machine-learning projects.

## Notes

The simple regression notebook expects `height-weight.csv` to remain in the repository root. The California Housing dataset is downloaded through scikit-learn when the multiple regression notebook runs.
