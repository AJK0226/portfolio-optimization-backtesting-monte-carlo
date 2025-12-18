# Portfolio Optimization using Modern Portfolio Theory

This project implements portfolio optimization using historical stock market data based on Modern Portfolio Theory (MPT).  
The objective is to identify optimal asset allocations that balance risk and return, and to evaluate their performance using out-of-sample backtesting.

---

## Project Overview

The project focuses on:
- Constructing optimal portfolios using historical price data
- Visualizing the Efficient Frontier
- Identifying:
  - Minimum Variance Portfolio
  - Maximum Sharpe Ratio Portfolio
- Evaluating portfolio performance on unseen data (backtesting)

This project is intended for learning and demonstration purposes in Data Science and Quantitative Finance.

---

## Methodology

### 1. Data Collection
- Stock price data is downloaded from Yahoo Finance
- Assets used:
  - AAPL
  - MSFT
  - GOOGL
  - AMZN
  - META

### 2. Data Preprocessing
- Daily closing prices are converted to daily returns
- Missing values are removed
- Covariance matrix is computed for risk estimation

### 3. Portfolio Optimization
- Random portfolios are generated
- Portfolio metrics computed:
  - Expected return
  - Volatility
  - Sharpe ratio
- Optimization performed using SciPy (SLSQP) with constraints:
  - Weights sum to 1
  - No short selling (weights between 0 and 1)

### 4. Efficient Frontier Visualization
- Risk vs return of random portfolios is plotted
- Key portfolios highlighted:
  - Minimum Variance Portfolio
  - Maximum Sharpe Ratio Portfolio

### 5. Backtesting (Out-of-Sample Evaluation)
- Historical data is split into training and testing periods
- Optimized portfolio weights are applied to unseen future data
- Portfolio performance is evaluated over time
- Look-ahead bias is avoided

---

## Output

- Efficient Frontier plot showing risk–return trade-off
- Optimal portfolio weights for minimum variance and maximum Sharpe ratio portfolios
- Portfolio performance during backtesting

---

## Tools and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- SciPy
- yFinance

All dependencies are listed in `requirements.txt`.

---

## Project Structure

---

## Team Members

- Hemanthkumar BM
- Aditya JK

---

## Future Enhancements

- Monte Carlo simulation
- Rolling (walk-forward) portfolio optimization
- Benchmark comparison
- Risk metrics such as VaR and CVaR

---

## Disclaimer

This project is for educational purposes only and does not constitute financial or investment advice.