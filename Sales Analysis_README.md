# Sales Analytics Dashboard

A dynamic Power BI dashboard to analyze and visualize sales data across multiple dimensions, providing actionable insights into sales performance, customer behavior, and product demand. This dashboard uses CSV data sources, advanced data modeling, and DAX functions to deliver key performance indicators (KPIs) and detailed analyses.

---

## Features

### Key Performance Indicators (KPIs):
- **Total Sales**: Aggregated sales amount.
- **Sales Order Count**: Total number of sales orders.
- **Customers**: Breakdown by demographics and purchasing patterns.
- **Products**: Product category-wise performance.
- **Countries**: Sales distribution across regions.

### Insights and Visualizations:
1. **Monthly and Calendar Year Sales Trends**:
   - Visualizes sales amounts at both monthly and yearly levels.
2. **Sales by Gender and Marital Status**:
   - Analyzes sales distribution based on customer demographics.
3. **Product Category and Territory-Wise Sales**:
   - Provides a detailed view of product performance by region.
4. **Customer Age Group Product Demand**:
   - Identifies popular products among different customer age groups.
5. **Sales by Customer Distance**:
   - Examines the impact of customer location on sales performance.

---

## Data Sources

The dashboard is built using the following CSV data sources:

1. **Sales Data**:
   - Fields: `Order ID`, `Customer ID`, `Product ID`, `Sales Amount`, `Order Date`, `Territory`, `Distance from Customer`
2. **Customer Data**:
   - Fields: `Customer ID`, `Gender`, `Age`, `Marital Status`, `Address`
3. **Product Data**:
   - Fields: `Product ID`, `Category`, `Sub-Category`, `Price`

---

## Tools and Technologies

- **Power BI**:
  - For creating interactive visualizations and dashboards.
- **Data Modeling**:
  - Establishes relationships between data tables for seamless analysis.
- **DAX Functions**:
  - Calculates custom metrics such as monthly sales trends, gender-based sales, and distance impact on sales.

---

## Key Metrics and DAX Examples

1. **Monthly Sales Amount**:
   - Formula: `SUM(Sales[Sales Amount])`
   - DAX Example: `MonthlySales = CALCULATE(SUM(Sales[Sales Amount]), MONTH(Sales[Order Date]))`

2. **Sales by Gender and Marital Status**:
   - DAX Example: `SalesByGender = SUMMARIZE(Sales, Customers[Gender], "TotalSales", SUM(Sales[Sales Amount]))`

3. **Product Category Sales**:
   - DAX Example: `CategorySales = SUMMARIZE(Products, Products[Category], "SalesAmount", SUM(Sales[Sales Amount]))`

4. **Customer Age Group Demand**:
   - DAX Example: `AgeGroupDemand = GROUPBY(Customers, Customers[Age Group], "Demand", SUM(Sales[Product Quantity]))`

5. **Sales by Customer Distance**:
   - DAX Example: `SalesByDistance = AVERAGE(Sales[Distance from Customer])`

---

## Dashboard Insights

- **Sales Trends**: Identify growth patterns and seasonal trends in sales.
- **Demographic Analysis**: Understand how gender, marital status, and age influence purchasing behavior.
- **Product Performance**: Evaluate top-performing categories and their regional success.
- **Customer Proximity Analysis**: Assess the impact of distance on sales efficiency.

---

## Setup Instructions

1. **Prepare the Data**:
   - Ensure all CSV files are clean and structured correctly. (At my end i am using data wrangling technique to clean data).

2. **Load Data into Power BI**:
   - Import `Sales Data`, `Customer Data`, and `Product Data`.

3. **Data Modeling**:
   - Establish relationships between `Customer ID`, `Product ID`, and `Order ID` tables.

4. **Create Measures and Calculations**:
   - Use DAX functions to calculate metrics such as sales trends, product demand, and demographic analysis.

5. **Build Visualizations**:
   - Design interactive charts, tables, and slicers for deeper insights.

---

## Contribution

Contributions are welcome! You can:
- Report issues or bugs.
- Suggest new metrics or features.
- Submit pull requests to improve the dashboard.

---


## Acknowledgments

- Sales professionals for providing insights into critical sales KPIs.
- Power BI for enabling advanced analytics and rich visualizations.
