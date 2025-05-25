# Time Series Forecasting of Traffic Flow Using SARIMA

This project applies a Seasonal Autoregressive Integrated Moving Average (SARIMA) model to forecast hourly traffic volume using historical sensor data from California’s freeway network.

## 📌 Project Overview

The goal is to accurately forecast January 2017 traffic volume from Sensor 548 using two years of historical hourly data (2015–2016) provided by the California Department of Transportation's Performance Measurement System (PeMS). 

Key tasks included:
- Data cleaning and feature engineering
- Exploratory data analysis (EDA)
- Seasonal model configuration and evaluation
- Forecasting and residual diagnostics

## 📈 Methodology

The analysis followed a structured forecasting pipeline:

1. **Data Cleaning & Feature Engineering**  
   - Converted timestamps, handled missing/invalid entries  
   - Created time-based features (hour, weekday, holiday, season)

2. **Exploratory Data Analysis**  
   - Identified daily and seasonal traffic patterns  
   - Validated temporal consistency using STL decomposition

3. **Modeling**  
   - Evaluated multiple SARIMA configurations  
   - Selected `SARIMA(1,0,1)(1,1,1)[24]` based on RMSE and residuals

4. **Forecasting**  
   - Trained on 2015–2016 data  
   - Forecasted January 2017 with confidence intervals

## ✅ Results

- **Best Model**: SARIMA(1,0,1)(1,1,1)[24]  
- **RMSE (Forecast)**: 0.01056  
- **MAE**: 0.00727  
- **Correlation**: 0.82  

The model successfully captured short-term fluctuations and strong daily seasonality, delivering accurate and stable forecasts.

## 🔧 Dependencies

- Python 3.10+
- pandas
- numpy
- statsmodels
- matplotlib
- holidays
- pmdarima

You can install them using:
```bash
pip install -r requirements.txt
