# Risk-Constrained Monte Carlo Portfolio Simulation and Optimization Using NSE Equities and Gold

This project simulates long-term portfolio returns using Monte Carlo methods, applies risk-aware constraints, and optimizes asset allocations based on Sharpe ratio. It uses real stock data from the National Stock Exchange of India (NSE) for large-cap equities and a gold ETF

---

## Project Overview

- **Objective**: Evaluate and optimize a long-term investment strategy using probabilistic simulations.
- **Assets Used**:
  - NSE-listed equities: RELIANCE, INFY, HDFCBANK, TATAMOTORS, ITC
  - Gold ETF: GOLDBEES
- **Time Horizon**: 1-year and 10-year forward simulations
- **Weighting Strategy**: Aggressive equity bias (90% equity, 10% gold), later optimized under constraints.

---

## Key Features

- **Monte Carlo Simulation**: 15,000+ portfolio paths using multivariate normal log returns.
- **Risk Awareness**:
  - Uses Ledoit-Wolf shrinkage for stable covariance estimation
  - 5% Value-at-Risk (VaR) calculation
  - Sharpe ratio maximization with weight constraints
- **Constraints Enforced**:
  - Individual asset weight: **min 5%**, **max 40%**
  - Portfolio weights sum to 1
- **Optimization**: Monte Carlo-based search for max Sharpe portfolio within constraints.

---

## Outputs

- Simulated 1Y and 10Y portfolio return distributions
- Efficient frontier plotted using 15,000 simulated portfolios
- Portfolio growth paths over 252 and 2520 trading days
- Final optimized asset allocation and metrics:
  - **Expected Return**
  - **Annualized Volatility**
  - **Sharpe Ratio**

---

## File Structure

- `MonteCarloPortfolioSimulation_Improved.py`: Main script containing all code for simulation, optimization, and visualization.
- `*.csv`: Historical price data for each asset (must include columns like `Date` and `Close`).
- `README.md`: This file.

---

## ▶️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/monte-carlo-portfolio-nse.git
   cd monte-carlo-portfolio-nse
