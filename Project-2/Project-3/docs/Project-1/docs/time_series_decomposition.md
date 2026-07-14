# Time Series Decomposition

## What is Time Series Decomposition?

Time Series Decomposition is the process of breaking a time series dataset into its main components. It helps analysts understand the underlying patterns in the data and improves forecasting accuracy.

## Components of Time Series

### 1. Trend

Trend represents the long-term movement of data over time.

Example:
Monthly sales increase steadily from 500 units to 1200 units over one year.

### 2. Seasonality

Seasonality represents patterns that repeat at regular intervals, such as monthly, quarterly, or yearly.

Example:
Ice cream sales increase every summer.

### 3. Residual (Noise)

Residual is the random variation left after removing the trend and seasonal components. These variations are caused by unexpected events or random factors.

Example:
A sudden drop in sales due to bad weather.

## Types of Time Series Decomposition

### Additive Model

Used when seasonal fluctuations remain approximately constant over time.

Formula:
Time Series = Trend + Seasonality + Residual

### Multiplicative Model

Used when seasonal fluctuations increase or decrease with the trend.

Formula:
Time Series = Trend × Seasonality × Residual

## Why is Time Series Decomposition Important?

- Identifies long-term trends.
- Detects seasonal patterns.
- Improves forecasting accuracy.
- Helps businesses make better decisions.
- Supports demand forecasting and inventory planning.

## Business Use Case

A supermarket analyzes three years of sales data. By separating trend and seasonal effects, the company predicts future demand more accurately and avoids stock shortages during festivals.

## Conclusion

Time Series Decomposition helps businesses understand historical data by separating trend, seasonality, and random variations. It is an essential step before building forecasting models.

## References

- Statsmodels Documentation
- Microsoft Learn
- IBM Data Analytics Documentation
