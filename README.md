# Tanuj_Jog_GDG_Tasks
My solutions for the GDG ML domain (AI-Driven Stock Market Intelligence) problems 1 and 2

                                                                                    TASK 1: STOCK MARKET FORECASTING USING ARIMA

https://colab.research.google.com/drive/1uKs__eMVKf3ChJZgnfchQl7Dz0UNjg0i?usp=sharing

This project implements time-series forecasting of stock prices using the ARIMA (AutoRegressive Integrated Moving Average) model. The notebook demonstrates how historical stock data can be analyzed, modeled, and used to generate short-term forecasts along with uncertainty estimates.

Overview:
Financial time series are noisy and non-stationary. This notebook focuses on:

1.Converting stock prices into log returns (to make it stationary)
2.Testing and enforcing stationarity (ADF - import adfuller)
3.Fitting an ARIMA model to historical data
4.Generating future price forecasts for 7 days
5.Showing confidence intervals

How It Works

1. Data Collection

Historical stock price data is loaded and cleaned (Open, Close, etc).

2. Preprocessing

Prices are converted to log returns to stabilize variance.
Stationarity is checked because ARIMA works only with stationary time series.

3. Model Training

An ARIMA(p, d, q) model is fit to the processed time series.
Model parameters are chosen based on observations in ACF and PACF plots.


4. Forecasting

The model forecasts returns for future time steps.
Returns are cumulatively summed and transformed back into price space.
Confidence intervals are computed and plotted.

5. Visualization

Historical prices vs predicted prices
Highlighted forecast region
Confidence bands for uncertainty estimation


6. Outputs

Historical stock price plot
Forecasted prices for future days
Confidence intervals around predictions


                                                                                    TASK 2:- FINANCIAL CHATBOT USING RAGs
                                                                                    
https://colab.research.google.com/drive/1JfxOFr5k_J5sc7u7kca7WNV6n19k2u4b?usp=sharing

This Colab Notebook represents my attempt to make a financially educated chatbot which:-

1. Identifies ticker based on user query
2. Uses yahoo finance to download dataframe of last two years stock prices
3. Fetches the articles from google news and converts them into embeddings 
4. Tries to find articles relating to query and answers questions.

Model used is Google Gemini 2.5 which I was trying to get to extract ticker as well, which would download a dataframe of that stock.

There are a few drawbacks to the model which I haven't fixed yet (but intend to soon)

1. Unless exact dates are typed, it gives dates between 2022 to 2024
2. It is not a chatbot in the traditional sense because the running of the program is fully dependent on the user's query and to get answer to a new query you need to run all the cells again
3. It is having trouble processing the two year dataframe for more accurate result

