# Week 5 – Volatility & Risk Modeling

## Learning Objectives

- Understand different types of volatility: realized, implied, and historical X
- Calculate historical volatility from return series using rolling windows X
- Visualize volatility over time and relate patterns to major market events X
- Learn the concept of volatility clustering and conditional heteroskedasticity 
- Implement ARCH and GARCH models to model time-varying volatility
- Compare GARCH forecasts to naive volatility estimates
- Diagnose model performance using residual plots and statistical tests

## Reading

- Textbook: Chapter 14 – Conditional Heteroskedasticity Models
  - Focus Sections: 14.1 – 14.4

## Coding Assignment

- Use TSLA return data (from Week 3–4)
- Compute and plot 20-day rolling standard deviation of returns
- Fit a GARCH(1,1) model using the `arch` library
- Plot and compare GARCH vs rolling volatility
- Diagnose model performance (ACF of residuals, Q-Q plot, Ljung-Box test)

## Written Exercise (`notes/week5_written_exercise.md`)

Answer the following:
1. What is volatility clustering and why is GARCH useful?
2. How do GARCH estimates differ from simple rolling std dev?
3. What do the diagnostics say about model fit?
4. When and how would volatility forecasts be used in practice?

## Deliverables

- `week5_volatility_modeling.ipynb`
- `notes/week5_written_exercise.md`
- Optional: `charts/week5_volatility.png`
