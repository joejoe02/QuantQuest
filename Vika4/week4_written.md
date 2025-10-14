Week 4 – Written Exercise: Regression-Based Modeling
### 1. What are the assumptions of linear regression? Which are violated in financial time series?

Linear regression relies on several core assumptions:

Linearity: The relationship between predictors and the target is linear.

Independence: Observations are independent of each other.

Homoscedasticity: Constant variance of errors across observations.

Normality of residuals: Errors follow a normal distribution.

No multicollinearity: Predictors are not too highly correlated.

Violations in financial data:

Linearity often does not hold due to complex market dynamics.

Independence is violated as financial data is sequential (autocorrelated).

Heteroscedasticity is common due to volatility clustering.

Residuals are often non-normal, especially during market shocks.

Multicollinearity may arise in feature sets like lagged returns and moving averages.

### 2. How did your model perform (metrics, visuals)?

I trained a logistic regression classifier to predict the next day’s return direction (up/down) based on engineered features from TSLA stock data.

Metrics:

Accuracy: ~46%

Precision: Varied between 43–47% per class

Recall: Slightly better on predicting "up" days

Confusion Matrix:

[[21 46]
 [28 41]]


This result shows marginal improvement over random guessing (50%) and demonstrates how hard financial prediction is. There may still be room for tuning and refining.

### 3. Which features seemed most useful?

Based on logistic regression weights and correlation analysis:

SMA_diff and Price/SMA_ratio helped capture trend strength.

Momentum_5 and Return_t-1 provided short-term movement information.

Volatility_20 helped reduce exposure to turbulent periods.

However, no single feature dominated, reaffirming the noisy nature of market data.

### 4. Would you trust this model for real-world decisions? Why or why not?

No. Despite its statistical significance and reasonable structure, the model:

Barely outperforms chance in prediction.

Doesn’t account for transaction costs, which could nullify all returns.

Is based on stationary historical features, which may shift in future markets.

Lacks risk-adjusted evaluation and doesn’t generalize well.

For real-world application, I would prefer probabilistic ensemble models, deeper validation, and more sophisticated features or external data (e.g. news sentiment, macro indicators).