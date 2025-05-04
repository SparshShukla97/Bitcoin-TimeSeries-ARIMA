




# 📈 Bitcoin Time Series Forecasting Using ARIMA Models

[bitcoin_logo]()

This project provides a detailed time series analysis and forecasting of the **monthly Bitcoin index (USD)** from **August 2011 to January 2025**. The analysis was conducted as part of the **MATH1318 - Time Series Analysis** course at **RMIT University**.

The core objective is to build an effective and interpretable **ARIMA(p,d,q)** model to forecast future Bitcoin prices and explore its trends, variance, and statistical properties.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Tech Stack](#tech-stack)
- [Methodology](#methodology)
- [Key Results](#key-results)
- [Folder Structure](#folder-structure)
- [How to Run](#how-to-run)
- [Forecast Plot (Sample)](#forecast-plot-sample)
- [References](#references)
- [Author](#author)
- [License](#license)

---

## 📊 Project Overview

The analysis includes:

- Descriptive statistics
- Stationarity checks (ADF, KPSS)
- Log and Box-Cox transformations
- ACF, PACF, and EACF analysis
- Model identification using BIC
- ARIMA model fitting, diagnostics, and evaluation
- Forecasting with 95% confidence intervals

---

## 🎯 Objectives

- Structure and clean the Bitcoin price dataset.
- Perform transformation and differencing to achieve stationarity.
- Identify optimal ARIMA model using advanced diagnostic tools.
- Compare candidate models using AIC, BIC, and MSE.
- Evaluate residuals for white noise and normality.
- Forecast Bitcoin prices for the next 12 months with uncertainty bounds.

---

## 🛠 Tech Stack

- **Language**: R
- **Core Libraries**:
  - `forecast`
  - `tseries`
  - `TSA`
  - `ggplot2`
  - `lubridate`
  - `tidyverse`

---

## 🔍 Methodology

The following steps were followed:

1. **Data Preparation**:
   - Monthly Bitcoin prices from CSV converted to time series object using `ts()`.

2. **Exploratory Data Analysis**:
   - Time series plot, histogram, LOESS trend smoother, Q-Q plot.

3. **Stationarity Check**:
   - ADF and KPSS tests confirm non-stationarity → differencing applied.

4. **Transformations**:
   - Log and Box-Cox transformations stabilize variance.

5. **Model Identification**:
   - Used ACF, PACF, EACF, and BIC subset plots to suggest `ARIMA(p,d,q)`.

6. **Model Fitting & Evaluation**:
   - Compared models like ARIMA(1,1,1), ARIMA(2,1,3) etc.
   - Selected ARIMA(2,1,2) as optimal based on AIC, BIC, and residual diagnostics.

7. **Forecasting**:
   - Forecasted Bitcoin prices for 12 months with confidence intervals.

---

## ✅ Key Results

| Model        | AIC   | BIC   | MSE    |
|--------------|-------|-------|--------|
| ARIMA(2,1,2) | 29.90 | 45.30 | 0.0646 |

- ✅ **Selected Model**: `ARIMA(2,1,2)`
- ✅ **Residuals**: White noise confirmed (no autocorrelation)
- ✅ **Q-Q Plot & Histogram**: Residuals approximate normality
- ✅ **Forecast**: Suggests upward trend with increasing uncertainty

---

Bitcoin-TimeSeries-ARIMA/
│
├── assignment_2.R             # Final analysis script
├── TS-Assignment_2.docx       # Submitted report
├── bitcoin_analysis.Rmd       # (Optional) R Markdown version of the analysis
├── data/
│   └── bitcoin_monthly.csv    # Input dataset
├── plots/
│   ├── ts_plot.png            # Time series plot
│   ├── forecast_plot.png      # Forecast with CI
│   └── residuals_qq.png       # Diagnostic plots
├── README.md                  # This file
