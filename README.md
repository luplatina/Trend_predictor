# Trend_predictor
Time series regression model, Use ARIMA model to predict the diabetes clinical trials tendency.

## Overview
This project to use time series analysis tool ARIMA to investigate the start dates of clinical trials targeting diabetes from 
clinicaltrial.gov. The main function is to forecast the diabetes clinical trials that going to launch in the near future.

## Procedure
The general procedure of this project includes:
1. quick explore the diabetes clinicaltrial data. use pandas dataframe catologued clinical trial starting dates.
2. test the stantionary of the time series data; use auto correlation and partial auto correlation to evaluate AR, AM setting.
3. train ARIMA model, and use the model prediction on test set to evaluate the model accuracy.

ARIMA stands for : 
AR(p), auto regression, captures the persistence of past history(p).
MA(q), moving average, captures the persistence of past shocks(q).
I(d), integrate, indicate the order of difference(d) to make the series stationary.

Pandas have very convinient package to deal time series data; The time series analysis is mainly implemented by statsmodels. One thing need to keep in mind is that statsmodels usually require index of dataframe to be time data.
The stationary of the time series data is critical presumption for ARIMA model. It can be calculated by Dickey-Fuller unit root test. The order of AR and MA can be evalutated by auto corralation and partial auto correlation diagrams.

The forcasting trend of diabetes trials was ploted to compare the test data and show the model accuracy.

![trial_trend](https://cloud.githubusercontent.com/assets/19654472/25076359/2a29f7f6-22ee-11e7-8b73-1e30abb0a44c.png)
