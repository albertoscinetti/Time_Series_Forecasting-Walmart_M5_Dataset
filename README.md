# Time Series Forecasting with Advanced Models - Walmart M5 Dataset 📈

This project explores advanced time series forecasting techniques to predict daily sales for 3,049 food products at Walmart's TX3 store in Texas. Forecasts are generated for the next 28 days, utilizing both univariate and multivariate models such as ARIMA, ETS, SNAIVE, TSLM, and PROPHET. By incorporating explanatory variables like weekday effects, SNAP eligibility, and holiday indicators, the project enhances prediction accuracy for stock optimization.

---

## **Models Used**

### 1. **ARIMA (Autoregressive Integrated Moving Average)**
   - **ARIMA:** Baseline univariate model using only `items_sold`.
   - **ARIMA1:** Multivariate model with `weekday`, `snap_TX`, and `is_holiday` as predictors.
   - **ARIMA2:** Multivariate model with `weekday` and `snap_TX` predictors.

### 2. **ETS (Error, Trend, Seasonality)**
   - Focuses on additive and multiplicative combinations of error, trend, and seasonal components.

### 3. **SNAIVE (Seasonal Naive)**
   - Relies on the most recent observed seasonal patterns for forecasting.

### 4. **TSLM (Time Series Linear Model)**
   - Incorporates predictors:
     - `trend()`
     - `season()`
     - `is_holiday`
     - `snap_TX`

### 5. **PROPHET**
   - A robust forecasting tool by Facebook that uses:
     - `weekday`
     - `is_holiday`
     - `snap_TX`

---

## **Dataset**

The dataset is derived from the **M5 Forecasting - Accuracy** competition and contains:
1. **`calendar_afcs2024.csv`**: Metadata about dates (e.g., holidays, weekdays, SNAP eligibility).
2. **`sell_prices_afcs2024.csv`**: Weekly product prices.
3. **`sales_train_validation_afcs2024.csv`**: Historical daily unit sales (training data).
4. **`sales_test_validation_afcs2024.csv`**: Testing data for the forecast horizon (28 days).
5. **`sample_submission_afcs2024.csv`**: Template for forecast submissions.

