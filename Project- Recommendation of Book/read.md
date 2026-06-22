# Power Demand Forecasting

## Project Overview
Forecast hourly power demand using machine learning models.

## Features
- Data preprocessing
- Feature engineering
- Model training
- Forecast visualization
- Streamlit deployment

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

  SARIMAX Results                                      
==========================================================================================
Dep. Variable:                            PJMW_MW   No. Observations:                 1000
Model:             SARIMAX(1, 1, 1)x(1, 1, 1, 24)   Log Likelihood               -5369.313
Date:                            Mon, 22 Jun 2026   AIC                          10748.627
Time:                                    12:12:04   BIC                          10772.904
Sample:                                03-16-2015   HQIC                         10757.877
                                     - 04-27-2015                                         
Covariance Type:                              opg                                         
==============================================================================
                 coef    std err          z      P>|z|      [0.025      0.975]
------------------------------------------------------------------------------
ar.L1          0.4291      0.044      9.766      0.000       0.343       0.515
ma.L1          0.1069      0.050      2.150      0.032       0.009       0.204
ar.S.L24       0.1331      0.025      5.272      0.000       0.084       0.183
ma.S.L24      -0.9078      0.019    -47.964      0.000      -0.945      -0.871
sigma2      4643.8861    195.492     23.755      0.000    4260.729    5027.043
===================================================================================
Ljung-Box (L1) (Q):                   0.03   Jarque-Bera (JB):                20.73
Prob(Q):                              0.87   Prob(JB):                         0.00
Heteroskedasticity (H):               0.94   Skew:                            -0.02
Prob(H) (two-sided):                  0.58   Kurtosis:                         3.72
===================================================================================

MODEL COMPARISON (sorted by RMSE, lower = better)
==================================================
                    RMSE       MAE  MAPE (%)      R2
XGBoost          226.254   168.932     2.815   0.950
LightGBM         226.854   172.923     2.894   0.950
Random Forest    298.143   231.334     3.935   0.914
Baseline Model   876.312   657.639    11.165   0.256
SARIMA          4318.087  3705.504       NaN -17.064

Best model: XGBoost

## Run Locally

pip install -r requirements.txt
streamlit run app2.py
