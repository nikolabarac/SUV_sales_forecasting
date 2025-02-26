# SUV Sales Forecasting  

## Project Overview  
This project focuses on forecasting SUV sales using time series models. The goal is to analyze historical sales data and build predictive models to estimate future sales trends.  

## Models Used  
The following time series forecasting models were implemented:  
- **ARIMA** (AutoRegressive Integrated Moving Average)  
- **ETS** (Error, Trend, Seasonality)  
- **STL + ETS** (Seasonal and Trend decomposition using Loess with ETS)  
- **Automatic ARIMA Selection**  

## Data Inspection  
To determine the optimal parameters for the Seasonal ARIMA model, I manually examined ACF (AutoCorrelation Function) and PACF (Partial AutoCorrelation Function) plots. Both seasonal differencing (d=0, D=1) and combined seasonal and regular differencing (d=1, D=1) models were explored.  

## Residual Diagnostics  
Residual analysis was performed to assess the model assumptions. The goal was to check whether the residuals followed a white noise pattern, indicating a well-fitted model.  

## Model Evaluation & Selection  
Based on test errors, the best-performing models were:  
- **ARIMA (3,0,0)(2,1,0)**  
- **STL + ETS**  
- **Automatic ARIMA Step/ARIMA Comp models**  

Even though the ARIMA (3,0,0)(2,1,0) model did not have white noise residuals, it was selected as the final model due to its superior test error performance.  

## Libraries Used  
The **fpp3** package was used, which includes all the necessary libraries for time series analysis in R.  

## Conclusion  
This project demonstrates the process of time series forecasting using different models and evaluating their effectiveness. The selected model can be used to predict future SUV sales trends, assisting businesses in inventory planning and market strategy.   
