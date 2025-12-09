# Blinkit Sales Analysis (SQL Project)

## Project Overview

This project serves as a comprehensive demonstration of advanced SQL capabilities applied to a real-world e-commerce sales dataset (Blinkit). The methodology covers the entire data lifecycle: **Data Cleaning, Feature Engineering, KPI Calculation,** and **Strategic Reporting**, providing actionable business intelligence directly from the database level.

## Methodology and Technical Depth

The entire analysis was conducted using SQL, focusing on efficiency and data integrity.

### 1. Data Preparation and Cleaning

* **Initial Data Audit:** Began by viewing the raw data to identify inconsistencies and structural issues (e.g., column naming, data types).
* **Column Standardization:** Utilized the `ALTER TABLE...CHANGE` command to rename ambiguous column headers (`ï»¿Item Fat Content`, `Total Sales`) for better query readability and maintainability.
* **Text Cleaning (`UPDATE` and `CASE`):** Executed a critical data cleaning step to standardize the `Item_Fat_Content` feature. Multiple low-fat labels ('LF', 'low fat') were unified to 'Low Fat', and 'reg' was converted to 'Regular'. This ensures accurate grouping for downstream profitability analysis.
* **Data Type Casting:** Explicitly cast relevant columns (`Total_sales`, `Item_Visibility`) to the `DOUBLE` data type to ensure precise numerical calculations.

### 2. Key Performance Indicator (KPI) Calculation

Calculated mission-critical metrics using aggregate functions to establish a foundational performance baseline:

* **Total Sales:** $\sum(\text{Total\_sales})$
* **Average Sales:** $\text{AVG}(\text{Total\_Sales})$
* **Order Volume:** $\text{COUNT}(*)$
* **Average Rating:** $\text{AVG}(\text{Rating})$
* *Note: Total Sales was presented in millions using the `CAST` function for executive reporting.*

### 3. Deep-Dive Analytical Reporting

The core of the project involved segmented analysis to diagnose performance drivers:

| Analysis | SQL Technique Used | Business Insight Gained |
| :--- | :--- | :--- |
| **Product Performance** | `GROUP BY Item_Type` | Identified **Snack Foods** as the leading sales category, informing inventory priority. |
| **Fat Content Analysis** | `GROUP BY Item_Fat_Content` | Determined the overall sales contribution of Low Fat vs. Regular items. |
| **Operational Efficiency** | `GROUP BY Outlet_Establishment_Year` | Tracked performance trends based on the store's age, aiding decisions on store upgrades/closures. |
| **Sales Segmentation** | **Conditional Aggregation** (`SUM(CASE WHEN...)`) | Analyzed the distribution of Low Fat vs. Regular sales across different `Outlet_Location_Type`s, allowing for geographical marketing customization. |
| **Market Share** | **Window Functions** (`SUM(SUM(...)) OVER()`) | Calculated the percentage of total sales contributed by each `Outlet_Size` (e.g., Small, Medium, High), revealing the market share of store formats. |

### 4. Comprehensive Outlet Metric Dashboard

* Generated a consolidated report for all `Outlet_Type`s (e.g., Supermarket Type1, Grocery Store) summarizing **Total Sales, Average Sales, Order Count, Average Rating,** and **Average Item Visibility**, providing a single-source truth for comparative operational review.

## Technologies

* **SQL (MySQL/PostgreSQL Syntax):** Expert-level application.
* **SQL Features:** `ALTER TABLE`, `UPDATE`, `CASE`, `GROUP BY`, `CAST`, `IFNULL`, and Aggregate Functions.
* **Data Focus:** E-commerce Sales/Retail Analytics.

---
*Developed by [Your Name/GitHub Username]*
