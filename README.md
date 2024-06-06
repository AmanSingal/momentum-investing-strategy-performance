# Momentum Investing Strategy Backtest

This repository contains a Python script to backtest a simple momentum investing strategy and evaluate its performance over a 4-year period.

## Data

The dataset obtained(from NSE website) includes historical daily closing stock prices for the past 5 years.

## Task Overview

### 1. Data Cleaning

### 2. Return Calculation
- Calculate the 3-month, 6-month, and 12-month percentage returns (if data allows) for each stock at the end of every week.

### 3. Weighted Average Return
- Assign weights of 1:2:3 to the 3-month, 6-month, and 12-month percentage returns, respectively.  
- Calculate the weighted average return for each stock at the end of every week. Ignore stocks that do not have a 12-month return history.

### 4. Stock Ranking & Portfolio Construction
- Rank all stocks in descending order based on their weighted average return at the end of each week.  
- Simulate a portfolio that buys the top 30 stocks at the end of each week and sells any holdings that fall outside the top 30. Trades occur only at the end of each week.  
- Assume equal weight allocation to each stock within the portfolio (1/30th of the total portfolio size).  
- Ignore transaction costs. The starting value of the portfolio is INR 1,00,00,000.

### 5. Performance Evaluation
- Calculate the following metrics for the entire 4-year holding period (excluding the first year, as there is no return history):  
  - Compound Annual Growth Rate (CAGR) of the portfolio.  
  - Maximum drawdown experienced by the portfolio during the holding period.  
  - Win/Loss ratio of all trades executed within the portfolio.  
  - Sharpe Ratio, a risk-adjusted performance measure.  
  - Average gain/loss per trade.  
