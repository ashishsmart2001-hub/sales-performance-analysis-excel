# Sales Performance Analysis Dashboard (Excel)

## 📌 Project Overview

This project is an end-to-end sales performance analysis built entirely in **Microsoft Excel**, covering data modeling, KPI calculation, pivot table analysis, and an interactive dashboard. It was developed as a self-paced practice project using a training dataset to demonstrate practical Excel skills used in real-world business reporting, with AI assistance used for guidance during development.

The dashboard answers key business questions such as: Which regions and channels drive the most revenue? Which products and customers are most profitable? How does sales performance trend over time?

## 🎯 Business Objectives

- Track overall sales, profit, and order volume across a 5-year period
- Compare performance across regions (Midwest, Northeast, South, West)
- Compare performance across sales channels (Distributor, Export, Wholesale)
- Identify top-performing products and top customers by profit
- Monitor monthly sales and profit trends

## 🗂️ Dataset

- **Source:** Training/practice dataset used for a course project
- **Time period:** January 2014 – November 2018
- **Volume:** 42,736 transaction rows across 10,684 unique orders
- **Scope:** 3,603 unique customers, 414 products across 13 categories, 3 sales channels, 4 regions

**Key fields:** Order Number, Order Date, Ship Date, Due Date, Customer Name, Channel, Warehouse Code, Region/State, Product Name & Category, Order Quantity, Unit Price, Line Total, Unit Cost, Row Cost, Profit, Profit Margin %

> **Note:** Product and category names in this dataset are generic placeholders (e.g., "Product 1", "Category 5") rather than real branded products, as is typical for practice/training datasets.

## 🛠️ Tools & Technologies

- Microsoft Excel
- Excel Tables (structured references)
- Pivot Tables & Pivot Charts
- Excel Formulas (VLOOKUP-style lookups, COUNTA + UNIQUE, SUM)
- Slicers for interactive filtering

## 🔄 Data Preparation / Cleaning

- Started from a raw transactional table (`Sales Orders`) containing only ID-based references (customer index, product index, region index)
- Built lookup tables for **Customers**, **Products**, **Regions** (US city-level data), and **State → Region** mapping
- Merged the raw data with lookup tables to create an enriched, analysis-ready table (`Final Sales Data`) containing readable fields: customer names, product names/categories, region, and state
- Added a calculated **Profit Margin %** column using structured table references

## 📊 KPIs

- **Total Sales:** $823,979,266
- **Total Profit:** $307,848,373
- **Profit Margin %:** 37.36%
- **Total Orders:** 10,684 (calculated using `COUNTA(UNIQUE(...))` on Order Number)

## 📈 Dashboard / Analysis

The dashboard includes the following components, built on top of pivot tables:

- **KPI Cards:** Total Sales, Profit Margin %, Total Orders, Total Profit
- **Category Performance:** Horizontal bar chart comparing Total Sales vs. Total Profit across 13 product categories
- **Channel Distribution:** Donut chart showing revenue share across Distributor, Export, and Wholesale channels
- **Sales Trend:** Line chart tracking Total Sales and Total Profit by month
- **Region Performance:** Bar chart showing profit margin % across Midwest, Northeast, South, and West
- **Top 10 Products by Sales:** Bar chart ranking best-selling products
- **Top 10 Customers by Profit:** Bar chart ranking most profitable customers

**Interactive filters (slicers):** Order Date (by month/year), Warehouse Code, Channel, Region

## 🔍 Key Insights

- **Wholesale is the dominant channel**, contributing 54% of total sales, followed by Distributor (31%) and Export (15%)
- **West and South regions lead in profit margin**, at 30.26% and 27.24% respectively, both ahead of Northeast (16.70%) and Midwest (25.80%)
- Monthly sales show relatively **stable performance with modest seasonal variation**, with the strongest months in mid-year (June–August) and a decline toward November–December
- A small set of top products and top customers contribute disproportionately to profit, visible in the Top 10 Products and Top 10 Customers charts, indicating concentration risk if these accounts/products underperform

## 💡 Business Recommendations

- Investigate why the Northeast region trails other regions in profit margin — this may point to pricing, cost structure, or channel mix issues specific to that region
- Since Wholesale drives the majority of revenue, prioritize retention and account management strategies for top Wholesale customers and products
- Monitor the year-end sales dip (Nov–Dec) to determine if it is seasonal and, if so, plan promotions or inventory adjustments in advance

## 📷 Dashboard Preview

![Dashboard Overview](screenshots/dashboard-overview.png)

*Full interactive dashboard showing KPI cards, category performance, channel split, sales trend, regional performance, and top products/customers.*

## 📁 Repository Structure

```
sales-performance-analysis-excel/
│
├── README.md
├── data/
│   └── Sales_Performance_Analysis.xlsx
└── screenshots/
    └── dashboard-overview.png
```

## 🚀 How to Use / Open the Project

1. Download `Sales_Performance_Analysis.xlsx` from the `data/` folder
2. Open the file in Microsoft Excel (2016 or later recommended, for full Pivot Table and slicer support)
3. Navigate to the **Dashboard** tab to view the interactive report
4. Use the slicers (Order Date, Warehouse Code, Channel, Region) to filter the dashboard
5. Explore the **Pivot Table**, **Final Sales Data**, and lookup tables (**Customers**, **Products**, **Regions**, **State Regions**) to see the underlying data model

## 📚 Skills Demonstrated

- Data modeling using lookup tables and structured Excel Tables
- Building pivot tables for multi-dimensional analysis (by month, region, channel, product, customer)
- KPI calculation using Excel formulas (SUM, COUNTA, UNIQUE)
- Interactive dashboard design with slicers and charts
- Business insight generation from transactional sales data

## 👤 Author

**Ashish Kumar**
GitHub: [ashishsmart2001-hub](https://github.com/ashishsmart2001-hub)
