# 📊 Indian Superstore Analytics — RLS-Enabled Regional Sales & Profit Dashboard

---

## 📌 1. Project Background & Business Scenario

You are working as a **BI Analyst** for a retail organization operating across multiple regions in **India**. The company sells products across three primary categories: **Technology**, **Furniture**, and **Office Supplies**. 

Executive management requires a centralized business intelligence dashboard to monitor overall revenue growth, profit margins, customer behavior, and fulfillment shipping performance. Additionally, security protocols mandate that Regional Managers must only access sales data specific to their designated territories.

---

## 🎯 2. Project Objectives

- **ETL Transformation:** Clean, transform, and normalize retail order datasets using Power Query.
- **Data Modeling:** Establish a **Star Schema** data model connecting central fact tables to dimension tables.
- **Row-Level Security (RLS):** Implement Static RLS roles for territory managers (Central, East, South, North, West).
- **Multi-Page Reporting:** Design interactive dashboards featuring Executive Sales, Customer Profiling, Product Profitability, and Regional Manager performance views.
- **Advanced BI Functionality:** Integrate Bookmarks, Custom Tooltips, Hierarchy Drill-Downs, and Right-Click Drill-Through features.

---

## 🏗️ 3. Phased Architecture & Execution Strategy

### 🧹 Phase 1: Data Import & Cleaning (Power Query ETL)
- **Source Data:** Excel dataset containing order, customer, product, and regional records.
- **Data Cleaning:** Removed null values, duplicates, and unneeded rows; set appropriate data types (Date, Decimal, Text).
- **Custom Logic:** Added custom calculated column:
  Delivery Days = Ship Date - Order Date

### 📐 Phase 2: Data Modeling & DAX Measures
- **Model Type:** Built a **Star Schema** centered around the `Orders` fact table.
- **Dimensions:** Connected `Dim_Date`, `Customer`, `Product`, and `Zone` (Region) tables via 1-to-Many single-direction relationships.
- **Key DAX Metrics:**
  - `Total Sales` 
  - `Total Profit` 
  - `Profit %`
  - `Total Orders`
  - `Discount %`
  - `Delivery Days`
    
---

## 🖥️ 4. Dashboard Architecture & Key Pages

### 📈 Page 1: Sales Overview
- **Key Metrics:** Total Sales (₹1.05bn), Total Profit (₹121.80M), Profit Margin (11.61%), Total Orders (51K).
- **Visuals:** Monthly Sales Trend area chart, Geographic Sales Density map by State, Sales breakdown by Category/Sub-Category, Top/Bottom products table.

### 👤 Page 2: Customer Insights & Profiling
- **Customer Segmentation:** Sales breakdown across Consumer, Corporate, and Home Office segments.
- **High-Value Accounts:** Top and bottom customer ranking tables based on net contribution.
- **Drill-Through (Page 2.1):** Right-click drill-through on any customer to access granular transaction order histories, shipping locations, and order profit margins.

### 🏷️ Page 3: Product & Discount Profitability
- **Discount Impact:** Scatter plot comparing `Discount %` against `Profit Status` to pinpoint loss-making discount thresholds.
- **Performance Matrix:** Detail ranking table analyzing sales, profits, and discounts per product.
- **Bookmark View Switching:** Integrated interactive toggles to switch between shipping mode performance (`Average Delivery Days`) and profit sensitivity views.

### 🗺️ Page 4: Region & Manager View
- **Regional Analysis:** Regional profit donut charts and historical timeline metrics.
- **Hierarchy Drill-Down:** Dynamic column charts enabling breakdown from `Region` ➔ `State` ➔ `City`.
- **Territory Toggles:** Regional sales and regional profit view switching bookmarks.

---

## ⚡ 5. Advanced Interactive Features Summary

1. **Static Row-Level Security (RLS):** Restricted access roles created for `Central`, `East`, `South`, `North`, and `West` regional managers.
2. **Bookmark Navigation:** Clean top-navigation bar across all pages with toggle states.
3. **Custom Tooltips:** Mouse-hover preview pages displaying deep product and category details.
4. **Drill-Through Target:** Page 2.1 configured to instantly pull specific customer order profiles.

---

## 💡 6. Executive Strategic Recommendations

1. **Cap Discount Thresholds:** Restrict discounts on loss-making sub-categories (Tables & Bookcases) to a maximum of 15%–20%.
2. **Optimize Logistics:** Streamline Standard Class fulfillment to reduce average shipping durations below 5 days[span_36].
3. **Replicate Regional Models:** Scale successful sales strategies from leading territories (North & West) into Central and South markets.

---

## 📁 7. Repository Structure

```text
.
├── Indian Superstore Analytics Dashboard_Mohd Sirajuddin Ahmed.pdf   # Visual Presentation Deck (PDF)
└── README.md                                                        # Documentation
