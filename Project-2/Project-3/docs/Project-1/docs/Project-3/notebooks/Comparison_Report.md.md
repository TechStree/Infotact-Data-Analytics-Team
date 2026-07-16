# Comparison Report: ML vs. Statistical Anomaly Detection
**Project:** Supply Chain Analytics – Demand Forecasting & Anomaly Detection (Week 2)

## 1. Introduction
The objective of this analysis is to identify operational anomalies in retail supply chain data. Anomaly detection is critical for recognizing unexpected supply shortages, anomalous demand spikes, or data entry errors. This report evaluates and compares two distinct methodologies: Machine Learning (Isolation Forest) and Statistical (Z-Score).

## 2. Methodology
The analysis was conducted on the daily aggregated dataset encompassing `Units Sold` and `Inventory Levels`.
- **Machine Learning Method (Isolation Forest):** An unsupervised learning algorithm that isolates anomalies by randomly selecting features and split values. It evaluates the dataset in multiple dimensions (combining Sales and Inventory). The contamination rate was set to 5%.
- **Statistical Method (Z-Score):** A standard univariate statistical measure calculating how many standard deviations a data point is from the historical mean. A rigid threshold of absolute value > 3 was applied to `Units Sold` to flag anomalies.

## 3. Isolation Forest Results
- **Detection Profile:** The Isolation Forest successfully identified anomalies that deviated from the normal clustering of daily operations.
- **Characteristics:** Because it evaluates multiple variables simultaneously, it flagged days where sales and inventory ratios behaved illogically (e.g., high inventory despite a massive sales spike, or low inventory with very low sales).
- **Visualization Context:** On the timeline chart, the flagged points (red) do not solely rest at the extreme peaks of the graph, highlighting the algorithm's ability to spot hidden structural issues.

## 4. Statistical Method Results
- **Detection Profile:** The Z-Score method acted as a strict, hard boundary. It only flagged the absolute most extreme outlier days in the entire two-year dataset.
- **Characteristics:** It operated under the assumption of a normal distribution. Consequently, it missed subtle operational anomalies and only alerted on massive volume spikes.
- **Visualization Context:** On the timeline chart, the flagged points (orange) sit exclusively at the very highest peaks of the sales line, representing days that breached the 99.7% confidence interval.

## 5. Comparison
| Feature | Isolation Forest (Machine Learning) | Z-Score (Statistical) |
| :--- | :--- | :--- |
| **Dimensionality** | Multivariate (Analyzes multiple metrics at once) | Univariate (Analyzes one metric at a time) |
| **Assumptions** | Non-parametric (No normal distribution required) | Parametric (Assumes data is normally distributed) |
| **Sensitivity** | High (Detects subtle, complex outliers) | Low (Detects only extreme volume variations) |
| **Use Case Fit** | Best for finding complex supply chain disruptions. | Best for simple, hard-coded dashboard alerts. |

## 6. Business Insights
1. **Multidimensional Alerts are Crucial:** Relying solely on volume thresholds (Z-Score) leaves the business blind to inventory desynchronization. Using Isolation Forest allows the business to see when stock levels are behaving irregularly in relation to baseline demand.
2. **Predicting the Extremes:** The extreme peaks flagged by the Z-Score are likely driven by macro-events (holidays, deep discounts). The business should analyze these specific dates cross-functionally with the Marketing department to ensure proper safety stock is ordered ahead of similar future events.
3. **Automated Monitoring:** The Machine Learning approach provides a dynamic baseline that doesn't require constant manual recalculation, making it ideal for integration into automated supply chain monitoring software.

## 7. Conclusion
While the Z-Score method provides a quick and mathematically simple way to identify extreme historical demand spikes, it is insufficient for modern supply chain analytics. The **Isolation Forest algorithm is vastly superior** for this use case. By analyzing multiple dimensions simultaneously and not relying on the assumption of data normality, Isolation Forest provides deeper, more actionable insights into supply chain friction, allowing inventory managers to react to systemic anomalies before they result in critical stockouts.