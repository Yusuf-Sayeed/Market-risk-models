# Market Risk Models

Quantitative risk models built in Python, replicating frameworks used by risk desks under Basel III.

---

## 1. GARCH(1,1) — Dynamic VaR & Expected Shortfall | ETERNAL.NS (Zomato)

**File:** `Eternal_GARCH_Model.ipynb`

Builds a complete market risk framework from scratch on Zomato (ETERNAL.NS) daily price data from NSE listing date (July 2021) through May 2026.

**What it covers:**
- Log return computation and volatility clustering analysis
- GARCH(1,1) conditional volatility estimation via Maximum Likelihood
- Parameter interpretation: ω, α (shock sensitivity), β (persistence)
- 1-day 99% Value at Risk (VaR) using GARCH conditional volatility
- Backtesting: 14 breaches out of 1,163 days (1.20% vs theoretical 1%)
- Expected Shortfall (CVaR) at 99%: -10.18%

**Key results:**
| Metric | Value |
|--------|-------|
| α (shock sensitivity) | 0.0999 |
| β (persistence) | 0.7989 |
| α + β | 0.8988 (stationary) |
| Long run daily volatility | ~3.02% |
| VaR breach rate | 1.20% |
| Expected Shortfall (99%) | -10.18% |

**Tools:** Python, pandas, numpy, arch, yfinance, matplotlib, scipy

---

## About

Built as part of a quantitative risk modelling portfolio targeting market risk and liquidity risk roles.

**Author:** Yusuf Sayeed | FRM Part 1 Cleared | FMVA (In Progress)
