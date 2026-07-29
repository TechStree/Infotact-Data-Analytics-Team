# Final Project Report

## 1. Introduction

Supply chain management plays a critical role in maintaining inventory efficiency and meeting customer demand. This project focuses on demand forecasting and anomaly detection using historical supply chain data.

The objective is to analyze sales patterns, identify unusual demand behavior, and forecast future demand to support inventory optimization.

---

## 2. Problem Statement

Organizations often face challenges such as:

* Overstocking inventory
* Stock shortages
* Demand fluctuations
* Unexpected anomalies

The project aims to build a data-driven solution that helps forecast demand and detect anomalies automatically.

---

## 3. Dataset Description

The dataset contains 73,100 records with the following features:

* Date
* Store ID
* Product ID
* Category
* Region
* Inventory Level
* Units Sold
* Units Ordered
* Demand Forecast
* Price
* Discount
* Weather Condition
* Holiday/Promotion
* Competitor Pricing
* Seasonality

---

## 4. Data Preprocessing

The following preprocessing steps were performed:

* Converted Date column into datetime format
* Sorted records chronologically
* Checked missing values
* Verified data consistency
* Created daily demand time series
* Prepared dataset for forecasting models

---

## 5. Exploratory Data Analysis

Key findings:

* Average Demand: 136.46 units
* Average Inventory: 274.47 units
* Furniture category recorded the highest demand
* East region generated the highest sales performance

Demand trends remained relatively stable across the observation period.

---

## 6. Anomaly Detection

Three anomaly detection techniques were implemented:

### Z-Score Method

Used statistical deviation from the mean to identify extreme observations.

### IQR Method

Used quartile-based boundaries to identify outliers.

### Isolation Forest

Machine learning-based approach for detecting anomalies in sales behavior.

Isolation Forest detected the highest number of unusual observations.

---

## 7. Demand Forecasting

### Moving Average Model

A 7-day moving average was used as a baseline forecasting model.

Results:

* MAE: 904.00
* RMSE: 1125.00
* MAPE: 6.90%

### ARIMA Model

An ARIMA(5,1,0) model was developed for time-series forecasting.

Results:

* MAE: 901.61
* RMSE: 1118.03
* MAPE: 6.84%

---

## 8. Model Comparison

ARIMA achieved the lowest forecasting errors and demonstrated better predictive performance compared to the Moving Average approach.

Therefore, ARIMA was selected as the final forecasting model.

---

## 9. Streamlit Dashboard

An interactive Streamlit dashboard was developed to provide:

* Historical Demand Analysis
* Category-wise Demand Insights
* Region-wise Demand Insights
* Forecast Visualization
* Forecast Accuracy Metrics
* Business Recommendations

The dashboard enables stakeholders to analyze supply chain performance efficiently.

---

## 10. Business Insights

Major insights obtained:

* Furniture products contribute the highest demand volume.
* East region consistently performs better than other regions.
* Demand forecasting can significantly improve inventory planning.
* Early anomaly detection can reduce operational disruptions.

---

## 11. Recommendations

* Increase inventory allocation for Furniture products.
* Prioritize stock planning in the East region.
* Use ARIMA forecasting for procurement planning.
* Monitor anomalies regularly to prevent stockouts and excess inventory.

---

## 12. Conclusion

The project successfully developed a complete supply chain analytics solution capable of demand forecasting and anomaly detection.

The ARIMA model provided accurate forecasts while anomaly detection techniques highlighted unusual operational behavior.

The Streamlit dashboard transformed the analysis into a user-friendly business application that supports inventory optimization and data-driven decision-making.
