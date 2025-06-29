# Sales Data Analysis Project

This project is a comprehensive data analysis of a retail store's sales performance across multiple U.S. cities over a year. It uses **Python (Pandas, Matplotlib)** to clean, process, and explore sales data to answer key business questions.

---

## Dataset

Sales data from various months in 2019, stored in individual CSV files under the `Sales_Data` directory.

### Columns:
- `Order ID`
- `Product`
- `Quantity Ordered`
- `Price Each`
- `Order Date`
- `Purchase Address`

---

## Tools Used

- Python 3.x
- pandas
- matplotlib
- os
- collections
- itertools

---

## Data Cleaning Steps

1. **Merged all monthly CSVs** into a single DataFrame.
2. **Dropped NaN rows** and handled bad headers.
3. Converted data types for:
   - `Quantity Ordered` → `int`
   - `Price Each` → `float`
4. Extracted new columns:
   - `Month` and `Hour` from `Order Date`
   - `City` from `Purchase Address`
5. Calculated additional columns:
   - `Sales = Quantity Ordered * Price Each`

---

## Analysis Performed

### 1. Best Month for Sales
Identified total sales by month to determine peak seasonality.

### 2. Top Performing Cities
Grouped data by `City` to visualize regions with highest revenue.

### 3. Best Time to Advertise
Extracted `Hour` from order time to suggest optimal ad display times.

### 4. Frequently Sold Together Products
Used `Order ID` duplicates and combinations to find top product bundles.

### 5. Best Selling Products
Grouped by `Product` and analyzed quantity and price relationships.

---

## Example Visualizations

- **Bar Chart**: Monthly sales trends
- **Bar Chart**: Sales by city
- **Line Plot**: Order frequency by hour
- **Text Output**: Top product combinations sold together

---
