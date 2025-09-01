# Stock Return Prediction with Machine Learning

This project applies **machine learning models** to predict stock price returns and evaluates **trading strategies** through backtesting.


## Overview

* **Models**: Logistic Regression (baseline) & Random Forest (non-linear)
* **Framework**: [BackTrader](https://www.backtrader.com/) for backtesting, results analyzed with PyFolio & QuantStats
* **Data**: Yahoo Finance (2000-01-01 to 2021-11-12, 10 tickers)


## Features

* Data pipeline: missing value handling, outlier removal, normalization
* Feature engineering: MA, EMA, Volatility, ATR, RSI, Momentum
* Model training & evaluation: Accuracy, Precision, F1, ROC AUC
* Trading strategies: SMA/EMA trend filters, ATR-based stop-loss & take-profit, dynamic position sizing


## Results

* Logistic Regression: stable \~65% accuracy, strong baseline
* Random Forest: \~63% accuracy, better on some tickers
* Backtests:

  * WMS achieved Sharpe ≈ 0.08, Max Drawdown ≈ -22%
  * DWDP & PGR ranked top in 10-stock universe with low drawdowns


## Setup

**Python 3.7.x**

Install dependencies:

```bash
pip install numpy pandas scikit-learn backtrader quantstats==0.0.62 pyfolio yfinance
```

Run in **Google Colab** for full trading reports
