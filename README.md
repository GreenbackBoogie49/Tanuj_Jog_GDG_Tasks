# Tanuj_Jog_GDG_Tasks
My solutions for the GDG ML domain (AI-Driven Stock Market Intelligence) problems 1 and 2

📈 Stock Market Forecasting Using ARIMA

This project implements time-series forecasting of stock prices using the ARIMA (AutoRegressive Integrated Moving Average) model. The notebook demonstrates how historical stock data can be analyzed, modeled, and used to generate short-term forecasts along with uncertainty estimates.

🧠 Overview

Financial time series are noisy and non-stationary. This notebook focuses on:

Converting stock prices into log returns

Testing and enforcing stationarity

Fitting an ARIMA model to historical data

Generating future price forecasts

Visualizing predictions alongside actual market data

Interpreting confidence intervals and volatility behavior

🚀 How It Works

1. Data Collection

Historical stock price data is loaded (Open, Close, etc.).

Missing values are handled and unnecessary columns removed.


2. Preprocessing

Prices are converted to log returns to stabilize variance.

Stationarity assumptions are checked.

Differencing is applied if required.


3. Model Training

An ARIMA(p, d, q) model is fit to the processed time series.

Model parameters are chosen based on diagnostics and residual behavior.


4. Forecasting

The model forecasts returns for future time steps.

Returns are cumulatively summed and transformed back into price space.

Confidence intervals are computed and plotted.


5. Visualization

Historical prices vs predicted prices

Highlighted forecast region

Confidence bands for uncertainty estimation


📊 Outputs

📉 Historical stock price plot

📈 Forecasted prices for future days

🌫️ Confidence intervals around predictions


🛠️ Requirements

This notebook runs on Google Colab. Required libraries include:

pandas

numpy

matplotlib

statsmodels

yfinance 


