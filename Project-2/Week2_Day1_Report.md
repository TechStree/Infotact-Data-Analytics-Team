# Week 2 Day 1 Report

## Objective

To analyze the distribution of demand and inventory data and identify potential anomalies before applying anomaly detection techniques.

## Units Sold Distribution Analysis

A histogram with KDE was generated to analyze the distribution of Units Sold.

### Findings

* The distribution is positively skewed.
* Most observations are concentrated at lower sales values.
* The frequency decreases as Units Sold increases.
* A long right tail is visible, indicating occasional high-demand periods.

### Descriptive Statistics

* Mean: 136.39
* Median: 108
* Standard Deviation: 108.94
* Minimum: 0
* Maximum: 496

Since the mean is greater than the median, the distribution is positively skewed.

---

## Units Sold Boxplot Analysis

A boxplot was created to identify potential outliers.

### Findings

* Several observations lie beyond the upper whisker.
* Potential outliers are present in the range of approximately 430–500 units.
* These values may represent demand spikes or unusual sales events.

---

## Inventory Level Distribution Analysis

A histogram with KDE was generated for Inventory Level.

### Findings

* Inventory values are distributed relatively evenly.
* No major skewness is observed.
* Inventory management appears consistent throughout the dataset.

### Descriptive Statistics

* Mean: 274.64
* Median: 274
* Standard Deviation: 129.73
* Minimum: 50
* Maximum: 500

Since the mean and median are nearly equal, the distribution is approximately symmetric.

---

## Inventory Level Boxplot Analysis

A boxplot was generated for Inventory Level.

### Findings

* No significant outliers were detected.
* Inventory levels remain within expected operational ranges.

---

## Conclusion

Initial analysis indicates that Units Sold contains potential anomalous observations due to visible outliers and positive skewness. Inventory Level appears stable and does not exhibit abnormal behavior. These findings provide the foundation for applying Z-Score and IQR-based anomaly detection methods in the next phase.
