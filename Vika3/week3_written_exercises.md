### Week 3 - Strategy Development & Evaluation

# Part A: Strategy Summary

This week, I implemented a rule-based trading strategy on Tesla (TSLA) using engineered featured derived from daily closing prices.

The primary strategy was based on:

- A simple moving average crossover (20-day > 50-day).
- Momentum check using 1-day and 5-day returns.
- Volatility confirmation via 20-day rolling standard deviation.
- Price action relative to trend: Price/SMA ratio and SMA difference.

The final signal was generated only when:

- SMA_20 > SMA_50 (bullish crossover),
- Return_1 > 0,
- Return_5 > 0,
- Price_SMA_ratio > 1,
- SMA_diff > 0,
- Volatility_20 below a moderate threshold (0.03).

This reduced noise and targeted periods of confirmed trend and stable volatility.


# Part B: Features Used

Feature Purpose

- SMA_20 & SMA_50 Trend detection & Crossover confirmation
- Simple/Log Returns	Daily price movement measurement
- Return_1 & Return_5	Short-term momentum check
- Volatility_20	Measures risk; filters out unstable periods
- SMA_diff	Confirms upward trend strength
- Price_SMA_ratio	Confirms price > trend average


# Part C: Evaluation Metrics

Performance Summary:

Number of Trades: 52
Winning Trades: 9
Losing Trades: 0
Win Rate: 17.31%
Sharpe Ratio: 4.64
Max Gain: 19.29%
Max Loss: 0.00%
Average Return/Trade: 0.87%

The strategy avoids large drawdowns, indicating the strict conditions minimize downside risk. However, the low win rate suggests the rules might be too restrictive.

# Part D: Interpretation

While the strategy has strong risk-adjusted returns (high Sharpe), the number of winning trades is low, and many opportunities might be missed due to tight filters. This trade-off between precision and recall is common in rule-based models.

The high max gain and zero loss are promising, but I would like to test relaxing some thresholds or exploring probabilistic models (e.g., logistic regression) in the next weeks to see if it can generalize better.


# Part E: Improvements


For future work i would like to:

- Test different thresholds or add parameter optimization.
- Compare against a baseline like SMA crossover alone.
- Include additional data like volume SMA or RSI.