# HR Analytics Dashboard

A comprehensive Power BI dashboard designed to provide insights into key HR metrics, including attrition rates, department-wise male-to-female ratios, and yearly hiring trends. This dashboard uses CSV data sources, advanced data modeling, and DAX functions to deliver actionable insights.

---

## Features

- **Attrition Analysis**: Visualizes attrition rates over time to identify trends and patterns.
- **Gender Ratio Insights**: Department-wise breakdown of male-to-female ratios for workforce diversity analysis.
- **Hiring Trends**: Tracks yearly new hires to monitor recruitment progress.
- **Interactive Visualizations**: Enables users to drill down and filter data for detailed analysis.

---

## Data Sources

The dashboard uses the following CSV data sources:

1. **Employee Data**:
   - Fields: `Employee ID`, `Department`, `Gender`, `Hire Date`, `Exit Date`
2. **Department Data**:
   - Fields: `Department ID`, `Department Name`
3. **Hiring Data**:
   - Fields: `Year`, `New Hires`

---

## Tools and Technologies

- **Power BI**:
  - Used for creating interactive dashboards and visualizations.
- **Data Modeling**:
  - Establishes relationships between data tables for efficient querying.
- **DAX Functions**:
  - Calculates metrics like attrition rates, gender ratios, and yearly hiring trends.

---

## Key Metrics

1. **Attrition Rate**:
   - Formula: `(Number of Employees Who Left / Average Total Employees) * 100`
   - DAX Example: `AttritionRate = DIVIDE(COUNTROWS(Exits), AVERAGE(TotalEmployees), 0)`

2. **Male-to-Female Ratio**:
   - Visualizes gender distribution within each department.
   - DAX Example: `GenderRatio = COUNTAX(FILTER(Employees, Employees[Gender] = "Male"), 1) / COUNTAX(Employees, 1)`

3. **Yearly New Hires**:
   - Tracks hiring trends across years.
   - DAX Example: `NewHires = SUM(HiringData[New Hires])`

---

## Dashboard Insights

- **Attrition Trends**: Identify peak attrition periods and potential causes.
- **Gender Diversity**: Ensure balanced representation across departments.
- **Recruitment Analysis**: Monitor and optimize hiring strategies.

---

## Setup Instructions

1. **Data Preparation**:
   - Ensure CSV files are clean and formatted as per the required structure.

2. **Load Data**:
   - Import the CSV files into Power BI.

3. **Data Modeling**:
   - Create relationships between `Employee Data`, `Department Data`, and `Hiring Data`.

4. **Build Visualizations**:
   - Use Power BI charts, slicers, and tables for interactive insights.

5. **Apply DAX Calculations**:
   - Add measures for attrition rates, gender ratios, and yearly hiring trends.

---

## How to Use

- Open the Power BI file (`HR_Analytics.pbix`).
- Use filters and slicers to explore data interactively.
- Analyze metrics across time periods, departments, and other dimensions.

---

## Contribution

Contributions are welcome! Feel free to:
- Suggest additional metrics or features.
- Report bugs or data inconsistencies.
- Submit pull requests to enhance the dashboard.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- HR professionals and analysts for their insights into critical HR metrics.
- Power BI and its rich ecosystem for enabling advanced analytics and visualization.
