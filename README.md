# StockPredictor_DeepLearning

This repository contains two Jupyter notebooks (.ipynb) for stock price prediction using deep learning techniques. The models are trained on NVIDIA (NVDA) stock data from Yahoo Finance and incorporate technical indicators such as SMA, EMA, and ATR.

## Models Implemented

1. LSTM (Long Short-Term Memory)
 - Captures short-term dependencies in stock price movement.
 - Performs well for immediate forecasting.
 - Code: [LSTM.ipynb](StockPredictor_DeepLearning/LSTM.ipynb)

2. Transformer + LSTM (Hybrid Model)
 - Uses a Transformer Encoder to capture long-term dependencies.
 - Passes extracted features through an LSTM for final prediction.
 - Provides better long-term trend forecasting.
 - Code: [Transformer_LSTM.ipynb](StockPredictor_DeepLearning/Transformer_LSTM.ipynb)

## Dataset
 - Stock: NVIDIA (NVDA)
 - Source: Yahoo Finance API
 - Timeframe: Last 2 years of daily stock prices
 - Features Used:
 - Stock Prices: Open, High, Low, Close
 - Technical Indicators:
 - Simple Moving Average (SMA, 10-day)
 - Exponential Moving Average (EMA, 10-day)
 - Average True Range (ATR, 10-day)

## Installation

```
Clone the repository and install dependencies:

git clone https://github.com/YOUR_USERNAME/StockPredictor_DeepLearning.git
cd StockPredictor_DeepLearning
pip install -r requirements.txt
```

## Model Training & Evaluation

Run the models in Jupyter Notebook:

Running LSTM Model

jupyter notebook LSTM.ipynb

 - RMSE: 25.19
 - MAE: 22.88
 - 5-day Predictions: [107.24, 105.99, 104.59, 102.97, 101.33]

Running Transformer + LSTM Model

jupyter notebook Transformer_LSTM.ipynb

 - RMSE: 8.71
 - MAE: 6.94
 - 5-day Predictions: [129.47, 122.77, 120.90, 119.04, 118.45]

## Observations & Discussion
 - LSTM predictions were closer to the current stock price (106.98 on 2025/03/11), making it more suitable for short-term forecasting.
 - Transformer + LSTM had better RMSE & MAE, making it more effective for long-term trends.
 - Future improvements may include:
 - Hyperparameter tuning
 - Ensemble models (combining multiple architectures)
 - Additional financial indicators

## Output

After running the models, the predicted stock prices for the next 5 days are saved in:

-> 41147011S.txt

## Future Work
 - Optimize hyperparameters using Bayesian Optimization.
 - Experiment with CNN-LSTM for improved feature extraction.
 - Implement attention mechanisms for dynamic feature weighting.

## License

This project is open-source under the MIT License.

## Author
  #### u-chow
  #### Institution: National Taiwan Normal University
  #### Contact: richard930326@gmail.com
