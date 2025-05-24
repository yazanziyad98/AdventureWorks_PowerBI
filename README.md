#📊 Adventure Works Dashboard

This project provides a visual analytics dashboard for **Adventure Works**, segmented into two major domains: **Internet Sales** and **Call Center**. The dashboards are built to facilitate business intelligence and decision-making by presenting key performance indicators and metrics in an interactive and accessible format.

---

### 🛒 Internet Sales Dashboard

![image](https://github.com/user-attachments/assets/e4472a2f-c89f-4176-8a02-f7f184b598a7)


### Key Metrics:

- **Total Sales**: $23.72M
- **Sales YTD**: 11M
- **Median Tax Amount**: $2.7992
- **Median Freight**: $0.8748
- **Number of Products**: 4

### Visual Insights:

- **Sales by Continent/Country**: Displays total sales grouped by region (Europe, North America, Pacific).
- **Top Products by Sales**: Bar chart of top-selling products.
- **Sales by Product Subcategory**: Highlights which subcategories (e.g., Road Bikes, Mountain Bikes) contribute most to revenue.
- **Sales by Currency**: Donut chart showing breakdown by currency (USD, AUD, GBP, Other).
- **Profit Over Time**: Line chart showing quarterly profit trends across years.

---

### 📞 Call Center Dashboard

 ![image](https://github.com/user-attachments/assets/075f66d5-3e86-445e-bfea-54615c481c8f)


### Key Metrics:

- **Total Calls**: 43K
- **Automatic Responses**: 30K
- **Issues Raised**: 162
- **Average Service Grade**: 0.10
- **Number of Call Centers**: 120

### Visual Insights:

- **Average Time per Issue by Shift**: Bar chart showing support performance by shift (AM, PM1, PM2, Midnight).
- **Call Volume by Shift**: Visualizes number of calls received during each shift.
- **Call Time Breakdown**: Donut chart showing weekday vs holiday call times.
- **Time vs Service Grade**: Scatter plot correlating average handling time with service grade.
- **Daily Call Volume**: Trend of calls received per day over a monthly period.

---

### 🛠️ Features

- Interactive filters: Year, Month, Product Category, Region (Internet Sales); Shift Time, Shift Day, Day of Month (Call Center)
- Cross-category drill-downs for detailed analysis
- Responsive and user-friendly layout

---

## 🧩 Data Model


The data model consists of a **star schema** structure with two main fact tables:

![image](https://github.com/user-attachments/assets/0c7a2e02-88f4-4a8c-be41-4908ed9388a8)

- **FactInternetSales** – Captures all e-commerce transaction details including sales amount, freight, tax, and date of purchase.
- **FactCallCenter** – Stores metrics related to call center operations such as number of calls, issues raised, automatic responses, and operator levels.

### 🔑 Key Relationships

- **DimProduct**, **DimProductSubcategory**, and **DimProductCategory** – These dimension tables provide hierarchical categorization for products used in internet sales.
- **DimCurrency** – Linked to FactInternetSales to track transactions across multiple currencies.
- **DimSalesTerritory** – Used for geographic segmentation of sales.
- **DimDate** – Shared by both fact tables to support temporal analysis by year, quarter, month, or day.
- **DimProduct ↔ DimProductSubcategory ↔ DimProductCategory** – Enables deep product-level analysis from broad categories to specific product names.



