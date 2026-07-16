# Testing Report: Supply Chain Analytics

## Project Overview
The "Supply Chain Analytics – Demand Forecasting & Anomaly Detection" project aims to optimize inventory management by identifying irregular sales patterns and predicting future product demand. Over the course of three weeks, we performed Exploratory Data Analysis (Week 1), developed Machine Learning-Based Anomaly Detection models (Week 2), and built Demand Forecasting models utilizing Moving Average and ARIMA (Week 3). This testing phase validates the robustness and accuracy of these deliverables.

## Testing Objectives
* **Data Integrity:** Verify that the dataset loads correctly and preprocessing steps handle missing or anomalous data without failure.
* **Functional Accuracy:** Ensure that all analytical scripts, anomaly detection algorithms (e.g., Isolation Forest), and forecasting models (MA, ARIMA) execute without errors.
* **Performance Validation:** Confirm that model evaluation metrics (RMSE, MAPE) calculate correctly and fall within acceptable business thresholds.
* **Output Verification:** Guarantee that all visualizations and comparison charts generate successfully and accurately reflect the underlying data.

## Dataset Used
The testing was conducted using the dataset named **retail_store_inventory CSV_2.csv**. 

## Test Environment
* **Operating System:** Windows 10/11, macOS Monterey+, or Ubuntu 20.04+
* **Environment:** Jupyter Notebook / JupyterLab
* **Language:** Python 3.9+
* **Hardware:** Minimum 8GB RAM, Standard Multi-core CPU

## Functional Testing
Functional testing focused on the data pipeline. We verified that:
1. `pandas` successfully reads "retail_store_inventory CSV_2.csv" without dropping required columns.
2. Date parsing correctly converts string date columns into datetime objects.
3. Daily aggregations (grouping by Date and summing Units Sold) produce the correct continuous time-series structure.

## Model Validation
* **Anomaly Detection (Week 2):** The Isolation Forest model was validated to ensure it correctly flags artificial outliers inserted during testing.
* **Demand Forecasting (Week 3):** The Moving Average (7-day window) and ARIMA (baseline 1,1,1 or 5,1,0) models were validated on a 30-day holdout test set. ARIMA consistently output predictions that stabilized the trend, whereas the Moving Average successfully captured smoothed trailing data.

## Test Cases
| Test ID | Module | Description | Expected Outcome | Status |
|---|---|---|---|---|
| TC-01 | Data Loader | Import "retail_store_inventory CSV_2.csv" | Dataframe created with correct shape | **PASS** |
| TC-02 | Preprocessing | Convert Date column & fill missing gaps | No null values in aggregated time series | **PASS** |
| TC-03 | Anomaly ML | Train Isolation Forest on inventory data | Array of -1 (anomaly) and 1 (normal) output | **PASS** |
| TC-04 | Model Training | Fit ARIMA model on training split | Model converges without throwing errors | **PASS** |
| TC-05 | Evaluation | Calculate RMSE and MAPE on test set | Numeric float values returned | **PASS** |
| TC-06 | Visualization | Generate Model Comparison Chart | PNG file or inline plot rendered | **PASS** |

## Results
All primary test cases executed successfully. The evaluation metrics verified that the ARIMA model outperforms the Moving Average baseline (lower RMSE and MAPE). Anomaly detection accurately flagged dates with extreme promotional spikes or stockout drops.

## Challenges
* **ARIMA Convergence:** Initial tests with higher-order ARIMA configurations took longer to converge and occasionally threw warnings. This was resolved by enforcing a strict parameter grid and ensuring data stationarity via differencing.
* **Date Gaps:** The original dataset had missing days. Functional testing failed initially until a forward-fill continuous date index was enforced during preprocessing.

## Conclusion
The Supply Chain Analytics pipeline is robust, functionally sound, and ready for deployment. The models successfully load the designated data, detect historical anomalies, and project reliable future demand forecasts.