📈 Inflation-Forecasting-Suite
A research-grade quantitative framework for forecasting 10-Year Breakeven Inflation using univariate statistical models (ARIMA), multivariate exogenous models (ARIMAX), and Deep Learning (LSTM with MC-Dropout).

🚀 Project Overview
This project implements a side-by-side comparison of traditional econometrics vs. modern neural networks to predict market-based inflation expectations. It is designed to meet the standards of sell-side Global Markets research, prioritizing statistical significance and uncertainty quantification over simple error metrics.

🛠 Key Features
Live Data Integration: Seamlessly switches between a calibrated Synthetic DGP and live financial data via the FRED API (T10YIE, CPI) and Yahoo Finance (GLD, USO, DXY, ^TNX).
Multi-Model Architecture:
ARIMA/ARIMAX: Benchmarked using automated order selection (pmdarima) and walk-forward validation.
LSTM with MC-Dropout: A deep learning approach that provides predictive distributions and 95% confidence intervals, rather than just point estimates.
Naive Random Walk: Every model is rigorously tested against a 'No-Change' benchmark to calculate Theil’s U Statistic.
Institutional-Grade Metrics: Uses the Diebold-Mariano Test to determine if model improvements are statistically significant or merely noise.
Trading Signal Backtest: Includes a momentum-based strategy simulation to evaluate the economic value of forecasts.
🧪 Methodology
Stationarity: Automated ADF testing and first-differencing.
Walk-Forward Validation: Expanding training windows to prevent look-ahead bias.
Bayesian Approximation: Using Monte Carlo Dropout during inference to quantify model uncertainty.
Directional Accuracy: Evaluation of 'Hit-Rates' for market-timing applications.
📊 Quick Start
To run with live data:

Add your FRED_API_KEY to your environment or Colab Secrets.
Install dependencies: pip install pmdarima yfinance pandas_datareader.
Execute the notebook to generate a 30-day forward-looking inflation forecast.
