# Stock-Market-Prices-Prediction-Using-Machine-Learning-and-Deep-Learning

# Introduction
Predicting stock market performance is a challenging task due to the volatile nature of share prices influenced by various factors, including both rational and irrational behavior. This project demonstrates how machine learning and deep learning techniques can be applied to historical stock price data to forecast future prices.

# Models Implemented
Moving Average
Linear Regression
k-Nearest Neighbours
Auto ARIMA
Prophet
Long Short Term Memory (LSTM)

# Dataset
The dataset includes the following columns:
Date,Open,High,Low
Last,Close,Total Trade Quantity,Turnover
The closing price is used as the target variable for predictions. 

# Techniques Used
# Moving Average
The moving average technique predicts the closing price for each day based on the average of a set of previously observed values. This section demonstrates how to implement moving averages in Python.

# Linear Regression
Linear regression analyzes the relationship between date features and closing prices. It involves feature engineering to extract relevant date components and uses them to build the model.

# k-Nearest Neighbours
kNN predicts the closing prices by finding the average of the k closest historical points. This section provides a walkthrough of the implementation and evaluation of the kNN model.

# Auto ARIMA
ARIMA is a powerful statistical method for time series forecasting. This section utilizes auto ARIMA to automatically select the best parameters for the ARIMA model to forecast stock prices.

# Prophet
Prophet is a time series forecasting tool developed by Facebook, which simplifies the forecasting process without extensive data preprocessing. This section outlines how to implement the Prophet model on stock data.

# Long Short Term Memory (LSTM)
LSTMs are advanced recurrent neural networks suitable for sequence prediction tasks. This section describes how to implement LSTM to predict stock prices and evaluates its performance.

# Conclusion
The project illustrates various techniques for predicting stock prices using machine learning and deep learning approaches. Despite achieving varying levels of accuracy, it emphasizes that stock price movements are influenced by unpredictable external factors, making forecasting inherently challenging.
