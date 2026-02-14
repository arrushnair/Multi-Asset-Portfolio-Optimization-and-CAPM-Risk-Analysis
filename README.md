# Project Overview

This project conducts a detailed quantitative analysis of high-growth technology equities including Apple, Meta, Amazon, and Nvidia, alongside the S&P 500 (SPY) as a market benchmark. Utilizing Python and libraries such as pandas and yfinance, the analysis calculates critical financial metrics including log returns, beta coefficients, and Jensen's Alpha. The project culminates in a sophisticated portfolio optimization using Monte Carlo simulations to determine the Efficient Frontier and identify optimal asset allocations based on risk-adjusted returns and volatility.

# Objectives

* **Price and Return Analysis:** Fetch and normalize historical stock data to analyze price trends and log-return distributions.
* **Risk Metric Calculation:** Determine the Beta coefficient for each stock to measure systemic risk relative to the S&P 500.
* **Performance Evaluation:** Calculate Jensen's Alpha to identify stocks generating significant excess returns above the Capital Asset Pricing Model (CAPM) prediction.
* **Portfolio Optimization:** Map the Efficient Frontier to identify the Maximum Sharpe Ratio and Minimum Volatility portfolios.
* **Risk Modeling:** Estimate and minimize the Value at Risk (VaR) at a 95% confidence level for a diversified portfolio.

# Methodology

* **Data Collection:** Utilized the yfinance API to programmatically extract historical Adjusted Close and Volume data for a 1.5-year period.
* **Quantitative Analysis:** Employed pandas and NumPy to perform statistical profiling, including the generation of a covariance matrix and annualized volatility metrics.
* **CAPM Framework:** Applied the Capital Asset Pricing Model to derive expected returns based on a 1.38% risk-free rate and systemic risk (Beta).
* **Monte Carlo Simulation:** Simulated 10,000+ random portfolio weight distributions to analyze the trade-offs between risk and return.
* **Visualization:** Used matplotlib and seaborn to create box plots, correlation heatmaps, and scatter plots of simulated portfolio outcomes.

# Key Findings

* **Alpha Generation:** Nvidia (NVDA) and Meta (META) demonstrated high Jensen's Alpha values (0.99 and 0.51 respectively), indicating substantial outperformance relative to their market-implied risk.
* **Risk Sensitivity:** Beta analysis revealed that NVDA (2.15) and META (1.80) are significantly more volatile than the broader market, while Apple (AAPL) remained closer to market parity (1.09).
* **Optimization Results:** The Maximum Sharpe Ratio portfolio achieved an annualized return of 117% with a Sharpe Ratio of 3.42, heavily weighting NVDA and META.
* **Conservative Allocation:** The Minimum Volatility portfolio significantly prioritized AAPL (76%), reducing annualized volatility to 20%.

# How to Run

Ensure Python 3.x is installed along with the required libraries. Clone the repository and execute the provided Python script or Jupyter Notebook. The script will automatically fetch the latest market data, perform the mathematical modeling, and display the visualization plots.

# Requirements

* Python 3.x
* pandas
* NumPy
* yfinance
* matplotlib
* SciPy (scipy.stats)
