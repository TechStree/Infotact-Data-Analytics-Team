# Forecast Analysis Report

## Demand Trend Analysis

Monthly demand remained relatively stable throughout 2022 and 2023.

Average monthly demand ranged between 390,000 and 438,000 units.

The highest demand month was:

- July 2023
- Total Units Sold: 437,919

The lowest complete month was:

- February 2023
- Total Units Sold: 385,168

January 2024 shows unusually low demand because only partial month data is available.

## Forecast Performance

ARIMA forecasting produced:

- MAE = 901.61
- RMSE = 1118.03
- MAPE = 6.84%

The forecast closely followed the average demand level and achieved acceptable prediction accuracy.

## Model Comparison

| Model | MAE | RMSE | MAPE |
|---------|---------|---------|---------|
| Moving Average | 904.00 | 1125.00 | 6.90 |
| ARIMA | 901.61 | 1118.03 | 6.84 |

ARIMA achieved the lowest error values and was selected as the best forecasting model.

## Business Interpretation

The demand pattern shows relatively stable sales with periodic fluctuations.

No strong long-term decline is observed.

The forecasting model can support:

- Inventory planning
- Demand estimation
- Replenishment decisions
- Supply chain optimization

## Conclusion

ARIMA is the recommended forecasting model for future demand prediction.
