# Week 2 – Time Series Stationarity & Statistical Analysis

## Overview
This week focused on foundational techniques in time series analysis for financial data. The primary objective was to evaluate the stationarity of daily log returns of two selected stocks (AAPL and MSFT), and determine whether their statistical properties were suitable for modeling and forecasting.

## Key Topics Covered
- Log and simple return calculation
- Moving averages and rolling statistics
- Stationarity in time series
- Autocorrelation (ACF) and partial autocorrelation (PACF)
- Augmented Dickey-Fuller (ADF) and KPSS stationarity tests
- ARCH effects and volatility modeling with GARCH

## Concepts Learned

### Stationarity
A stationary time series has constant mean and variance over time. Stationarity is critical in time series modeling because many models (ARIMA, GARCH) assume it. Returns are typically stationary, while prices are not.

### Returns
- **Simple returns**: \( R_t = \frac{P_t - P_{t-1}}{P_{t-1}} \)
- **Log returns**: \( r_t = \log\left(\frac{P_t}{P_{t-1}}\right) \)

### ACF and PACF
- ACF shows total correlation at each lag
- PACF isolates direct correlation with a given lag, removing intermediate effects
- Used to identify model structure (e.g., AR/MA orders)

### Statistical Testing
- **ADF Test**: Tests for unit root (non-stationarity); p < 0.05 suggests stationarity
- **KPSS Test**: Tests for stationarity; p > 0.05 supports stationarity
- **ARCH LM Test**: Detects volatility clustering (heteroskedasticity)

## Results Summary

| Metric | AAPL | MSFT |
|--------|------|------|
| ADF p-value | ≈ 7.64e-15 | ≈ 2.21e-29 |
| KPSS p-value | > 0.1 | > 0.1 |
| Stationary? | Yes | Yes |
| ARCH Effect? | Present | Not significant |

## Modeling Insights
- The return series for both AAPL and MSFT are stationary without differencing.
- No strong autocorrelation was found in returns, indicating limited predictability in the mean.
- AAPL returns exhibit volatility clustering, making it suitable for GARCH modeling.
- MSFT returns appear homoskedastic, but GARCH can be tested as an alternative.

## Deliverables
- `week2_time_series.ipynb`: Full analysis of returns, ACF/PACF, stationarity tests, and volatility modeling
- `notes/week2_written_exercise.md`: Conceptual answers and interpretation of results
