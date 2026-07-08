# Data Dictionary

## Dataset Overview

This dataset contains retail inventory and sales information across multiple stores, products, and regions. It is designed for supply chain analytics, demand forecasting, inventory management, and anomaly detection.

| Column Name        | Data Type | Description                                                                   | Example                        |
| ------------------ | --------- | ----------------------------------------------------------------------------- | ------------------------------ |
| Date               | Date      | Date on which the inventory and sales record was captured                     | 2022-01-01                     |
| Store ID           | String    | Unique identifier assigned to each retail store                               | S001                           |
| Product ID         | String    | Unique identifier assigned to each product                                    | P0001                          |
| Category           | String    | Product category to which the item belongs                                    | Groceries, Electronics, Toys   |
| Region             | String    | Geographic region where the store operates                                    | North, South, East, West       |
| Inventory Level    | Integer   | Number of units currently available in stock                                  | 231                            |
| Units Sold         | Integer   | Number of units sold during the period                                        | 127                            |
| Units Ordered      | Integer   | Number of units ordered for inventory replenishment                           | 55                             |
| Demand Forecast    | Float     | Predicted customer demand generated using forecasting methods                 | 135.47                         |
| Price              | Float     | Selling price of the product                                                  | 33.50                          |
| Discount           | Integer   | Percentage discount offered on the product                                    | 20                             |
| Weather Condition  | String    | Weather conditions that may influence customer demand                         | Sunny, Rainy, Cloudy           |
| Holiday/Promotion  | Integer   | Indicates whether a holiday or promotional event was active (0 = No, 1 = Yes) | 0, 1                           |
| Competitor Pricing | Float     | Price of similar products offered by competitors                              | 29.69                          |
| Seasonality        | String    | Seasonal period associated with the product demand pattern                    | Summer, Autumn, Winter, Spring |

## Business Importance of Key Fields

### Inventory Level

Represents the available stock at a store. Low inventory may lead to stockouts, while excessive inventory can increase storage costs.

### Units Sold

Represents actual sales and is a key measure of product performance.

### Units Ordered

Represents replenishment activity and helps track inventory management decisions.

### Demand Forecast

Represents expected future demand and is the primary target variable for forecasting models.

### Holiday/Promotion

Helps analyze the impact of marketing campaigns and special events on sales.

### Weather Condition

Allows analysis of external factors that may influence customer purchasing behavior.

### Seasonality

Helps identify recurring demand patterns throughout the year.
