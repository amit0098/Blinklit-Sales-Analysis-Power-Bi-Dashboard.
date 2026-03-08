# 🛒 Blinkit Sales Analysis Dashboard

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white" />
  <img src="https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />
</p>

---

## 📌 Project Overview

The **Blinkit Sales Analysis Dashboard** is an interactive Power BI report built to analyze and visualize sales performance across multiple dimensions — product categories, outlet types, locations, and time periods.

This project empowers stakeholders with data-driven insights to:
- Monitor key sales KPIs at a glance
- Identify top-performing and underperforming categories
- Understand customer ratings and preferences
- Make informed strategic decisions

---

## 🖥️ Dashboard Preview

> *Power BI dashboard with interactive filters across all KPIs, charts, and slicers.*

![Dashboard Preview](https://github.com/user-attachments/assets/2bb44b34-c6cd-43e4-a70f-6bf70e2ab8bf)

---

## 📊 Key KPIs

| Metric | Value |
|--------|-------|
| 💰 Total Sales | **$1.20M** |
| 📦 Total Items Sold | **8,523** |
| ⭐ Average Rating | **~3.92 / 5** |
| 🏪 Top Outlet Size by Sales | **Medium ($507.9K)** |
| 🥇 Top Category by Sales | **Fruits & Vegetables ($178.12K)** |
| 📉 Lowest Category by Sales | **Seafood ($9.08K)** |

---

## 🔍 Key Insights

### 🏪 Sales by Outlet Size
- **Medium outlets** drive the most revenue at **$507.9K**
- High-size outlets surprisingly record the lowest sales at **$248.99K**

### 🥗 Fat Content Analysis
- **Low Fat** items dominate sales: **$776.32K**
- Regular fat items account for **$425.36K**

### 📅 Sales Trend
- Sales peaked in **2018**, making it the highest-revenue year on record

### ⭐ Average Ratings by Category

| Category | Rating |
|----------|--------|
| Meat | 4.00 |
| Household | 3.95 |
| Baking Goods | 3.95 |
| Canned | 3.95 |
| Frozen Foods | 3.93 |
| Others | 3.93 |
| Health & Hygiene | 3.93 |
| Dairy | 3.92 |
| Fruits & Vegetables | 3.91 |
| Seafood | 3.91 |
| Starchy Foods | 3.91 |
| Breakfast | 3.90 |
| Snack Foods | 3.90 |
| Soft Drinks | 3.89 |
| Hard Drinks | 3.84 |
| Breads | 3.83 |

> Null rating values were excluded from calculations as they were not relevant for all customers.

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** — Dashboard development & data modeling
- **Power Query** — Data extraction, cleaning & transformation
- **DAX (Data Analysis Expressions)** — Custom KPI measures & calculated columns
- **Microsoft Excel** — Source dataset (`.xlsx`)

---

## ⚙️ DAX Measures

```dax
-- Total Sales
Total Sales = SUM('BlinkIT Grocery Data'[Sales])

-- Average Sales
Avg Sales = AVERAGE('BlinkIT Grocery Data'[Sales])

-- Average Rating
Avg Rating = AVERAGE('BlinkIT Grocery Data'[Rating])

-- Number of Items
No of Items = COUNTROWS('BlinkIT Grocery Data')
```

### 📐 Metrics Matrix (Dynamic Slicer)
```dax
Metrics = {
    ("Total Sales", NAMEOF('BlinkIT Grocery Data'[Total Sales]), 0),
    ("Avg Sales",   NAMEOF('BlinkIT Grocery Data'[Avg Sales]),   1),
    ("Avg Rating",  NAMEOF('BlinkIT Grocery Data'[Avg Rating]),  2),
    ("No of Items", NAMEOF('BlinkIT Grocery Data'[No of Items]), 3)
}
```
> This matrix powers the dynamic slicer, allowing all KPIs and charts to update based on the selected metric.

---

## 📁 Project Structure

```
📦 Blinkit-Sales-Analysis
 ┣ 📊 BLINKIT_SALES_DASHBOARD.pbix   # Power BI dashboard file
 ┣ 📂 BlinkIT_Grocery_Data.xlsx      # Raw dataset
 ┣ 🖼️ background_kpi.png             # Custom dashboard background
 ┣ 📑 Blinkit_Sales_Analysis.pptx    # Project presentation
 ┗ 📄 README.md                      # Project documentation
```

---

## 🚀 Getting Started

1. **Clone this repository**
   ```bash
   git clone https://github.com/your-username/blinkit-sales-analysis.git
   ```

2. **Open the dashboard**
   - Launch **Power BI Desktop**
   - Open `BLINKIT_SALES_DASHBOARD.pbix`

3. **Explore the data**
   - Use slicers to filter by outlet, location, fat content, or item type
   - Switch KPI metrics using the dynamic metric slicer

---

## 📋 Steps Followed

1. Loaded the dataset (`.xlsx`) into Power BI Desktop
2. Used Power Query Editor to inspect column distribution, quality, and profiling
3. Cleaned and transformed data for accuracy and consistency
4. Defined key business KPIs and built DAX measures
5. Built an interactive single-page dashboard with charts and card visuals
6. Created a custom metrics matrix to power a dynamic slicer across all visuals
7. Published the report to Power BI Service

---

## 📬 Contact

Feel free to reach out or connect if you have feedback or questions!

<p align="left">
  <a href="https://www.linkedin.com/"><img src="https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin" /></a>
  <a href="mailto:your-email@example.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" /></a>
</p>

---

<p align="center">⭐ If you found this project helpful, please consider giving it a star!</p>
