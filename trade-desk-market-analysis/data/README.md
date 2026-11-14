# Data provenance

Daily historical adjusted prices are retrieved for **The Trade Desk (TTD)** and the **S&P 500 index (^GSPC)** through Yahoo Finance using the R `quantmod` package.

- **Requested period:** March 1, 2021 through March 1, 2026 (the end date is exclusive for some data retrieval functions).
- **Processing:** Trading-date alignment, removal of missing matched observations, descriptive statistics and modeling.
- **Data distribution:** No raw market prices are redistributed in this repository.

**Reproducibility:** Run `../analysis.Rmd` in an R environment with internet access. Historical provider revisions may affect results.
