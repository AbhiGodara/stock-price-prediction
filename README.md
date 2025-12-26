# 📈 Advanced Stock Price Prediction using Attention-based LSTM

This project implements an **advanced deep learning pipeline for stock price forecasting** using historical market data. It combines **extensive feature engineering, exploratory data analysis (EDA), and an attention-enhanced LSTM architecture** to accurately predict future stock prices and trends.

The model is trained and evaluated on **Apple Inc. (AAPL)** historical stock data sourced from Yahoo Finance and demonstrates strong predictive performance with low error metrics.

---

## 📌 Table of Contents

- Project Overview
- Dataset
- Feature Engineering
- Exploratory Data Analysis
- Model Architecture
- Training & Evaluation
- Results
- Future Price Forecasting
- Visualizations
- Installation
- Usage
- Results Summary
- Future Work
- License

---

## 📖 Project Overview

Financial time-series forecasting is a challenging problem due to market volatility and non-linearity.  
This project addresses the problem using an **Advanced Bidirectional LSTM with Attention Mechanism**, enabling the model to focus on the most relevant time steps while making predictions.

The pipeline covers:
- Data acquisition
- Feature engineering
- Deep learning model design
- Training & evaluation
- Future price forecasting
- Comprehensive visualization

---

## 📊 Dataset

- **Source:** Yahoo Finance (via `yfinance`)
- **Stock:** Apple Inc. (AAPL)
- **Time Range:** 2010-01-01 to 2023-12-31
- **Records:** ~3,500 daily observations

---

## 🛠️ Feature Engineering

The following technical indicators and features are used:

- Close Price
- Trading Volume
- Daily Returns
- High-Low Percentage (HL %)
- Open-Close Percentage (OC %)
- Moving Averages (MA5, MA20, MA50)
- 20-Day Rolling Volatility

Missing values are handled appropriately after rolling computations.

---

## 📊 Exploratory Data Analysis (EDA)

EDA includes:
- Stock price trends with moving averages
- Distribution of daily returns
- Volatility analysis
- Trading volume (log-scale)
- Feature correlation heatmap
- Relationship analysis between price-based indicators

Both **static Matplotlib** and **statistical visualizations** are used for deep market insight.

---

## 🧠 Model Architecture

### 🔹 Advanced LSTM with Attention
- Bidirectional LSTM (3 layers)
- Attention mechanism to weigh important time steps
- Fully connected layers with dropout for regularization
- RobustScaler for feature normalization
- Gradient clipping for training stability

**Total Parameters:** ~960K

---

## 🧪 Training & Evaluation

- **Sequence Length:** 60 days
- **Train/Test Split:** 80% / 20%
- **Optimizer:** Adam
- **Loss Function:** Mean Squared Error (MSE)
- **Scheduler:** ReduceLROnPlateau
- **Epochs:** 100
- **Batch Size:** 32

---

## 📈 Model Performance

| Metric | Value |
|------|------|
| MSE | 51.21 |
| MAE | 3.89 |
| RMSE | 7.15 |
| R² Score | 0.982 |
| MAPE | 5.14% |

The model demonstrates **high explanatory power** and **low prediction error**, making it suitable for real-world forecasting scenarios.

---

## 🔮 Future Price Forecasting

- Predicts **next 30 trading days**
- Uses recursive forecasting with the last observed sequence
- Produces smooth and realistic price trajectories
- Includes:
  - Future price plot
  - Daily change analysis
  - Tabular forecast with percentage changes

---

## 📊 Visualizations

- Actual vs Predicted Prices
- Error Distribution
- Zoomed Prediction View
- Future Forecast Plot
- Daily Price Change (absolute & percentage)
- Forecast Summary Table

---

## ⚙️ Installation

```bash
git clone https://github.com/your-username/stock-price-prediction-lstm.git
cd stock-price-prediction-lstm
pip install -r requirements.txt
