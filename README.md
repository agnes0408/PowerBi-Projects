# 🛒 E-Commerce Sales Analysis | Power BI Project

### 📌 Objective
This project demonstrates **data transformation, modeling, and analysis** of e-commerce sales data using Power BI.  
It was developed as part of a **Data Analytics course assignment** to explore real-world business intelligence workflows.

---

## 📂 Datasets Used
- **List of Orders.csv** — Contains overall order information such as customer, location, and order dates.  
- **Order Details.csv** — Includes product-level details, profit, and sales amounts.  
- **Sales Target.csv** — Holds monthly or category-level sales targets.

---

## 🧠 Key Tasks Performed

### 🔹 Data Import & Transformation
- Imported all CSV files into **Power Query Editor**.  
- Restricted the *List of Orders* table to the first 500 rows.  
- Converted data types:
  - *Order Date* → Date  
  - *Amount* and *Target* → Fixed Decimal Number  
- Applied text formatting:
  - *Customer Name* → Proper case  
  - Merged *State* and *City* columns into a new **Location** column (`City, State`).
- Created calculated columns:
  - **Profit Margin** = Profit / Amount  
  - **Profit Status**:
    - Profit < 0 → Loss  
    - Profit = 0 → Break-Even  
    - Profit > 0 → Profit  

---

### 🔹 Data Cleaning
- Identified and handled missing values and duplicates.  
- Standardized field names for consistency.  

---

### 🔹 Data Merging & Relationships
- Merged *List of Orders* and *Order Details* using **Order ID** → created `Orders Data`.  
- Established relationships:
  - *List of Orders* ↔ *Order Details* via **Order ID**  
  - *Order Details* ↔ *Sales Target* via **Category**  

---

### 🔹 Sorting, Filtering & Aggregation
- Sorted data by *Order Date (descending)* to view recent sales trends.  
- Filtered data by *State = Tamil Nadu* for regional insights.  
- Grouped data to:
  - Count of Order IDs per Category  
  - Average Profit by Category  
  - Total Amount by Sub-Category  
  - Total Target Amount by Month  

---

## 📊 Dashboard Insights
- Overall sales trends by region and category.  
- Profit margin distribution across states.  
- Comparison between **sales vs. targets** by month.  
- Top-performing subcategories and customer segments.  

---

## 🧩 Tools & Technologies
- **Power BI**
- **Power Query**
- **Data Modeling**
- **DAX (for calculated columns)**
- **CSV Data Sources**

---

## 🚀 How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/E-Commerce-Sales-Analysis-PowerBI.git
