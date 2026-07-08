# Initial EDA Report

## Dataset Overview

* Total Rows: 73,100
* Total Columns: 15

## Data Types

### Numerical Columns

* Inventory Level
* Units Sold
* Units Ordered
* Demand Forecast
* Price
* Discount
* Holiday/Promotion
* Competitor Pricing

### Categorical Columns

* Date
* Store ID
* Product ID
* Category
* Region
* Weather Condition
* Seasonality

## Missing Values

No missing values were found in the dataset.

Total Missing Values: 0

## Duplicate Records

No duplicate records were found.

Total Duplicate Records: 0

## Statistical Summary

### Inventory Level

* Mean: 274.47
* Minimum: 50
* Maximum: 500

### Units Sold

* Mean: 136.46
* Minimum: 0
* Maximum: 499

### Units Ordered

* Mean: 110.00
* Minimum: 20
* Maximum: 200

### Demand Forecast

* Mean: 141.49
* Minimum: -9.99
* Maximum: 518.55

### Price

* Mean: 55.14
* Minimum: 10.00
* Maximum: 100.00

## Initial Observations

* The dataset is complete with no missing values or duplicate records.
* Inventory levels range from 50 to 500 units across stores and products.
* Demand Forecast contains some negative values, which may require further investigation during preprocessing.
* Holiday and Promotion activities are evenly distributed in the dataset.
* The dataset contains sufficient information for demand forecasting and anomaly detection tasks.
