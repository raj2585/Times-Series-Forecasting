# Electricity Consumption Forecasting — ARIMA vs LSTM

Time series forecasting on 397 months of US electricity consumption data (1985–2017).
Compares a classical statistical model (ARIMA) against a deep learning approach (LSTM)
to evaluate effectiveness on seasonal, non-linear consumption patterns.

## Results

| Model | Best Parameters | Metric |
|-------|----------------|--------|
| ARIMA | (2, 1, 2) | AIC = -1499.61 |
| LSTM | 75 units, seq_len=12, epochs=50 | MSE = 9.69 |

LSTM outperformed ARIMA on non-linear seasonal patterns. ARIMA remained competitive
for stable trend segments. A hybrid approach is identified as future scope.

## Methods

- Stationarity testing via Augmented Dickey-Fuller (ADF) test
- ACF/PACF plots for ARIMA parameter selection (p, q)
- Grid search over ARIMA (p, d, q) configurations, selected by AIC
- MinMaxScaler normalization for LSTM input
- Sliding window sequences (length = 12 months) for LSTM training
- Early stopping to prevent overfitting
- Evaluation metrics: MSE, AIC

## Dataset

[Electric Production dataset](https://www.kaggle.com/datasets/kandij/electric-production) — Kaggle  
Monthly electricity consumption (kWh), January 1985 to January 2017.

## Setup

```bash
git clone https://github.com/raj2585/Times-Series-Forecasting
cd Times-Series-Forecasting
pip install -r requirements.txt
```

**Requirements:** Python 3.8+, numpy, pandas, matplotlib, tensorflow, statsmodels

## Usage

Run notebooks in order:
1. `data_preprocessing.ipynb` — EDA and preprocessing
2. `arima_training.ipynb` — ARIMA model training and forecasting
3. `lstm_training.ipynb` — LSTM model training and forecasting
