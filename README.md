<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README - Model Development</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            padding: 20px;
            background-color: #f4f4f4;
        }
        h1, h2, h3 {
            color: #333;
        }
        pre {
            background: #eee;
            padding: 10px;
            border-radius: 5px;
            overflow-x: auto;
        }
    </style>
</head>
<body>
    <h1>README - Model Development</h1>
    
    <h2>1. Introduction</h2>
    <p>This project focuses on developing and comparing different models for forecasting/predicting data trends. The models used are:</p>
    <ul>
        <li>ARIMA (AutoRegressive Integrated Moving Average)</li>
        <li>Linear Regression</li>
        <li>Polynomial Regression (Degree 3)</li>
        <li>LSTM (Long Short-Term Memory)</li>
    </ul>
    
    <h2>2. Data Collection</h2>
    <p>The dataset used for training and testing the models was collected from Yahoo Finance. Steps involved:</p>
    <ul>
        <li>Used the <code>yfinance</code> Python library to fetch historical stock data.</li>
        <li>Selected relevant features such as Open, Close, High, Low, and Volume.</li>
        <li>Performed preprocessing, including handling missing values and feature scaling.</li>
        <li>Split the dataset into training and testing sets for model evaluation.</li>
    </ul>
    <pre>
    import yfinance as yf
    data = yf.download('AAPL', start='2020-01-01', end='2024-01-01')
    data = data[['Open', 'High', 'Low', 'Close', 'Volume']]
    data.dropna(inplace=True)
    </pre>
    
    <h2>3. Model Development</h2>
    <h3>3.1 ARIMA Model</h3>
    <p>Implemented using the <code>statsmodels</code> library. Steps:</p>
    <ul>
        <li>Checked stationarity and performed differencing</li>
        <li>Used ACF and PACF plots to determine AR and MA terms</li>
        <li>Trained the ARIMA model and optimized parameters</li>
    </ul>

    <h3>3.2 Linear Regression</h3>
    <p>Implemented using <code>scikit-learn</code>. Steps:</p>
    <ul>
        <li>Defined independent and dependent variables</li>
        <li>Trained the model using least squares regression</li>
        <li>Evaluated performance using error metrics</li>
    </ul>

    <h3>3.3 Polynomial Regression (Degree 3)</h3>
    <p>Implemented using <code>PolynomialFeatures</code> from <code>scikit-learn</code>. Steps:</p>
    <ul>
        <li>Generated polynomial features</li>
        <li>Trained a regression model on transformed data</li>
        <li>Evaluated performance</li>
    </ul>
    
    <h3>3.4 LSTM Model</h3>
    <p>Implemented using <code>TensorFlow/Keras</code>. Steps:</p>
    <ul>
        <li>Transformed time series data into sequences</li>
        <li>Built an LSTM model with input, hidden, and output layers</li>
        <li>Trained using Adam optimizer and evaluated results</li>
    </ul>
    
    <h2>4. Performance Comparison</h2>
    <p>The models were evaluated using the following metrics:</p>
    <ul>
        <li>Mean Absolute Error (MAE)</li>
        <li>Mean Squared Error (MSE)</li>
        <li>Root Mean Squared Error (RMSE)</li>
        <li>R² Score</li>
    </ul>
    <pre>
ARIMA Performance:
MAE: 1.1887, MSE: 3.7155, RMSE: 1.9276, R² Score: 0.9991

Linear Regression Performance:
MAE: 17.9300, MSE: 484.0622, RMSE: 22.0014, R² Score: 0.8877

Polynomial Regression (Degree 3) Performance:
MAE: 10.8805, MSE: 197.9070, RMSE: 14.0679, R² Score: 0.9541

LSTM Performance:
MAE: 4.6599, MSE: 37.1658, RMSE: 6.0964, R² Score: 0.9501
    </pre>
    
    <h2>5. Conclusion</h2>
    <p>From the comparison, the best-performing model is:</p>
    <ul>
        <li><strong>ARIMA</strong> - Best for short-term forecasting with highest R² score.</li>
        <li><strong>Polynomial Regression (Degree 3)</strong> - Outperforms linear regression and closely follows data trends.</li>
        <li><strong>LSTM</strong> - Suitable for long-term predictions and time series patterns.</li>
    </ul>
    
    <h2>6. Future Improvements</h2>
    <ul>
        <li>Optimize ARIMA parameters using Grid Search.</li>
        <li>Experiment with higher-degree Polynomial Regression.</li>
        <li>Enhance LSTM by adding attention mechanisms and hyperparameter tuning.</li>
        <li>Try hybrid models (e.g., ARIMA + LSTM) for better accuracy.</li>
    </ul>

    <h2>7. Installation and Usage</h2>
    <p>To run the models, install the required libraries:</p>
    <pre>
    pip install numpy pandas scikit-learn statsmodels tensorflow keras yfinance
    </pre>
    <p>Execute the corresponding scripts for each model.</p>
    
    <h2>8. References</h2>
    <ul>
        <li>Yahoo Finance API: <a href="https://pypi.org/project/yfinance/">https://pypi.org/project/yfinance/</a></li>
        <li>Scikit-learn Documentation: <a href="https://scikit-learn.org/">https://scikit-learn.org/</a></li>
        <li>TensorFlow Documentation: <a href="https://www.tensorflow.org/">https://www.tensorflow.org/</a></li>
    </ul>
</body>
</html>
