# ✏️ Week 2 – Written Exercise: Stationarity & Time Series Analysis

## 🧠 Instructions:
Answer the following questions in your own words. You may refer to Chapter 12 of the textbook, your notebook, or external resources as needed. Submit this file with your answers added below each question.

---

## 📘 Section A: Concepts

### 1. What does it mean for a time series to be *stationary*? Why is stationarity important in time series modeling?

Stationary process is a type of stochastic process (random process) where the statistical properties, like the mean and variance do not change over time. Stationarity is a crucial concept in time series analysis because it simplifies modeling and forecasting. A stationary time series has statistical properties (mean, variance, autocovariance) that do not vary over time, making it easier to model patterns and predict future values. Non-stationary series, which exhibit trends or seasonality, can lead to inaccurate model results.

---

### 2. What is the difference between **autocovariance** and **autocorrelation**? Why is autocorrelation often preferred in practice?

---

### 3. Explain the purpose of the **Autocorrelation Function (ACF)** and **Partial Autocorrelation Function (PACF)**. What does a slow decay in the ACF indicate?

---

### 4. What is the null hypothesis of the **Augmented Dickey-Fuller (ADF)** test? What does a p-value < 0.05 suggest about the time series?

---

### 5. If you had a time series that was non-stationary, what steps could you take to make it stationary?

---

## 📊 Section B: Applied Interpretation

You generated the ACF, PACF, and performed the ADF test on your stock log returns. Based on your results:

### 6. What did your ACF and PACF plots show about autocorrelation in your return series?

---

### 7. What was the p-value of your ADF test? What was your conclusion — is your return series stationary?

---

### 8. What impact does your conclusion from Q7 have on your ability to use this series in future forecasting models?

---

## 🧠 Bonus Challenge (Optional):

### 9. Simulate two series using Python: one stationary and one non-stationary. Describe the visual and statistical differences.

(Hint: Try using `np.random.normal()` for stationary and `np.cumsum()` for non-stationary.)

---

✅ When complete, commit this file as:  
`notes/week2_written_exercise.md`

