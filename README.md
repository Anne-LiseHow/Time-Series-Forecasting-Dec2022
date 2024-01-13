# Time-Series-Forecasting
This repository contains the implementation of machine learning models in Python to forecast the weather in a particular city. Data is confidential and therefore cannot be uploaded here. The measurements have been recorded at one minute interval and models for prediction in 5, 10, 15, 30 minutes and 1,2,6,12 hours in the future have been developped.

## Data Cleaning
The following data cleaning processes were conducted:
* Check for NULL values
* Check and remove duplicate values
* Convert the time variable to a suitable data type
* Check if record is available for each minute and impute using appropriate imputation methods
* Denoise the time series
* Select data according time interval prediction
* Normalise data using: StandardScaler, MinMaxScaler, Normalisation
* Split into data into input and output

## Support Vector Regression
Support Vector Regression has implemented and optimised using Grid Search. Pre-processing the data using the Min-Max Scaler has the best predictive performance. The R\<sup>2</sup> values show that around 90% of variance is retained by the model for most of the features.

## Artificial Neural Network
Three Artificial Neural Networks: MLP, Bi-LSTM, CNN have been implemented and optimised using Bayesian Optimisation. Out of the three models, Bi-LSTM achieved the best forecasting performance with StandardScaler as pre-processing, indicated by the average R\<sup>2</sup> value of 0.9 and low MSE and MAE values. A decrease in predictive capability can be noticed as the interval prediction gets larger. 
