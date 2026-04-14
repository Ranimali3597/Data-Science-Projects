Monthly Milk Production Forecasting using RNN, LSTM, and GRU

Problem Statement:
Forecast future monthly milk production based on historical time series data using deep learning models.

Dataset:
Monthly milk production dataset
Time-based sequential data
Features: Month, Production values

Steps Performed:
Data Cleaning and Preprocessing
Time Series Visualization
Sequence/Window Creation

Model Building using:
RNN
LSTM
GRU
Model Training and Prediction
Performance Comparison of Models:
	Compare the performance of RNN, LSTM, and GRU.
i) RNN:
Predicted next month's milk production: 818.47

ii)LSTM:
Predicted next month's milk production: 812.10

iii)GRU:
Predicted next month's milk production: 786.72

Best Model: RNN
The RNN model produced the most accurate forecasts based on evaluation metrics and predicts 
the next month’s milk production to be approximately 818.47 units. LSTM and GRU models also generated 
similar predictions, indicating consistency across models, but with slightly lower accuracy. 
Therefore, the RNN model is selected as the final model for forecasting.

Business Insight:
Expected production ≈ 800–820 units
Helps in:
Inventory planning
Supply chain optimization
Demand forecasting
 Predictions are consistent
RNN is best-performing model
Final forecast ≈ 818 units

Tools & Technologies:
Python
NumPy, Pandas
TensorFlow / Keras
Matplotlib

Visualizations:
Actual vs Predicted Graphs
Model comparison plots
