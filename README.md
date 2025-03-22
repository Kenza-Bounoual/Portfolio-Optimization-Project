# Portfolio Optimization Project with Python

## What This Project Does

This project takes stock data from Yahoo Finance, analyzes it, and then uses different methods to optimize the portfolio. We’ll calculate key metrics like returns, risk, and how stocks correlate with each other. Ultimately, we’ll create efficient portfolios using **PyPortfolioOpt** and visualize the results with tools like **Plotly**, **Seaborn**, and **Matplotlib**.

### Here's what the project covers:

- **Stock Data Download**: We pull stock data using Yahoo Finance's API (`yfinance`).

- **Portfolio Returns**: We calculate daily returns based on the adjusted closing prices, and then calculate cumulative returns to see how our portfolio performs over time.

- **Correlation Matrix**: We generate a normalized correlation matrix to understand how the stocks are related to each other in terms of returns.

- **Portfolio Optimization**: We use a few different methods to optimize the portfolio:
  - **Expected Returns**: We estimate the future returns for each stock .
  - **Covariance Matrix**: We calculate the covariance matrix .
  - **Efficient Frontier**: This is a fancy way of showing the trade-off between risk and return. We use **PyPortfolioOpt** to compute the efficient frontier.
  - **Minimum Volatility Portfolio**: This portfolio aims to have the least risk (volatility).
  - **Maximum Sharpe Ratio Portfolio**: This portfolio maximizes the Sharpe Ratio, meaning it offers the best return for a given level of risk.

## The Optimization Methods:

### 1. **Mean-Variance Optimization**
The goal of **Mean-Variance Optimization** is simple: minimize the risk (variance) while maximizing the return. This method relies on two key elements:
- **Expected Returns**.
- **Covariance Matrix**: This shows how the returns of the stocks move in relation to one another.

Then, we use the `min_volatility()` method in **PyPortfolioOpt’s EfficientFrontier** class to find the portfolio that minimizes risk for a set of expected returns.

### 2. **Sharpe Ratio Maximization**
The **Sharpe Ratio** is a measure that tells us how much return we’re getting for each unit of risk. The higher the Sharpe ratio, the better the risk-adjusted return. Here, we maximize the Sharpe ratio using the `max_sharpe()` method in **PyPortfolioOpt**, with a risk-free rate of 0.9% (a commonly used benchmark for the risk-free rate).

### 3. **Efficient Frontier**
The **Efficient Frontier** is a plot that shows the best possible portfolios for each level of risk. It helps investors understand the trade-off between risk and return. Using **PyPortfolioOpt**, we calculate the efficient frontier and plot it. The plot will show:
- **Minimum Volatility Portfolio** (the portfolio with the lowest risk)
- **Maximum Sharpe Portfolio** (the portfolio with the highest Sharpe ratio)
