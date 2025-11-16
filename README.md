# Data-Unlocked-Transforming-Retail-Sales-into-Strategic-Advantage
Retail Sales Analytics — End-to-End Data Cleaning, SQL Analysis & Insight Generation
Project Summary

A compact end-to-end analytics project demonstrating data cleaning (Python), SQL analytics, EDA, and business-oriented insight generation.
The goal: analyze retail sales data to understand revenue drivers, discount behavior, and seasonal patterns.

This project shows the full workflow:
raw data → cleaned dataset → SQL aggregations → visual insights → strategic findings.

Key Skills Demonstrated

Python (Pandas) — cleaning, preprocessing, EDA

SQL — category-level aggregation, time-series trends, discount analysis

Visualization — scatter plot, histogram, heatmap

Business Interpretation — translating findings into actionable recommendations

Dataset

Mock retail transaction dataset containing:

Order_ID

Customer_Name

Product_Category

Order_Date

Revenue

Discount (%)

Workflow Overview
1. Data Cleaning (Python)

Removed duplicate transactions

Standardized date formats

Filled missing values (email, phone, discount)

Validated revenue and discount ranges

Exported cleaned dataset for SQL analysis

2. Exploratory Data Analysis

Basic distributions

Outlier checks

Revenue segmentation

Initial trend exploration

3. SQL Analysis

Core queries include:

Revenue by Product Category

Monthly Sales Trend

Average Discount per Category

These queries provide the foundation for identifying category performance and seasonal behavior.

4. Visualizations

(Stored in the /visuals folder)

Scatter Plot: Relationship between discount rate & revenue

Heatmap: Revenue by month and category

Histogram: Distribution of transaction values

Insights (High-Level)

Category Drivers: Furniture & Electronics contribute the majority of revenue.

Discount Behavior: Higher discount rates correlate strongly with increased sales.

Seasonality: Clear sales peaks during winter months; lower performance in early spring.

How to Run

Install requirements

pip install pandas


Run the cleaning script

python scripts/clean_data.py


Load cleaned_sales.csv into your SQL environment.

Execute queries from /sql/analysis.sql.

View visualizations in /visuals.
