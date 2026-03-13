# Do Crypto Markets Generate Volatility in Borsa Istanbul?
### Evidence from a VARX with Weekly Data

**Authors:** Yiğit Erdoğan · Halil İbrahim Özsoy · Yaman Dinçkan
**Course:** IKT 451 — Applied Econometrics: Time Series Analysis
**Date:** August 2025

---

## Overview

This empirical study investigates whether cryptocurrency markets contribute to the volatility of **Borsa Istanbul (BIST 100 / XU100)**. Using weekly observations spanning from **November 2017 to August 2025** (~406 data points), we estimate a Vector Autoregression with Exogenous Controls (**VARX**) to test whether crypto shocks transmit meaningfully to Turkish equity markets.

**Key finding:** Cryptocurrency innovations have **economically small and statistically weak** effects on BIST volatility. At 10-week horizons, over 95–97% of XU100 return variance is explained by its own shocks — crypto contributes only a few percent at most.

---

## Methodology

| Step | Description |
|------|-------------|
| **Data** | Weekly log-returns: BTC, ETH, BNB, XRP composite (L_AVGCRP) + BIST 100 (L_XU100) |
| **Controls** | S&P 500, Gold, USD/TRY, U.S. Fed Rate, VIX (exogenous) |
| **Stationarity** | ADF & Phillips-Perron unit root tests → first-differenced to log-returns |
| **Volatility Proxy** | Absolute returns: V_AVGCRP and V_XU100 |
| **Model** | Bivariate VARX(2) with contemporaneous + lagged exogenous controls |
| **Identification** | Cholesky orthogonalization with ordering [Crypto → XU100] |
| **Robustness** | Principal-component crypto factor + COVID-period dummy |

---

## Main Results

- **Granger Causality:** Crypto returns do **not** Granger-cause XU100 returns at the 5% level, once global macro controls are included.
- **Impulse Response Functions:** A one-standard-deviation shock to crypto produces near-zero response in XU100 after 1–2 weeks, well within confidence bands at all horizons up to 10 weeks.
- **Forecast Error Variance Decomposition (FEVD):** XU100 variance is driven overwhelmingly (~95–97%) by its own shocks.
- **Historical Decomposition:** Crypto factor explains a minimal share of XU100 fluctuations throughout the sample period.
- **Diagnostics:** No serial correlation (LM & Portmanteau tests), stable model (all inverse AR roots inside unit circle).

---

## Repository Contents

| File | Description |
|------|-------------|
| `Do_Crypto_Markets_Generate_Volatility_in_Borsa_Istanbul.docx` | Full empirical report with tables, figures, and discussion |

---

## Tools & Software

- **EViews** — VARX estimation, unit root tests, IRFs, FEVD
- **Microsoft Word** — Report writing and formatting

---

## Keywords

`Cryptocurrency` · `Borsa Istanbul` · `BIST 100` · `VARX` · `Granger Causality` · `Impulse Response Functions` · `Variance Decomposition` · `Volatility Transmission` · `Time Series Analysis`
