# Project 3 – Supply Chain Analytics

## Week 1 – Time-Series Data Preparation

### Objective
Prepare the retail inventory dataset for time-series forecasting and anomaly detection.

## Tasks Completed

- Loaded retail inventory dataset
- Inspected dataset structure
- Checked missing values
- Converted Date column to datetime# 📦 Project 2: Supply Chain Analytics – Time-Series Data Preparation & Decomposition

## 👤 Team Member
**Name:** Ananthsairam Goundla  
**Branch:** `ananthsai-work`

---

# 📖 Project Overview

This project focuses on preparing supply chain data for time-series analysis and understanding sales behavior through seasonal decomposition. The processed data will be used in later weeks for anomaly detection and demand forecasting.

---

# ✅ Week 1: Time-Series Data Preparation

## Objective

Prepare the retail inventory dataset for time-series analysis by creating a clean, continuous, and structured dataset.

---

## Tasks Completed

### 1. Dataset Loading
- Loaded the `retail_store_inventory.csv` dataset using Pandas.
- Verified dataset structure and column information.

### 2. Data Inspection
- Examined:
  - Dataset shape
  - Column names
  - Data types
  - Missing values
  - Summary statistics

### 3. Date Conversion
- Converted the `Date` column into Pandas DateTime format.

```python
df["Date"] = pd.to_datetime(df["Date"])
```

### 4. Set Date as Index

Created a DatetimeIndex for time-series operations.

```python
df = df.set_index("Date")
```

### 5. Chronological Sorting

Sorted records in ascending date order.

```python
df = df.sort_index()
```

### 6. Daily Aggregation

Aggregated numeric columns by date.

```python
daily_df = df.groupby(df.index).mean()
```

### 7. Missing Date Detection

Generated a complete daily date range and identified missing dates.

```python
full_range = pd.date_range(
    daily_df.index.min(),
    daily_df.index.max(),
    freq="D"
)
```

### 8. Reindexing

Created a continuous daily timeline.

```python
daily_df = daily_df.reindex(full_range)
```

### 9. Missing Value Treatment

Applied time-based interpolation to numeric columns.

```python
daily_df.interpolate(method="time")
```

### 10. Validation

Verified:

- No missing dates
- Correct DatetimeIndex
- Chronological order
- Missing values handled

### 11. Export

Saved the cleaned dataset.

```
cleaned_supply_chain_dataset.csv
```

---

# 📁 Week 1 Deliverables

- Week1_Data_Preprocessing.ipynb
- cleaned_supply_chain_dataset.csv
- README.md

---

# 📊 Week 2: Time-Series Decomposition

## Objective

Analyze the cleaned time-series data by decomposing it into:

- Trend
- Seasonal Component
- Residual Component

using the Statsmodels library.

---

## Tasks Completed

### 1. Loaded Cleaned Dataset

Imported the cleaned dataset from Week 1.

```python
pd.read_csv("cleaned_supply_chain_dataset.csv")
```

---

### 2. Prepared Time Series

- Converted Date to Datetime
- Set Date as Index
- Selected the target variable
- Checked missing values

---

### 3. Seasonal Decomposition

Performed additive decomposition.

```python
from statsmodels.tsa.seasonal import seasonal_decompose

result = seasonal_decompose(
    ts,
    model="additive",
    period=7
)
```

---

### 4. Extracted Components

Generated:

- Trend
- Seasonal
- Residual

---

### 5. Visualization

Created:

- Full decomposition plot
- Trend plot
- Seasonal plot

---

### 6. Exported Results

Saved:

```
trend_component.csv
seasonal_component.csv
residual_component.csv
```

Saved figures:

```
trend_plot.png
seasonal_plot.png
decomposition_full.png
```

---

# 📁 Week 2 Deliverables

- Decomposition_Notebook.ipynb
- decomposition_full.png
- trend_plot.png
- seasonal_plot.png
- trend_component.csv
- seasonal_component.csv
- residual_component.csv

---

# 📚 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Jupyter Notebook

---

# 📈 Results

### Week 1

✔ Converted Date column to DateTime

✔ Created DatetimeIndex

✔ Sorted records chronologically

✔ Identified missing dates

✔ Interpolated missing observations

✔ Generated cleaned time-series dataset

---

### Week 2

✔ Performed Seasonal Decomposition

✔ Extracted Trend Component

✔ Extracted Seasonal Component

✔ Extracted Residual Component

✔ Generated visualization plots

✔ Exported decomposition outputs

---

# 📂 Project Structure

```
Project-2/
│
├── Week1_Data_Preprocessing.ipynb
├── Decomposition_Notebook.ipynb
├── retail_store_inventory.csv
├── cleaned_supply_chain_dataset.csv
│
├── trend_component.csv
├── seasonal_component.csv
├── residual_component.csv
│
├── trend_plot.png
├── seasonal_plot.png
├── decomposition_full.png
│
└── README.md
```

---

# 🚀 Future Work

Week 3 will focus on:

- Statistical Anomaly Detection
- Demand Forecasting
- Moving Average
- ARIMA
- Prophet Forecasting
- Forecast Evaluation
- Dashboard Development

---

## Author

**Ananthsairam Goundla**

**Project:** Supply Chain Analytics

**Week 1 & Week 2 Contribution**
- Set Date as DataFrame index
- Sorted records chronologically
- Aggregated daily observations
- Generated continuous daily timeline
- Checked for missing dates
- Applied time-based interpolation
- Validated cleaned dataset
- Exported cleaned dataset

## Deliverables

- Week1_Data_Preprocessing.ipynb
- cleaned_supply_chain_dataset.csv

## Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook

## Outcome

The cleaned dataset is ready for anomaly detection, seasonal decomposition, and demand forecasting using ARIMA and Prophet.
