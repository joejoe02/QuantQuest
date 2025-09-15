# Week 4 – Regression-Based Modeling for Stock Prediction

## 📘 Learning Objectives

- Understand how linear regression can be applied to predict financial time series.
- Learn how to construct input features from time series data (e.g., lagged returns, moving averages).
- Implement and evaluate a simple linear regression model on stock return data.
- Interpret coefficients, performance metrics, and residuals.
- Learn to split time series data for training and testing (avoiding lookahead bias).
- Compare predictions to actual market behavior and assess predictability.

## 🛠️ Technical Skills

- Feature engineering from stock data
- Linear regression with `scikit-learn`
- Time series train/test splitting
- Regression metrics: MSE, RMSE, R²
- Visualizing predictions vs actual returns

## 📊 Dataset

Continue using your existing Tesla (`TSLA`) dataset from Week 3 (daily adjusted close prices 2022–2024).

## ✏️ Assignment Tasks

1. **Feature Engineering:**
   - Lagged returns (1, 2, 3 days)
   - Moving averages (5-day, 10-day)
   - Volatility (rolling std of returns)
   - SMA Crossover signal (binary)

2. **Model Training:**
   - Predict 1-day future returns or direction (`Return_1`)
   - Use `LinearRegression()` from `sklearn`
   - Train on 80% of the data, test on last 20%

3. **Evaluation:**
   - Plot predicted vs actual returns
   - Compute MSE, RMSE, R²
   - Discuss overfitting/underfitting and model assumptions

4. **Documentation:**
   - Update `week4_learning.md` summarizing concepts and findings
   - Commit updated code and documentation to your GitHub repo

## 🧠 Written Exercise

- Reflect on the assumptions of linear regression in a financial context.
- Analyze when it is appropriate and what risks it carries.
- Include in `week4_written_exercise.md`.

## 🎥 Video Resources

- [Linear Regression for Stock Returns (Ken Jee)](https://www.youtube.com/watch?v=9D1x7-2FmTA)
- [Finance-focused ML & Regression Crash Course](https://www.youtube.com/watch?v=xdz_9eC3WBA)

## Optional Extension

- Try Ridge or Lasso regression for regularization.
- Evaluate how regularization affects predictions and weights.
