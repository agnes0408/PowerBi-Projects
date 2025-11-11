# 🛒 E-Commerce Sales Analysis (Power BI Project)

This Power BI project focuses on analyzing **e-commerce sales performance** using DAX and interactive data visualization techniques.  
It includes calculated columns, DAX measures, and insightful dashboards to explore trends, profitability, and performance metrics within the e-commerce domain.

---

## 🎯 Project Objectives

- Analyze e-commerce data to uncover sales, profit, and performance insights.  
- Build an interactive Power BI dashboard using data modeling and DAX.  
- Compare actual sales with sales targets to measure performance.  
- Visualize geographic, category-wise, and time-based sales trends.  

---

## 📊 Project Overview

**Project Name:** E-Commerce Sales Analysis  
**Tool Used:** Power BI Desktop  
**Data Source Files:**
- `List of Orders.csv`
- `Order Details.csv`
- `Sales Target.csv`

---

## 🧮 DAX & Data Modeling

### 🧱 Calculated Columns
1. **Category Type:** Combines the `Category` and `Sub-Category` columns into one field.  
   ```DAX
   Category Type = 'Order Details'[Category] & " - " & 'Order Details'[Sub-Category]


   Revenue per Order: Calculates total revenue for each order.

Revenue per Order = 'Order Details'[Amount] * 'Order Details'[Quantity]


Sales Category: Categorizes sales as “Above Average” or “Below Average” based on the amount.

Sales Category = 
IF(
    'Order Details'[Amount] > AVERAGE('Order Details'[Amount]),
    "Above Average",
    "Below Average"
)

📏 Calculated Measures

Total Order Count

Order Count = COUNTROWS('Order Details')


Average Profit (Delhi)

Avg Profit (Delhi) =
CALCULATE(
    AVERAGE('Order Details'[Profit]),
    'List of Orders'[City] = "Delhi"
)


Year-to-Date (YTD) Sales

YTD Sales = 
TOTALYTD(
    SUM('Order Details'[Revenue per Order]),
    'List of Orders'[Order Date]
)

📈 Visualizations Created
Visualization Type	Purpose
Clustered Column Chart	Compare actual sales vs. targets by category
Donut Chart	Display maximum profit margin by sub-category
Line Chart	Show monthly sales trend over time
Scatter Chart	Compare profit vs. quantity by sub-category
Cards & Multi-Row Cards	Display total sales, targets, and minimum target per segment
Matrix View	Analyze sales vs. targets across categories and months
Map Visual	Display total sales geographically by city
Treemap	Show sales distribution by sub-category
Funnel Chart	Visualize order count by state
🌍 Geographic & Trend Analysis

Mapped sales performance by city to identify high-demand regions.

Visualized monthly sales growth and target achievements.

Compared profitability vs. quantity to understand product performance.

📸 Dashboard Preview

(Add screenshots inside a folder named /screenshots and link them below)






⚙️ Tools & Technologies Used

Power BI Desktop

DAX (Data Analysis Expressions)

Data Modeling & Relationships

Data Cleaning and Transformation

CSV Data Sources

🔍 Key Insights & Learnings

Identified top-performing categories and sub-categories driving revenue.

Pinpointed regions underperforming against targets.

Observed monthly trends and growth opportunities using YTD sales analysis.

Created KPI cards for quick business decision-making.

📘 Conclusion

This Power BI project demonstrates:

End-to-end data modeling and DAX calculations

Creation of interactive dashboards for actionable business insights

Application of data visualization best practices in a real-world scenario

📂 Repository Structure
E-Commerce-Sales-Analysis-PowerBI/
│
├── E-Commerce_Sales_Analysis.pbix             # Main Power BI dashboard
│
├── datasets/                                  # Source data files
│   ├── List of Orders.csv
│   ├── Order Details.csv
│   ├── Sales target.csv
│
├── screenshots/                               # Dashboard images
│   ├── dashboard_overview.png
│   ├── sales_target_chart.png
│   ├── geographic_sales_map.png
│
└── README.md                                  # Documentation

Author

Name: Agnes
Role: Data Analyst | Business Analyst | Power BI Developer
Location: Chennai / Coimbatore, India
Skills: Power BI | DAX | SQL | Python | Excel | Data Visualization
