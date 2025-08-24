From week2_time_series.ipynb

Are the log returns stationary?

From what i tested:

I assessed the stationarity of daily log returns for AAPL and MSFT (1 year of trading days) using complementary tests:

* ADF (Augmented Dicker-Fuller):
    - H0: series has a unit root (non-stationary)
* KPSS (Kwiatkowski-Phillips-Schmidt-Shin):
    - H0: series is (trend-)stationary
* Ljung-Box (on returns): tests for autocorrelation in the mean
* ARCH LM (on returns): tests for conditional heteroskedasticity (volatility clustering)

| Test                         |                        AAPL |                         MSFT | Interpretation                                                       |
| ---------------------------- | --------------------------: | ---------------------------: | -------------------------------------------------------------------- |
| **ADF (log returns)**        | stat = −8.973, p = 7.64e−15 | stat = −16.486, p = 2.21e−29 | **Reject H₀ (unit root)** → supports stationarity                    |
| **KPSS (log returns)**       |     stat = 0.068, p ≈ 0.10† |      stat = 0.220, p ≈ 0.10† | **Fail to reject H₀ (stationary)**                                   |
| **Ljung–Box(20) on returns** |                   p = 0.109 |                    p = 0.627 | No significant autocorrelation in the mean                           |
| **ARCH LM(10)**              |                p = 3.08e−06 |                    p = 0.907 | **AAPL:** volatility clustering; **MSFT:** no evidence at these lags |

+ '+' Interpolation warning indicates the statistic is so small the true p-value is >= the table's upper bound, which is even more stronger evidance for stationarity

In conclusion:

* For both tickers, the ADF strongly rejects a unit root and the KPSS does not reject stationarity.
* Therefor, daily log returns appear stationary in mean over the sample
* There is no meaningful autocorrelation in returns (Ljung-box)
* AAPL shows conditional heteroskedasticity (ARCH) effects, meaning volatility changes over time; MSFT does not at tested lags

Why stationary matters:

* Many time-series models assume stationarity so their parameters are meaningful and inference is valid
* Modeling prices directly often violates stationarity (unit root); modeling returns typically satisfies it - reducing risk of spurious regression and making forecasts and confidance intervals more reliable
* Even when the mean is stationary, the variance may not be constant (as with AAPL). In such cases, volatility models like GARCH(1,1) with heavy-tailed errors (Student-t) are appropriate

