# Stock Price Forecasting with LSTM

This project demonstrates stock price prediction using **Long Short-Term Memory (LSTM)** networks, a deep learning model designed to handle time-series data. The model predicts future stock prices based on historical closing prices, using **Apple Inc. (AAPL)** stock data from Yahoo Finance.

## Features

- **Stock Data Collection**: Downloads historical stock data for Apple (AAPL) using `yfinance`.
- **Data Preprocessing**: Scales the closing price data to a range of [0, 1] using **MinMaxScaler**.
- **LSTM Model**: A deep learning model is built using **Keras** to predict the future stock price based on the past 60 days' closing prices.
- **Prediction and Evaluation**: The model evaluates the stock prices using Root Mean Squared Error (RMSE) and plots the training, validation, and predicted stock prices.
- **Real-Time Prediction**: The model predicts the next day's stock price based on the last 60 days' data.

## Prerequisites

Before running the project, make sure you have the following:

- **Python 3.x**: This project is built with Python 3.x.
- **Libraries**:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `sklearn`
  - `keras`
  - `yfinance`

You can install the required libraries using:

```bash
pip install -r requirements.txt
```

## Files

1. **stock_prediction_lstm.py**: The main Python script containing the LSTM model implementation and stock price prediction.
2. **requirements.txt**: The list of required libraries for the project.

## Installation

1. Clone this repository to your local machine:

    ```bash
    git https://github.com/21A91A6128/Stock-Price-Forecasting-with-LSTM.git
    cd Stock-Price-Forecasting-with-LSTM
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

### 1. Download Stock Data

The code downloads historical stock data for **Apple Inc. (AAPL)** from Yahoo Finance. You can change the stock ticker symbol by modifying the script if you wish to predict for other companies.

### 2. Preprocessing Data

- The closing prices of the stock are filtered and scaled to a range between 0 and 1 using the **MinMaxScaler**.
  
- 80% of the data is used for training, while 20% is used for testing.

### 3. LSTM Model

- An LSTM model is defined using the **Keras** library to predict the stock price. The model consists of two LSTM layers followed by dense layers.

- The model is trained using the scaled data for one epoch with a batch size of 1.

### 4. Making Predictions

After training, the model is used to predict the stock prices for the test data. The predicted values are inversely scaled to retrieve the original stock price.

### 5. Visualization

The code plots the **training**, **validation**, and **predicted** stock prices using **Matplotlib**.

### 6. Real-Time Prediction

After training the model, it predicts the stock price for the next day based on the last 60 days of data. This is done by extracting the last 60 closing prices, scaling them, and feeding them into the model.

## Results

The model outputs a **Root Mean Squared Error (RMSE)** value that represents the model's performance on the test data. A lower RMSE indicates better accuracy.

---
