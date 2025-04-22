# Elevate-Labs-Task-2

📘 In Tableau
1. Sales Trend
Rows: SUM(sales)

Columns: orderdate (converted to MONTH)

Chart Type: Line

Add Trend Line (Analytics Pane) for insights

2. Product Line Sales
Rows: productline

Columns: SUM(sales)

Chart: Bar

Sort descending by sales

3. Top 10 Customers
Filter Top N: customername by SUM(sales)

Chart: Bar (Horizontal)

4. Territory Map (Optional)
Use Country or Territory for a Map if latitude/longitude is available.

Or use Bar Chart with territory vs SUM(sales)

5. Deal Size Distribution
Chart: Pie / Donut

Label: Deal Size

Size: Count of records or total sales

6. Monthly Sales by Year
Columns: month_id

Rows: SUM(sales)

Color: year_id

Chart Type: Line or Area chart

📘 In Power BI
Use Line & Clustered Column, Stacked Bar, Pie, and Map visuals.

Use Date Hierarchies for orderdate.

Apply slicers (filters) for productline, territory, or year to create an interactive dashboard.

Add a Summary Card showing:

Total Sales

Number of Customers

Avg Deal Size
