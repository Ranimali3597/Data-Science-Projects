# Power Demand Forecasting

## Project Overview

Forecast hourly power demand using machine learning models.
1. Power Demand Forecasting (Highly Recommended)

Since you've recently worked on time-series forecasting, create a project with:

Data cleaning and feature engineering


## Features

- Data preprocessing
- Feature engineering
- Model training
- Forecast visualization:
  XGBoost
  LightGBM
  Random Forest
  ARIMA
  SARIMA

- Model comparison
- Streamlit deployment
- Future demand prediction

## Technologies
streamlit
pandas
numpy
plotly
scikit-learn
xgboost
lightgbm
matplotlib
statsmodels
openpyxl
holidays

## Results

XGBoost
  RMSE     : 226.25 MW
  MAE      : 168.93 MW
  MAPE     : 2.82%
  R2 Score : 0.950

Random Forest
  RMSE     : 298.14 MW
  MAE      : 231.33 MW
  MAPE     : 3.94%
  R2 Score : 0.914
LightGBM
  RMSE     : 226.85 MW
  MAE      : 172.92 MW
  MAPE     : 2.89%
  R2 Score : 0.950
Baseline Model
  RMSE     : 876.31 MW
  MAE      : 657.64 MW
  MAPE     : 11.16%
  R2 Score : 0.256
SARIMA
  RMSE     : 4318.09 MW
  MAE      : 3705.50 MW
  MAPE     : nan%
  R2 Score : -17.064

 SARIMAX Results:
 
| Parameter          | Value                       |
| ------------------ | --------------------------- |
| Dependent Variable | PJMW_MW                     |
| Observations       | 1000                        |
| Model              | SARIMAX(1,1,1) × (1,1,1,24) |
| Log Likelihood     | -5369.313                   |
| AIC                | 10748.627                   |
| BIC                | 10772.904                   |
| HQIC               | 10757.877                   |
| Sample Period      | 16-Mar-2015 to 27-Apr-2015  |
| Covariance Type    | OPG                         |

==============================================================================

Model Coefficients:

| Variable        | Coefficient | Std. Error | z-Statistic | P-value | 95% CI Lower | 95% CI Upper |
| --------------- | ----------: | ---------: | ----------: | ------: | -----------: | -----------: |
| AR(1)           |      0.4291 |      0.044 |       9.766 |   0.000 |        0.343 |        0.515 |
| MA(1)           |      0.1069 |      0.050 |       2.150 |   0.032 |        0.009 |        0.204 |
| Seasonal AR(24) |      0.1331 |      0.025 |       5.272 |   0.000 |        0.084 |        0.183 |
| Seasonal MA(24) |     -0.9078 |      0.019 |     -47.964 |   0.000 |       -0.945 |       -0.871 |
| Sigma²          |   4643.8861 |    195.492 |      23.755 |   0.000 |     4260.729 |     5027.043 |


===================================================================================

Diagnostic Statistics:
| Diagnostic Test            | Value |
| -------------------------- | ----: |
| Ljung-Box (Q) Statistic    |  0.03 |
| Ljung-Box p-value          |  0.87 |
| Jarque-Bera (JB) Statistic | 20.73 |
| Jarque-Bera p-value        |  0.00 |
| Heteroskedasticity (H)     |  0.94 |
| Heteroskedasticity p-value |  0.58 |
| Skewness                   | -0.02 |
| Kurtosis                   |  3.72 |


===================================================================================

MODEL COMPARISON (sorted by RMSE, lower = better)

Best model: XGBoost

| Model          |   RMSE ↓ |    MAE ↓ | MAPE (%) ↓ |    R² ↑ |
| -------------- | -------: | -------: | ---------: | ------: |
| XGBoost        |  226.254 |  168.932 |      2.815 |   0.950 |
| LightGBM       |  226.854 |  172.923 |      2.894 |   0.950 |
| Random Forest  |  298.143 |  231.334 |      3.935 |   0.914 |
| Baseline Model |  876.312 |  657.639 |     11.165 |   0.256 |
| SARIMA         | 4318.087 | 3705.504 |        N/A | -17.064 |


## Run Locally

pip install -r requirements.txt

streamlit run app2.py
