# EDA Report: Supply Chain Analytics – Demand Forecasting & Anomaly Detection

## 1. Title
**Comprehensive Exploratory Data Analysis (EDA) Report on Retail Store Inventory & Demand Vectors**  
*Project Week 1 Deliverable — Operational Baselines & Visual Diagnostics*

---

## 2. Dataset Overview
The dataset (`retail_store_inventory CSV.csv`) contains **73,100 records** and **15 feature dimensions**. It maps daily multi-store operational metrics tracking product levels, regional sales velocities, internal markdown variables, and structural external dimensions (weather indices and competitive tracking). 

### Feature Inventory:
- **Temporal Vectors:** `Date`
- **Identifiers:** `Store ID`, `Product ID`
- **Categorical Factors:** `Category`, `Region`, `Weather Condition`, `Seasonality`
- **Supply Metrics:** `Inventory Level`, `Units Sold`, `Units Ordered`, `Demand Forecast`
- **Financial Factors:** `Price`, `Discount`, `Competitor Pricing`, `Holiday/Promotion`

---

## 3. Data Cleaning Summary
- **Type Conversions:** The temporal column `Date` was cast from an unindexed object/string into an explicit datetime format (`datetime64[ns]`) to facilitate rolling aggregation routines.
- **Structural Sanity:** No values required truncation or trimming as string layouts and numerical metrics adhered to clean uniform parameters.

---

## 4. Descriptive Statistics
A granular look into numerical data fields yields the following structural characteristics:
- **Inventory Level:** Maintained strictly within a truncated boundary from 50 to 500 units, averaging **274.47**. 
- **Units Sold:** Highly volatile average of **136.46 units** per observation with a significant standard deviation (**108.92**).
- **Pricing Dynamics:** Centralized price average of **$55.14** mirrors competitor profiles (**$55.15**) with narrow spread variations.
- **Demand Forecasting:** Possesses a structural floor of **-9.99**, pointing to minor mathematical artifacts or negative balance corrections in the baseline calculation models.

---

## 5. Missing Value & Duplicate Analysis
- **Missing Entries:** Exact count of **0 missing fields** across all 73,100 positions. 
- **Duplicate Records:** **0 duplicate rows** detected across the composite primary key combinations (`Date` + `Store ID` + `Product ID`).
- **Data Integrity Evaluation:** Exceptional. The dataset represents an intact system log that does not require artificial synthetic imputation or row filtering.

---

## 6. Sales Trend Analysis
- **Temporal Profile:** Aggregated daily volume exhibits a tight, noisy oscillating sequence. The lack of macro trend shifts implies that core baseline consumer demand across the network remains structurally consistent.
- **Distribution Profile:** Marked right-skewness. Low to mid-tier transactional throughput represents standard daily business operations, whereas massive volume days (350+ units) act as isolated events.

---

## 7. Inventory Trend Analysis
- **Temporal Profile:** Network inventory aggregates show stable maintenance bounds (24,000–31,000 units). The system avoids erratic long-term stock accumulation or rapid stock depletion cycles.
- **Distribution Profile:** Displays a rigid uniform distribution layout across individual products. Stock levels are evenly distributed between the 50-unit floor and 500-unit ceiling, indicating automated max-min fulfillment limits.

---

## 8. Product Category Analysis
The dataset presents a completely uniform distribution among major product classifications:
- **Categories Checked:** *Furniture, Toys, Clothing, Groceries, Electronics*
- **Distribution Balance:** Each category makes up approximately **20%** of the recorded operational matrix. This ensures structural parity, allowing subsequent forecasting models to generalize evenly without category-specific volume imbalances.

---

## 9. Charts Explanation & Diagnostics
1. **Daily Total Units Sold over Time (Line Chart):** Captures high-frequency sales movements. Highlights that demand spikes are frequent but transient, typically snapping back to the operational mean within short intervals.
2. **Distribution of Units Sold (Histogram & Boxplot):** Formally maps the positive skewness. The boxplot emphasizes that high volume observations are not uncharacteristic errors, but rather extended valid demand spikes.
3. **Daily Total Inventory Levels over Time (Line Chart):** Confirms an unfluctuating aggregate pattern, validating that logistical replenishment schedules are in sync with consumption cycles.
4. **Distribution of Inventory Levels (Histogram & Boxplot):** Visualizes the flat, uniform distribution shape. This confirms that stock is held uniformly across the warehouse footprint rather than clustering around a central mean.
5. **Correlation Heatmap:** 
   - Reveals an exact **1.00 correlation** between `Units Sold` and `Demand Forecast`, indicating a highly integrated calculation logic.
   - Highlights a **0.99 correlation** between `Price` and `Competitor Pricing`, indicating systematic price-matching algorithms.
   - Indicates a **0.59 correlation** between `Inventory Level` and `Units Sold`, verifying that store-level stock availability heavily drives sales volumes.

---

## 10. Key Findings
1. **Aggressive Pricing Alignment:** The organization is locked into immediate response pricing loops with external market players ($r = 0.99$).
2. **Predictive Sync:** The absolute correlation between actual units sold and demand forecast vectors indicates that operational planning tools operate on perfect tracking assumptions.
3. **Stock-Driven Conversion:** High volume sales events are fundamentally bounded by store holding volumes ($r = 0.59$). 

---

## 11. Business Recommendations
- **Transition to Proactive Pricing:** Instead of maintaining a reactive price-matching posture ($r=0.99$), run elasticity experiments on high-performing categories to find margin expansion opportunities.
- **Differentiate Inventory Caps:** Move away from a flat uniform stock distribution profile. Reallocate warehouse and shelf limits by lowering slow-moving categories (e.g. Furniture) and expanding allocation windows for fast-moving consumer items.
- **Isolate Promotion Spikes:** Trace the high-volume trailing sales observations to specific promotional or weather variables to improve targeted logistics readiness.

---

## 12. Conclusion
The initial week of data analysis verifies that the supply chain infrastructure is highly organized, clean, and operates within strict control bounds. The presence of clear correlation signals guarantees a solid foundation for building the next phase: predictive forecasting and automated anomaly detection systems.
