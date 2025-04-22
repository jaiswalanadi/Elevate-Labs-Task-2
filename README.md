# Elevate-Labs-Task-2

The dataset (sales_data_cleaned.csv) contains detailed sales information with fields like ordernumber, quantityordered, priceeach, sales, orderdate, productline, customername, country, dealsize, and more. Below is a step-by-step plan to analyze the data and create insightful visualizations:

Data Schema and Cleaning:
Fields: Numeric (quantityordered, priceeach, sales, msrp, etc.), categorical (productline, dealsize, customername, country, status), and temporal (orderdate, year_id, month_id, qtr_id).
Cleaning: Use PapaParse to parse CSV, skip empty lines, trim headers/values, and convert fields to appropriate types (e.g., sales to number, orderdate to Date using chrono.parseDate).
Validation: Check for invalid types (e.g., null, NaN) in numeric fields and handle missing or malformed dates.
Key Insights to Explore:
Sales Performance by Product Line: Which product lines (e.g., Classic Cars, Motorcycles) drive the most revenue? Use a bar chart to compare total sales.
Customer Contribution: Identify top customers by sales volume. A treemap will highlight key contributors.
Sales Trend Over Time: Analyze sales trends by year or quarter to identify growth patterns. A line chart will show temporal trends.
Deal Size Distribution: Understand the proportion of Small, Medium, and Large deals. A pie chart (with ≤7 categories) will suffice.
Geographic Sales Distribution: Compare sales by country or territory. A bar chart will show regional performance.
Interesting Fact: Investigate if certain product lines have unusually high priceeach compared to msrp, indicating premium pricing or discounts.
Visualization Choices:
Bar Chart (Sales by Product Line): Aggregates sales by productline, sorted by total sales.
Treemap (Top Customers): Displays customername by total sales, with size and color encoding sales volume.
Line Chart (Sales Trend): Plots sales by year_id or qtr_id, with a brush for zooming into specific periods.
Pie Chart (Deal Size): Shows proportion of dealsize categories, avoiding clutter with clear labels.
Bar Chart (Sales by Country): Aggregates sales by country, highlighting top markets.
Recharts Components:
Use Recharts.BarChart for product line and country sales.
Use Recharts.Treemap for customer contribution.
Use Recharts.LineChart with Recharts.Brush for sales trends.
Use Recharts.PieChart for deal size distribution.
Wrap all charts in Recharts.ResponsiveContainer for responsive design.
Design Principles:
Avoid Clutter: Limit to 5 visualizations, use consistent color schemes (e.g., Tailwind’s blue and green shades).
Highlight Takeaways: Add tooltips and labels to emphasize key data points (e.g., top customer, peak sales year).
Context: Include chart titles, axis labels, and a summary section explaining insights.
Business Insights: Focus on actionable findings, e.g., “Classic Cars dominate sales, suggesting inventory prioritization.”
Summary Slide: Create a header section summarizing key findings and an interesting fact.
Data Processing:
Aggregate data for each visualization (e.g., sum sales by productline, group by year_id).
Handle large datasets by sampling or binning if needed (though this dataset is small, ~300 rows).
Use loadFileData("sales_data_cleaned.csv") to load CSV at runtime.
