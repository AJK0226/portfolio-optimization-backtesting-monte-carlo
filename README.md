# Portfolio Optimization with Backtesting, Monte Carlo, and Rolling Optimization

This project implements portfolio optimization using historical stock market data based on Modern Portfolio Theory (MPT).  
The objective is to identify optimal asset allocations that balance risk and return, and to evaluate their performance using:

- Out-of-sample backtesting
- Monte Carlo simulation
- Rolling (walk-forward) optimization
- Benchmark comparison
- Factor model analysis

This project is intended for learning and demonstration purposes in Data Science and Quantitative Finance.

---

## 📌 Project Overview

The project focuses on:

- Constructing optimal portfolios using historical price data
- Visualizing the Efficient Frontier
- Identifying:
  - Minimum Variance Portfolio
  - Maximum Sharpe Ratio Portfolio
- Evaluating portfolio performance on unseen data (backtesting)
- Simulating future portfolio performance using Monte Carlo methods
- Performing rolling (walk-forward) portfolio optimization
- Comparing performance with benchmark index (S&P 500)
- Analyzing asset returns using factor models

---

## 🧠 Methodology

### 1. Data Collection
- Stock price data downloaded from Yahoo Finance
- Assets used:
  - AAPL
  - MSFT
  - GOOGL
  - AMZN
  - META
- Benchmark:
  - S&P 500 (^GSPC)

### 2. Data Preprocessing
- Daily closing prices converted to daily returns
- Missing values removed
- Covariance matrix computed for risk estimation

### 3. Portfolio Optimization
- Random portfolios generated
- Portfolio metrics computed:
  - Expected return
  - Volatility
  - Sharpe ratio
- Optimization performed using SciPy (SLSQP) with constraints:
  - Weights sum to 1
  - No short selling (weights between 0 and 1)

### 4. Efficient Frontier Visualization
- Risk vs return of random portfolios plotted
- Key portfolios highlighted:
  - Minimum Variance Portfolio
  - Maximum Sharpe Ratio Portfolio

### 5. Backtesting (Out-of-Sample Evaluation)
- Historical data split into training and testing periods
- Optimized portfolio weights applied to unseen future data
- Portfolio performance evaluated over time
- Look-ahead bias avoided

### 6. Monte Carlo Simulation
- Future portfolio returns simulated using random sampling
- Thousands of possible price paths generated
- Estimates distribution of future portfolio values
- Used to analyze potential risk and return scenarios

### 7. Rolling Optimization (Walk-Forward Strategy)
- Portfolio is re-optimized periodically using rolling historical windows
- Weights updated dynamically based on recent data
- More realistic simulation of real-world portfolio management
- Avoids static weight assumptions

### 8. Benchmark Comparison
- Portfolio performance compared against S&P 500 index
- Metrics compared:
  - Total return
  - Annualized return
  - Volatility
  - Sharpe ratio

### 9. Factor Model Analysis
- Asset returns analyzed using factor-based regression
- Measures sensitivity of assets to common market risk factors
- Helps understand drivers of portfolio performance

---

## 📊 Output

- Efficient Frontier plot showing risk–return trade-off
- Portfolio equity curve from backtesting
- Monte Carlo simulation plot showing future portfolio paths
- Rolling optimization performance curve
- Benchmark comparison plot vs S&P 500
- Factor exposure visualizations

---

## 🛠 Tools and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- SciPy
- yFinance

All dependencies are listed in `requirements.txt`.

---

## 📁 Project Structure


```

portfolio-optimization/
├── optimization.py
├── backtesting.py
├── monte_carlo.py
├── rolling_optimization.py
├── factor_models.py
├── requirements.txt
├── README.md
├── plots/
│   ├── efficient_frontier.png
│   ├── backtesting_equity_curve.png
│   ├── monte_carlo_simulation.png
│   ├── rolling_optimization.png
│   ├── benchmark_comparison.png
│   └── factor_model_exposure.png


```

---

## 🚀 Future Enhancements

- Transaction cost modeling
- Portfolio turnover analysis
- Regime detection
- Forecast-assisted allocation
- Value at Risk (VaR) and Conditional VaR (CVaR)
- Dashboard for interactive visualization
- Paper trading integration

---

## ⚠ Disclaimer

This project is for educational purposes only and does not constitute financial or investment advice.

