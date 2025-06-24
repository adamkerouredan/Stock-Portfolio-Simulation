# Stock-Portfolio-Simulation
# Stock Portfolio Simulation using Monte Carlo and Risk Metrics (VaR & CVaR)

This project simulates the performance of a diversified stock portfolio using Monte Carlo methods and evaluates downside risk through Value-at-Risk (VaR) and Conditional Value-at-Risk (CVaR). It serves as an academic yet practical exercise in quantitative portfolio analysis and risk management.

---

## Project Objectives

- Simulate future portfolio trajectories using historical covariance structure and Gaussian returns.
- Estimate risk metrics (VaR and CVaR) based on the simulated distribution of terminal portfolio values.
- Provide a visual and quantitative framework for portfolio scenario analysis.
- Explore Cholesky decomposition as a method to preserve correlation between assets.

---

## Methodology

- **Assets**: AAPL, GOOGL, MSFT, MCD, TTE, MC.PA
- **Historical data**: Fetched using `yfinance` and `pandas_datareader`
- **Monte Carlo logic**:
  - Use Cholesky decomposition to correlate daily shocks across assets
  - Simulate 1,000 portfolio paths over 365 days
  - Initial portfolio value: $1,000
  - Portfolio weights randomly generated and normalized
  - Daily portfolio returns computed as dot product of asset returns and weights

---

## Risk Metrics

- **Value-at-Risk (VaR)**: Loss threshold not exceeded with 95% confidence
- **Conditional VaR (CVaR)**: Expected loss given that the loss exceeds the VaR threshold

These are computed from the empirical distribution of final portfolio values across simulations.

---

## Key Outputs

- **Monte Carlo simulations** of portfolio value over time
- **VaR line** (dashed blue) and **CVaR line** (dashed red) displayed on the chart
- **Textual interpretation** of both metrics for investor comprehension

![Screenshot 2025-06-25 00 08 35](https://github.com/user-attachments/assets/5d8e5a56-f7dc-4781-a382-953c4a4495da)


