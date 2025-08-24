# ✏️ Week 2 – Written Exercise: Stationarity & Time Series Analysis

## 🧠 Instructions:
Answer the following questions in your own words. You may refer to Chapter 12 of the textbook, your notebook, or external resources as needed. Submit this file with your answers added below each question.

---

## 📘 Section A: Concepts

### 1. What does it mean for a time series to be *stationary*? Why is stationarity important in time series modeling?

Stationary process is a type of stochastic process (random process) where the statistical properties, like the mean and variance do not change over time. Stationarity is a crucial concept in time series analysis because it simplifies modeling and forecasting. A stationary time series has statistical properties (mean, variance, autocovariance) that do not vary over time, making it easier to model patterns and predict future values. Non-stationary series, which exhibit trends or seasonality, can lead to inaccurate model results.

---

### 2. What is the difference between **autocovariance** and **autocorrelation**? Why is autocorrelation often preferred in practice?

Autocovariance and autocorrelation both analyze the relationship of a time series with a lagged version of itself, but they differ in how they measure this relationship. Autocovariance calculates the covariance between the time series and its lagged values, while autocorrelation standardizes the autocovariance by dividing it by the variance. Both are crucial metrics in financial time series econometrics.
Autocorrelation is more preferred in practice because it reveals patterns and dependencies within time series data, which is crucial for various applications like forecasting, model validation, and understanding data characteristics. By analysing how a variable correlates with its past values, autocorrelation helps identify trends, seasonality, and other structural aspects of the data. It provides a standardized measure of correlation, making it easier to interpret and compare across different time series or lags.
---

### 3. Explain the purpose of the **Autocorrelation Function (ACF)** and **Partial Autocorrelation Function (PACF)**. What does a slow decay in the ACF indicate?

The purpose of the autocorrelation function is to analyze the correlation between a time series and lagged versions of itself. It helps in understanding the dependency of data points on their past values, revealing patterns like trends and seasonality, crucial for time series analysis and forecasting, allowing analysts to identify patterns and build more accurate models.

PACF is a statistical tool used in time series analysis to identify the order of an autoregressive model. It measures the direct correlation between an observation and lagged versions of itself, after accounting for the effects of all intervening lags. It simply helps determine how much a value in a time series is directly related to its past values, without the influence of the values in between.

A slow decay in the ACF indicates that the series is non-stationary, in a stationary series there would be a fast pattern following similar mean values
---

### 4. What is the null hypothesis of the **Augmented Dickey-Fuller (ADF)** test? What does a p-value < 0.05 suggest about the time series?

The null hypothesis of the augmented dickey-fuller test is that the time series is non-stationary and contains a unit root. In other words, the test assumes the time series has a tendancy to wander randomly and is not reverting to a mean value.

If a P-value < 0.05 then we cannot reject the null hypothesis and that the time series is likely non-stationary

---

### 5. If you had a time series that was non-stationary, what steps could you take to make it stationary?

I would transform the non-stationary series to stationary by applying a couple of transformations to the variable, f.x. applying logs, differences.
When the series is non-stationary and it has a positive trend we need to retrain the series.
---

## 📊 Section B: Applied Interpretation

You generated the ACF, PACF, and performed the ADF test on your stock log returns. Based on your results:

### 6. What did your ACF and PACF plots show about autocorrelation in your return series?

My results look like white noise in the mean.
* ACF: Aside from lag 0, almost all spikes sit inside the 95% bands. Apple has a couple of small, borderline blips at short lags but nothing persistant
* PACF: Same story, no clear cuttoff or decay pattern; spikes hover around 0

---

### 7. What was the p-value of your ADF test? What was your conclusion — is your return series stationary?

* ADF P-values:
    - AAPL: p ≈ 7.64×10⁻¹⁵ (stat = −8.973 < −2.873)

    - MSFT: p ≈ 2.21×10⁻²⁹ (stat = −16.486 < −2.873)

Both strongly reject the unit-root null so the log returns are stationary (in mean)

### 8. What impact does your conclusion from Q7 have on your ability to use this series in future forecasting models?

My ADF tests returned extremely small p-values for both AAPL and MSFT, so I reject the unit-root null and conclude the daily log-return series are stationary. KPSS results are consistent with this, and ACF/PACF plus Ljung–Box show no meaningful autocorrelation in the mean, implying a near-zero constant mean is adequate. Practically, this means I can model returns with ARMA/ARIMA without differencing (d=0) and obtain valid inference. The predictability is not in the mean but in the variance: AAPL shows clear ARCH effects, so GARCH-type models (with Student-t errors) are appropriate for volatility forecasting and risk (e.g., VaR/ES). MSFT shows no strong ARCH at tested lags, so a homoskedastic error model may suffice—though a simple GARCH can be compared by AIC/BIC. If price forecasts are needed, I’ll model returns and cumulate them rather than modeling prices directly.

---

## 🧠 Bonus Challenge (Optional):

### 9. Simulate two series using Python: one stationary and one non-stationary. Describe the visual and statistical differences.

(Hint: Try using `np.random.normal()` for stationary and `np.cumsum()` for non-stationary.)

---

✅ When complete, commit this file as:  
`notes/week2_written_exercise.md`

