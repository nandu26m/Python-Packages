# Sales Data Analysis Project

This project is a comprehensive data analysis of a retail store's sales performance across multiple U.S. cities over a year. It uses **Python (Pandas, Matplotlib)** to clean, process, and explore sales data to answer key business questions.

---

## Dataset

Sales data from various months in 2019, stored in individual CSV files under the `Sales_Data` directory.

---

## Tools Used

- Python 3.x
- pandas
- matplotlib
- regex
- collections (Counter)
- itertools (combinations)

---

## Data Cleaning Steps

1. **Merged all monthly CSVs** into a single DataFrame.
2. **Dropped NaN rows** and handled bad headers.
3. Removed rows with invalid data (e.g., incorrect order times).
4. Added new columns such as `Month`, `Sales` (quantity × price), `City`, and `Hour` extracted from order timestamps.

---

## Analysis Performed

### 1. Best Month for Sales
Identified total sales by month to determine peak seasonality.

### 2. Top Performing Cities
Grouped data by `City` to visualize regions with highest revenue.

### 3. Best Time to Advertise
Extracted `Hour` from order time to suggest optimal ad display times.

### 4. Frequently Sold Together Products
Used duplicate `Order ID`s and product combinations to find top product bundles.

### 5. Best Selling Products
Grouped by `Product` and analyzed quantity and price relationships.

---

## Example Visualizations

- **Bar Chart**: Monthly sales trends
- **Bar Chart**: Sales by city
- **Line Chart**: Sales volume by hour of day
- **Network Graph** (optional): Common product pairings

---

## Key Findings

- **Best Month for Sales:** [Insert Month], with total sales of $[Insert Amount].
- **Top Sales City:** San Francisco CA generated the highest sales revenue.
- **Peak Sales Hours:** Sales peaked between [Insert Hour Range], suggesting optimal advertisement times.
- **Most Common Product Pairs:** 'iPhone' and 'Lightning Charging Cable' were the most frequently sold together.
- **Top Selling Product:** [Insert Product Name], likely due to its affordability/popularity/necessity.

---

## How to Run

1. Place all monthly sales CSV files inside the `Sales_Data` directory.
2. Run the Python script/notebook sequentially to load, clean, and analyze the data.
3. Visualizations will be generated inline using matplotlib.
4. Adjust file paths if your directory structure differs.

---

## Future Improvements

- Enhance data validation to catch more irregularities.
- Incorporate more granular time-based analysis (e.g., day of week).
- Use advanced association rule mining (e.g., Apriori algorithm) for product bundling.
- Deploy dashboards for real-time insights and automated reporting.
