# Market Risk Models

Quantitative risk models built in Python, replicating frameworks used by risk desks under Basel III.

| # | Model | Asset | Method |
|---|---|---|---|
| 01 | [GARCH(1,1) Dynamic VaR](./01_GARCH_Dynamic_VaR/) | Zomato (ETERNAL.NS) | MLE, Backtesting |
| 02 | [Monte Carlo VaR](./02_MonteCarlo_VaR/) | Nifty 50 (^NSEI) | Historical Bootstrap |

---

## 01. GARCH(1,1) — Dynamic VaR & Expected Shortfall | Zomato (ETERNAL.NS)

Builds a complete market risk framework on Zomato daily price data from NSE listing (July 2021) through May 2026.

| Metric | Value |
|---|---|
| α (shock sensitivity) | 0.0999 |
| β (persistence) | 0.7989 |
| α + β | 0.8988 (stationary) |
| Long run daily volatility | ~3.02% |
| VaR breach rate | 1.20% |
| Expected Shortfall (99%) | -10.18% |

---

## 02. Monte Carlo Simulation — VaR & Expected Shortfall | Nifty 50 (^NSEI)

Estimates 10-day, 99% VaR and Expected Shortfall for a ₹1,00,000 Nifty 50 portfolio using historical bootstrapped Monte Carlo simulation.

| Metric | Value |
|---|---|
| 10-Day VaR (99%) | ₹9,759.80 |
| 10-Day ES (99%) | ₹12,416.09 |

---

**Author:** Yusuf Sayeed | FRM Part I Cleared | FMVA
