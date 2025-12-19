# Portfolio Optimization using Modern Portfolio Theory

This project implements portfolio optimization using historical stock market data based on Modern Portfolio Theory (MPT).  
The objective is to identify optimal asset allocations that balance risk and return, and to evaluate their performance using out-of-sample backtesting and Monte Carlo simulation.

---

## Project Overview

The project focuses on:
- Constructing optimal portfolios using historical price data
- Visualizing the Efficient Frontier
- Identifying:
  - Minimum Variance Portfolio  
  - Maximum Sharpe Ratio Portfolio
- Evaluating portfolio performance on unseen data (backtesting)
- Simulating future portfolio performance using Monte Carlo methods

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

### 6. Monte Carlo Simulation
- Future portfolio returns are simulated using random sampling
- Thousands of possible price paths are generated
- Helps estimate the distribution of future portfolio values
- Used to analyze potential risk and return scenarios

---

## Output

- Efficient Frontier plot showing risk–return trade-off
- Optimal portfolio weights for minimum variance and maximum Sharpe ratio portfolios
- Portfolio equity curve from backtesting
- Monte Carlo simulation plot showing multiple future portfolio paths

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

## Future Enhancements

- Rolling (walk-forward) portfolio optimization
- Benchmark comparison (e.g., S&P 500)
- Risk metrics such as VaR and CVaR
- Transaction cost modeling

---

## Disclaimer

This project is for educational purposes only and does not constitute financial or investment advice.
