# Sales Data Analysis Project

## Overview
This project analyzes 12 months of sales data from multiple CSV files to extract meaningful business insights. The analysis covers sales trends by month, city, hour of the day, product combinations frequently sold together, and product popularity. The goal is to uncover actionable insights that can help optimize marketing strategies, inventory management, and overall sales performance.

## Project Structure
- **Data Loading and Merging:** Merging sales data from 12 monthly CSV files into a single DataFrame for analysis.
- **Data Cleaning:** Handling missing values, filtering invalid rows, and correcting erroneous data entries.
- **Feature Engineering:** Adding new columns such as `Month`, `Sales`, `City`, and `Hour` for better segmentation.
- **Analysis Tasks:**
  1. Identifying the best month for sales and total revenue earned.
  2. Determining which city generated the highest sales.
  3. Analyzing peak sales hours to optimize advertisement timing.
  4. Discovering the most common product pairs sold together.
  5. Investigating the most sold product and possible reasons behind its popularity.

## Libraries Used
- pandas
- regex
- matplotlib
- collections (Counter)
- itertools (combinations)

## Key Findings
- **Best Month for Sales:** [Insert Month], with total sales of $[Insert Amount].
- **Top Sales City:** San Francisco CA generated the highest sales revenue.
- **Peak Sales Hours:** Sales peaked between [Insert Hour Range], suggesting optimal advertisement times.
- **Most Common Product Pairs:** 'iPhone' and 'Lightning Charging Cable' were the most frequently sold together.
- **Top Selling Product:** [Insert Product Name], likely due to its affordability/popularity/necessity.

## How to Run
1. Mount Google Drive (if using Colab) and set the working directory to the sales data folder.
2. Run the Python script cells sequentially to load, clean, and analyze the data.
3. Visualizations will be generated inline using matplotlib.
4. Modify paths or filenames as necessary based on your file locations.

## Future Improvements
- Enhance data validation to catch more irregularities.
- Incorporate more granular time-based analysis (e.g., day of week).
- Use advanced association rule mining (e.g., Apriori algorithm) for product bundling.
- Deploy dashboards for real-time insights and automated reporting.
