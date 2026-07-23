# Week 3 Day 3 – ARIMA Demand Forecasting

## Objective

Develop an ARIMA forecasting model to predict future demand and evaluate forecasting performance.

---

## Data Preparation

- Converted Date column to datetime format.
- Aggregated Units Sold by Date.
- Sorted data chronologically.
- Set Date as index.

---

## Train-Test Split

- Training Data: 584 days
- Testing Data: 147 days

---

## ARIMA Model

Model Used:

ARIMA(5,1,0)

The model was trained on historical demand data and used to forecast future demand.

---

## Forecast Results

Forecast Length:

147 Days

Sample Forecast Values:

| Date | Forecast |
|--------|--------|
| 2023-08-08 | 14027.54 |
| 2023-08-09 | 13980.83 |
| 2023-08-10 | 13935.43 |
| 2023-08-11 | 13858.97 |
| 2023-08-12 | 14050.15 |

---

## Model Evaluation

| Metric | Value |
|----------|----------|
| MAE | 901.61 |
| RMSE | 1118.03 |
| MAPE | 6.84% |

---

## Interpretation

- Forecast error remained low.
- MAPE below 10% indicates strong forecasting accuracy.
- ARIMA successfully captured overall demand patterns.
- The model can be used as a reliable baseline forecasting solution.

---

## Visualizations Generated

- Daily Demand Trend
- ARIMA Forecast vs Actual Demand
- Forecast Error Distribution

---

## Conclusion

The ARIMA model achieved strong forecasting performance with a MAPE of 6.84%. It provides reliable future demand estimates and can support inventory planning and supply chain decision-making.
