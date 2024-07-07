# Deep Reinforcement Learning for Stock Trading

## Introduction
This project applies Deep Reinforcement Learning (DRL) for trading multiple stocks. The strategy uses DRL to analyze and make trading decisions across a selected portfolio of stocks, aiming to maximize portfolio value over time.

## Project Structure

### Data Preprocessing
- Import necessary libraries.
- Download historical stock data from Yahoo Finance for 8 stocks (AAPL, KO, MSFT, F, PEP, TSLA, JNJ, PFE) from 2010-2023.
- Calculate technical indicators (RSI, MACD, ATR) using the `stockstats` library.
- Calculate the turbulence index to measure major market events.

### Feature Engineering
- Process the data and perform feature engineering to prepare it for input into the deep learning model.

### DRL Environment
- Create a custom environment using `gym` to simulate stock trading.
- Implement the `StockTrain` and `StockTrade` classes for training and trading environments, respectively.

### DRL Model
- Use the Deep Deterministic Policy Gradient (DDPG) algorithm from `stable_baselines3`.
- Train the DDPG model on the training data.
- Test the trained model on unseen data.

### Performance Evaluation
- Plot the profit/loss graph of the DRL strategy against a simple buy-and-hold strategy.
- Calculate and compare the Sharpe ratios of the DRL strategy and the buy-and-hold strategy.

## Conclusion
The DRL algorithm demonstrated a return of $12,264 over the course of Jan 2022-Dec 2023, with a Sharpe Ratio of 0.205, indicating its profitability despite some volatility. In comparison, the buy-and-hold strategy had a loss of about 12%, with a Sharpe ratio of -0.463. The DRL algorithm shows promise and opportunities for further optimization.
