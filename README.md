# 📊 Sales Analytics Power BI Dashboard

This Power BI report provides an end-to-end Sales Analytics solution built using multiple related datasets including Sales, Customers, Products, Categories, Territories, and Returns.  
The objective of this dashboard is to analyze sales performance, customer distribution, product contribution, return trends, and geographical insights in a dynamic and interactive format.

---

## 🎯 Project Objectives

- Track total sales and order performance over time
- Identify top-performing products and categories
- Understand customer demographics and purchasing behavior
- Analyze regional sales distribution using map visuals
- Monitor returns and determine return percentage trends
- Provide decision-makers with interactive filters and drill-down insights

---

## 🧱 Data Model Overview

The data model follows a **Star Schema** for optimized performance.

| Table Name | Type | Key Purpose |
|-----------|------|-------------|
| `FinalSales` | Fact | Contains core sales records (Order Date, CustomerKey, ProductKey, Sales Amount, Quantity, etc.) |
| `Returns` | Fact | Tracks product returns and return quantity |
| `Customers Table` | Dimension | Customer profile details (Name, Gender, Email, Income Level, etc.) |
| `Products` | Dimension | Product details (Product Name, Color, Model, Cost, Size, etc.) |
| `Product Subcategories` | Dimension | Sub-categorization of products |
| `Product Categories` | Dimension | Higher level product grouping |
| `Territories` | Dimension | Region and country mapping |
| `Datetable` | Dimension | Calendar table for time intelligence |

**Relationships:**  
- `FinalSales` linked to `Customers`, `Products`, `Territories`, and `Datetable` via surrogate keys  
- Category hierarchy: **Product Categories → Product Subcategories → Products**

This model ensures efficient slicing and drill-down analysis.

---

## 📌 Key KPIs Displayed

| KPI | Description |
|----|-------------|
| **Total Sales** | Total revenue generated |
| **Count of Orders** | Total number of transactions |
| **Sum of Returns** | Overall returned quantity |
| **Return %** | (Return Quantity ÷ Total Quantity) × 100 |
| **Top Customer Sales Ranking** | Customer leaderboard based on sales contribution |

---

## 🖥 Dashboard Pages Overview

### **1️⃣ Overview Page**
This is the primary dashboard summarizing the business performance.

- **KPIs** section shows Total Sales, Orders, and Return %
- **Filters**: Region, Category, Gender, Quarter, Email Address
- **Sales by Sub-Category (Income Based)** – Stacked bar chart grouped by customer income level
- **Sales by Country (Map Visual)** – Helps understand geographical markets
- **Top Customers Table** – List of highest-value customers ranked by revenue
- **Sales Trend Over Time** – Line chart with slicer for *Adjustable Price* to simulate price sensitivity
- **Monthly KPI Cards** – Targets vs Achieved for one selected time period (Dec 2017 shown in example)

---

### **2️⃣ Product Details Page**
- Deep-dive into product performance
- Sales comparison across product categories and subcategories
- Product-wise contribution and order count visualizations
- Helps identify **best-selling and low-performing items**

---

### **3️⃣ Tooltip Pages**
Report tooltips are used so when the user hovers over:
- Product points on charts
- Customer names in tables

they get quick mini insights like:
- Product Name, Category, Total Sales, Return %
- Customer Demographics & Loyalty Value

This improves **context without switching tabs**.

---

### **4️⃣ Drillthrough Pages**
Drillthrough allows users to right-click and *zoom into details*.

Examples:
- **Customer Drillthrough** → Shows complete profile + all purchases of the selected customer.
- **Product Drillthrough** → Shows trend, return ratio, and region-wise distribution for the selected product.

This supports **root cause analysis** and decision making.

---

## 🧠 Key Insights Derived

- **Mountain Bikes** have the highest sales volume, driven mainly by customers with medium income.
- **Road Bikes** show strong demand in **North America**, but returns were slightly higher in Q3.
- **Europe** shows lower total order counts but **higher average order value**, indicating premium buyers.
- Some accessories like **Gloves and Shorts** have minimal sales impact → recommended for bundling or promotional campaigns.
- Return rate ~**7.26%**, suggesting potential improvement in quality or replacement policy.

---

## 🛠 Technologies & Skills Used

| Tool/Skill | Application |
|----------|-------------|
| **Power BI Desktop** | Data modeling & visualization |
| **DAX Measures** | KPI calculations, return % logic, time intelligence |
| **Data Cleaning & Transformation** | Using Power Query |
| **Star Schema Modeling** | Optimized relationships |
| **Drillthrough & Tooltips** | User experience enhancements |

---

## 🚀 How to Use the Report
1. Download the `.pbix` file from this repository.
2. Open using **Power BI Desktop**.
3. Ensure Data Model relationships remain the same.
4. Use top slicers to interact and analyze different business segments.

---

## 📩 Contact / Collaboration

If you would like to discuss this dashboard or need guidance on Power BI dashboards:

**Created by:** *Saloni Shrigoud*  
**LinkedIn:** *https://linkedin.com/in/saloni-shrigoud-2bb082153*  
**Email:** *shrigoudsaloni@gmail.com*

