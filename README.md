# 📈 Blinkit E-commerce Sales Performance Analysis

## Project Title

**Blinkit E-commerce Sales Performance Analysis using Advanced SQL**

## Description

This project showcases a complete data analysis pipeline built entirely with SQL. The focus is on cleaning, transforming, and analyzing a dataset of Blinkit (e-commerce/retail) sales transactions. The goal is to move beyond simple data retrieval to generate **actionable business intelligence**, specifically identifying key sales drivers, optimizing inventory strategy, and evaluating outlet performance.

## Features / Purpose

The analysis delivers critical insights by addressing core business questions:

* **Data Integrity:** Implemented data cleansing procedures to ensure the accuracy and reliability of all subsequent analyses.
* **KPI Benchmarking:** Calculated and presented core financial and operational Key Performance Indicators (KPIs), including **Total Sales** (in millions), **Average Transaction Value**, and **Overall Item Rating**.
* **Sales Segmentation:** Identified the highest-performing product categories (e.g., **Snack Foods**) and the most profitable retail formats (**Supermarket Type3**).
* **Strategic Reporting:** Generated detailed reports to support strategic decisions:
    * Sales distribution segmented by **Outlet Size** and **Outlet Establishment Year**.
    * Localized performance analysis using **Conditional Aggregation** based on `Item_Fat_Content` across different `Outlet Location Types`.
* **Performance Dashboard:** Created a comprehensive metric summary for all Outlet Types, facilitating easy comparative operational review.

## Technologies Used

* **SQL (MySQL/PostgreSQL Syntax):** The entire analytical pipeline was executed using standard SQL commands.
* **Key SQL Features Demonstrated:**
    * **Data Cleaning:** `UPDATE` and `CASE` statements for standardizing categorical data (e.g., Item Fat Content).
    * **Schema Management:** `ALTER TABLE` for column renaming and data type casting (`CAST()`).
    * **Advanced Aggregation:** `GROUP BY`, `SUM`, `AVG`, and **Window Functions** for market share percentage calculation.
    * **Conditional Logic:** `SUM(CASE WHEN...)` for deep-dive segmentation reports.
* **Data Visualization:** Output queries are optimized for direct integration into Business Intelligence (BI) tools like Tableau or Power BI.

## How to Run the Project

1.  **Database Setup:** Ensure you have a running instance of a SQL database (MySQL is recommended for the syntax used).
2.  **Import Data:** Import the `[Your_Data_File.csv or .xlsx]` file into your database and name the table `blinkit_glosary`.
3.  **Execute Script:** Open the `Blinkit SQL analysis.sql` file.
4.  **Run Queries:** Execute the queries sequentially, as the **Data Cleaning** steps must be completed before the **KPI** and **Analytical Reporting** sections will run correctly.

## File Descriptions

* `Blinkit SQL analysis.sql`: This is the main file containing all the documented SQL code, covering data cleaning, KPI calculation, and all detailed analytical queries.
* `[Original Data File Name]`: (Optional: Include the original data file if you are allowed to share it.)

## Author / Contact

* **Author:** [Your Full Name]
* **GitHub:** [Your GitHub Profile Link]
* **LinkedIn:** [Your LinkedIn Profile Link]
* **Email:** [Your Professional Email Address]
