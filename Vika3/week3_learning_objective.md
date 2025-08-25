
# Week 3 – Strategy Backtesting & Moving Averages

## Learning Objectives

By the end of this week, I will:

- Understand how basic stock trading strategies are structured
- Code and backtest a **Simple Moving Average (SMA)** crossover strategy
- Learn how to measure strategy performance (returns, Sharpe Ratio, drawdowns)
- Analyze in-sample vs out-of-sample performance

## Key Concepts

### SMA Crossover Strategy
- Buy when short SMA crosses above long SMA (bullish signal)
- Sell when short SMA crosses below long SMA (bearish signal)

### Backtesting
- Simulate a strategy over historical data
- Record performance metrics like:
  - Total return
  - Daily return
  - Volatility
  - Max drawdown
  - Sharpe Ratio

### Performance Evaluation
- Compare with buy-and-hold benchmark
- Analyze signal delays, whipsaws, and market trends

## Reading Assignment

### Book:
- Chapter 13 (Trading Strategies): Sections 13.1–13.3

### Optional:
- Chapter 14 (Performance Evaluation): Section 14.1

## Video Lectures

1. [Backtesting Strategies in Python – SMA Example (freeCodeCamp)](https://www.youtube.com/watch?v=xfzGZB4HhEE)
2. [Measuring Risk & Sharpe Ratio](https://www.youtube.com/watch?v=KTYcFn0hvuc)

## Deliverables

- `week3_backtest_sma.ipynb`
- `notes/week3_written_exercise.md`
- Update `README.md` with summary and performance results
