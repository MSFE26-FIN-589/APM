# APM

This repository contains a macroeconomic forecasting project focused on short- to medium-horizon forecasts for U.S. growth and inflation conditions. The work is organized around a set of notebook-based time-series models and supporting data files used to evaluate forecasting performance.

## Project goal

The project centers on forecasting:
- Growth conditions using the ISM New Orders series
- Inflation conditions using CPI-based measures
- A range of benchmark and advanced model families, including AR, dynamic factor models, Bayesian VAR, and regularized forecasting approaches

## Repository structure

- `AR/`  
  Baseline autoregressive forecasting models.
  - `AR_Baseline_Models.ipynb` — AR-based benchmark models for growth and inflation, including stationarity checks, lag selection, and rolling forecast evaluation.

- `DFM/`  
  Dynamic factor modeling notebooks.
  - `DFM_Model_Growth.ipynb` — DFM approach for growth forecasting.
  - `DFM_Model_Inflation.ipynb` — DFM approach for inflation forecasting.

- `Data/`  
  Input datasets used by the models.
  - `Growth_monthly_combined.xlsx`
  - `Growth_raw.xlsx`
  - `Inflation_monthly_combined.xlsx`
  - `Inflation_raw.xlsx`
  - `CPIAUCSL.xlsx`
  - `AR_Model_Data.xlsx`

- `Final Models/`  
  Final forecasting notebooks selected for presentation and evaluation.
  - `BVAR_ISM_Forecast.ipynb` — Bayesian VAR model for ISM-based growth forecasting.
  - `CPI_LassoCV_Forecast.ipynb` — Lasso cross-validation forecast for CPI inflation.

## Modeling workflow

The project follows a typical forecasting pipeline:
1. Load raw macroeconomic data and clean it into monthly time series.
2. Test for stationarity and select an appropriate transformation when needed.
3. Compare model families and lag structures.
4. Run in-sample and out-of-sample validation using rolling or holdout tests.
5. Select the strongest-performing model.
6. Refit on the full sample and generate forward-looking forecasts.

## Key modeling themes

- AR baseline models for simple, interpretable benchmarks
- Dynamic factor models to capture latent macro signals from multiple indicators
- Bayesian VAR forecasting for macroeconomic system dynamics and uncertainty intervals
- Lasso-based regularization for sparse high-dimensional inflation forecasting
- Forecast evaluation using RMSE and other error metrics over relevant horizons

## Data overview

The repository includes both raw and combined macroeconomic datasets in Excel format. These data sources support the growth and inflation forecasting exercises and are used across the notebook workflows.

## How to use this repo

1. Clone the repository.
2. Open the relevant notebook in Jupyter or VS Code.
3. Ensure the required Python libraries are installed.
4. Run the notebook from the repo root so the relative file paths resolve correctly.

Recommended Python stack:
- pandas
- numpy
- matplotlib
- statsmodels
- scikit-learn
- bvar
- openpyxl

## Notes

- This is primarily a research and forecasting notebook repository rather than a packaged application.
- The notebooks are the main source of analysis and final outputs.
- Data files and model notebooks are intended to be used together, with file paths relative to the repo root.

## Summary

APM combines classical time-series methods and modern forecasting techniques to build practical macroeconomic forecasts for growth and inflation. The repo is structured as a modeling workspace for experimentation, validation, and final forecast production.
