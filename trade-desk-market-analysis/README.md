# The Trade Desk (TTD) vs. the S&P 500

**Researcher:** Sachhyam Manandhar  
**Course project:** Spring 2026  
**Tools:** R, R Markdown, quantmod, ggplot2, econometric modeling

## Research question

How did the adjusted daily share price of **The Trade Desk (TTD)** move relative to the S&P 500 index (`^GSPC`) from March 2021 through February 2026? Do more flexible descriptive model specifications show patterns missed by a simple linear regression?

## What I did

- Downloaded historical daily price data via Yahoo Finance using R's `quantmod`.
- Explored adjusted-price distributions, candlestick charts, moving averages, correlations, and time-series decomposition.
- Fit a linear regression and explored LOESS and polynomial models, comparing model fit across specifications.
- Communicated the data patterns and modeling limitations in a written R Markdown analysis.

## Key takeaway

The original linear price-level model reported a statistically detectable but weak descriptive association. More flexible models increased *in-sample* fit, but that does **not** demonstrate predictive accuracy.

**Important limitations:** Price levels are potentially nonstationary and serially dependent. These estimates are descriptive, not causal effects, estimates of market beta, validated forecasts, or trading recommendations.

## Project files

- [`analysis.Rmd`](analysis.Rmd) — a lightly edited version of the original R Markdown course analysis
- [Data notes](data/README.md) — source and date range

The analytical source has **not been independently rerun** since being prepared for this repository. Some outputs depend on live data availability and the user's local R environment.

## Reproduce the analysis

Install R, RStudio, and the required packages. Then open `analysis.Rmd` and knit it. The source loads packages including `quantmod`, `zoo`, `dplyr`, `ggplot2`, `lubridate`, `mgcv`, `tidyr`, and `kableExtra`:

```r
install.packages(c("rmarkdown", "knitr", "quantmod", "zoo", "dplyr",
                   "ggplot2", "lubridate", "mgcv", "tidyr", "kableExtra"))
rmarkdown::render("analysis.Rmd")
```

PDF output may also require a LaTeX installation (e.g., TinyTeX). The code retrieves Yahoo Finance data at runtime; data-provider changes may affect reproducibility.

*Academic research only; not investment advice.*
