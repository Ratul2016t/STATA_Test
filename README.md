 Diagnostics for Cobb-Douglas Production Function (Stata)

- **Model**: `ln_gdp = β₀ + β₁*ln_capital + β₂*ln_labor + ε`
- **Diagnostics:**
  - `vif` — Multicollinearity (VIF < 5 is OK)
  - `estat hettest` — Heteroskedasticity (p < 0.05 → use robust SEs)
  - `sktest resid` — Normality of residuals (p > 0.05 is OK)
  - `estat ovtest` — Model specification (p < 0.05 → misspecification)
  - `estat bgodfrey` — Autocorrelation (for time series/panel, p < 0.05 → autocorrelation)

Ensure `tsset year` or `xtset country year` is run before autocorrelation test.
