# 📈 Apple Stock Price Prediction (2010–2025 & 2018-2025)

This project forecasts Apple's stock price using deep learning models (LSTM), trained on historical data leading up to 2025 — including just before the stock market crash.

## What It Does

- Gathers AAPL stock data from 2010 to March 2025
- Scales and sequences the data for time series prediction
- Trains and compares two LSTM-based models to predict 30 days into the future
- Visualizes predictions alongside historical data
- Calculates RMSE to evaluate model performance

## Dataset

- **Source**: [Yahoo Finance (via yfinance)](https://pypi.org/project/yfinance/)
- Data range: January 2010 – March 2025
- Includes features like Open, High, Low, Close, and Volume

## Techniques Used

- Time series data preprocessing
- MinMaxScaler normalization
- Sequence generation for LSTM input
- LSTM model with two hidden layers and Dense output
- RMSE evaluation and future forecasting

## Tech Stack

- Python, TensorFlow/Keras, NumPy, pandas, yfinance, matplotlib
- Jupyter Notebook (swtiched to Google Colab)

## Results

- Two models were compared — the second model (trained with more historical context) performed significantly better
- **30-day prediction** for April 2025 generated after final training
- RMSE calculated to evaluate model reliability
- Visualizations highlight prediction vs actual price trend before the crash

## Future Improvements

- Integrate news sentiment analysis for more context-aware forecasting
- Build a real-time dashboard with prediction updates
- Compare performance with other models (e.g., ARIMA, Transformer-based)

See notebook for full code, data handling, training process, and visualization.
