# Forecasting Data Trends Using ARIMA, Linear Regression, Polynomial Regression, and LSTM

## 1. Introduction
This project focuses on developing and comparing different models for forecasting/predicting data trends. The models used are:

- **ARIMA (AutoRegressive Integrated Moving Average)**
- **Linear Regression**
- **Polynomial Regression (Degree 3)**
- **LSTM (Long Short-Term Memory)**

## 2. Data Collection
The dataset used for training and testing the models was collected from Yahoo Finance. The steps involved include:

- Used the `yfinance` Python library to fetch historical stock data.
- Selected relevant features such as Open, Close, High, Low, and Volume.
- Performed preprocessing, including handling missing values and feature scaling.
- Split the dataset into training and testing sets for model evaluation.

### Data Collection Code:
```python
import yfinance as yf

data = yf.download('AAPL', start='2020-01-01', end='2024-01-01')
data = data[['Open', 'High', 'Low', 'Close', 'Volume']]
data.dropna(inplace=True)
```

## 3. Model Development

### 3.1 ARIMA Model
Implemented using the `statsmodels` library. Steps:

- Checked stationarity and performed differencing.
- Used ACF and PACF plots to determine AR and MA terms.
- Trained the ARIMA model and optimized parameters.

### 3.2 Linear Regression
Implemented using `scikit-learn`. Steps:

- Defined independent and dependent variables.
- Trained the model using least squares regression.
- Evaluated performance using error metrics.

### 3.3 Polynomial Regression (Degree 3)
Implemented using `PolynomialFeatures` from `scikit-learn`. Steps:

- Generated polynomial features.
- Trained a regression model on transformed data.
- Evaluated performance.

### 3.4 LSTM Model
Implemented using `TensorFlow/Keras`. Steps:

- Transformed time series data into sequences.
- Built an LSTM model with input, hidden, and output layers.
- Trained using Adam optimizer and evaluated results.

## 4. Performance Comparison
The models were evaluated using the following metrics:

- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**

## 5. Installation & Usage

### Requirements
Ensure you have the following dependencies installed:
```bash
pip install yfinance numpy pandas scikit-learn statsmodels tensorflow matplotlib seaborn
```

### Running the Models
Clone the repository and run the scripts:
```bash
git clone https://github.com/LOKESHGOPAL21/Stock_Market_Prices_Prediction
cd forecasting-models
python train_models.py
```

## 6. Contributors
- [LOKESHGOPAL21](https://github.com/LOKESHGOPAL21/)

