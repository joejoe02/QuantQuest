# 📅 Week 2: Time Series Fundamentals & Stationarity (August 5 – August 11, 2025)

## 🎯 Objectives
- Understand the concept of **stationarity** in time series data.
- Learn and visualize **autocorrelation (ACF)** and **partial autocorrelation (PACF)**.
- Compute **rolling mean** and **rolling volatility** of log returns.
- Perform the **Augmented Dickey-Fuller (ADF)** test to statistically test for stationarity.
- Understand how stationarity impacts forecasting and model design.

---

## 📚 Reading & Theory

### 📖 Book Reference: *Statistics and Data Analysis for Financial Engineering* by David Ruppert

- **Chapter 12 – Time Series Models: Basics**
  - **12.1** Introduction to Time Series
  - **12.2** Mean, Autocovariance, and Autocorrelation
  - **12.3** Stationarity
  - **12.4** Sample Autocorrelation Function and Lag Plots

### 🔍 Key Concepts:
- Stationarity (weak and strong)
- Autocovariance and autocorrelation functions
- ACF vs PACF interpretation
- Random walks and unit roots
- Augmented Dickey-Fuller test

---

## 🛠️ Coding Assignment

Notebook: `week2_time_series.ipynb`

1. Load your AAPL or MSFT daily price data.
2. Plot:
   - Closing price
   - Daily log returns
   - 20-day rolling mean & std of log returns
3. Plot ACF and PACF of log returns.
4. Perform the ADF test and interpret the result.
5. Write markdown explaining whether your data is stationary and why that matters.

---

## 📺 Video Lectures

- [Stationarity in Time Series Analysis (Python Tutorial)](https://www.youtube.com/watch?v=ZLvLf9aCSr8)
- [ACF vs PACF Explained Simply](https://www.youtube.com/watch?v=BNA4BDQvhq0)

Take notes in: `notes/week2_video_notes.md`

---

## 📄 Deliverables (Due by Sunday, August 11)
- `week2_time_series.ipynb` with markdown explanations
- Updated `README.md` with Week 2 summary, key formulas, and interpretations
- `notes/week2_reading.md` (optional): highlights from Chapter 12

---

Let me know when you'd like to review your notebook or need help! 🔍📈
