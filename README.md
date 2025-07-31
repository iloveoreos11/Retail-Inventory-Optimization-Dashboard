# 🛒 Retail Inventory Optimization Dashboard (2023)

## 📊 Project Overview

This project analyzes retail inventory and sales data for three products (A, B, and C) across multiple warehouses over a 90-day period in 2023. The goal is to identify stockout risks, overstock inefficiencies, and improve restocking strategies to support better operational planning and cost savings.

Retailers often struggle with balancing inventory: too much leads to wasted storage costs, too little results in missed sales and customer dissatisfaction. This analysis helps address both issues using Excel-based data cleaning and Power BI dashboarding.

---

## 🎯 Business Goals

- Identify trends in daily stock levels, restocks, and sales across products and warehouses
- Detect stockout risks and understocking patterns
- Optimize restock timing based on average daily sales
- Recommend strategies to improve inventory turnover and reduce excess

---

## 🗂️ Dataset Overview

The dataset simulates retail operations data with the following fields:

- `Date`: Daily record of activity
- `Product`: Product name (A, B, C)
- `Warehouse`: Fulfillment location (North, South, East)
- `Sales`: Units sold per day
- `Stock_Level`: Remaining inventory at end of day
- `Restock_Amount`: Units added back into stock (if any)
- `Stockout_Flag`: Calculated flag for when inventory drops below 10
- `7_day_avg_sales`: Rolling 7-day average sales to monitor product demand

---

## 🔧 Tools Used

- **Excel** for data cleaning, pivot analysis, and calculated columns
- **Power BI** for dashboard creation and data visualization
- **Python** (initially, to validate structure and prep if needed)

---

## 🧼 Data Cleaning Steps (Excel)

1. **Formatted Date column** to readable `dd/mm/yyyy` format
2. **Removed duplicate records** to ensure data accuracy
3. **Created `Stockout_Flag`** column to identify low-stock days (`=IF([Stock_Level]<10, "Yes", "No")`)
4. **Calculated `7_day_avg_sales`** to estimate reorder points (rolling average of sales)
5. **Created Pivot Tables** summarizing:
   - Total Sales per Product and Warehouse
   - Total Restock Volume
   - Number of Stockout Days
   - Weekly trends (using `=WEEKNUM()`)

---

## 📊 Dashboard Features

Built using Power BI, the dashboard includes the following visuals:

- **Line Chart**: Stock levels over time for each product
- **Bar Chart**: Total Sales vs Restock Volume
- **KPI Cards**: Total Sales, Average Daily Sales, Stockout Days
- **Weekly Breakdown Table**: Restock timing and demand behavior
- **Recommendations Panel**: Strategic suggestions based on insights

---

## 🔍 Key Insights

- 📉 **Product stock levels** declined steadily across all warehouses, showing predictable consumption patterns.
- ⚠️ **Stockout days were minimal**, but products consistently dipped below critical thresholds, especially near restock intervals.
- 🛒 **All products sold evenly (~12 units/day)**, meaning restock cycles can be predicted using historical average sales.
- 🚚 **Restocks occurred every 15 days**, suggesting room to optimize frequency or automate alerts.
- 🧊 **Warehouse performance** was similar across regions, but Product C in the East warehouse approached stockout more often than others.

---

## ✅ Strategic Recommendations

1. **Set automated low-stock alerts** when inventory drops below 30 units to avoid stockouts.
2. **Adjust restock frequency** from 15 days to 12 days based on 7-day rolling sales averages.
3. **Introduce dynamic reorder points** that adapt to product demand rather than fixed cycles.
4. **Visualize daily trends** weekly to track seasonal or campaign-related spikes in product demand.
5. **Prioritize safety stock thresholds** for Product C in the East warehouse to avoid last-minute restocks.

---

## 📂 Files Included

- `retail_inventory_cleaned.xlsx` – Cleaned dataset with calculated fields  
- `inventory_dashboard.pbix` – Power BI file with visuals and layout  
- `dashboard_screenshot.png` – Preview of the full dashboard  
- `README.md` – Full project documentation

---

