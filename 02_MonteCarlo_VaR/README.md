# Monte Carlo Simulation — Value at Risk (VaR) | Nifty 50

Estimates **10-day, 99% VaR and Expected Shortfall** for a ₹1,00,000 Nifty 50 portfolio using Monte Carlo simulation with historical bootstrapping.

---

## Methodology

- **Data:** Nifty 50 daily close prices from Jan 2020 (`^NSEI` via `yfinance`)
- **Returns:** Simple daily returns — (Pt / Pt-1) − 1
- **Simulation:** 10,000 paths × 10 days, resampled from historical returns with replacement
- **No distributional assumption** — purely empirical, non-parametric bootstrap

---

## Risk Metrics

| Metric | Definition |
|---|---|
| VaR (99%) | Maximum expected loss 99% of the time over 10 days |
| ES / CVaR (99%) | Mean loss across all tail scenarios beyond VaR |

ES is a coherent risk measure and preferred over VaR under Basel III / FRTB.

---

## Output

10-Day VaR (99%): ₹9,759.80
10-Day ES  (99%): ₹12,416.09

A ₹1,00,000 Nifty 50 portfolio has a 1% chance of losing more than ₹9,759 over 10 days. In the worst 1% of scenarios, the average loss is ₹12,416.

---

## Tech Stack

`numpy` `pandas` `scipy` `yfinance` `matplotlib`

---

## Author

Yusuf Sayeed | FRM Part I Cleared | FMVA
