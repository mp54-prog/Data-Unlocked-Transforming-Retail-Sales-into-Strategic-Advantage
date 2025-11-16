# 📊 Data-Unlocked-Transforming-Retail-Sales-into-Strategic-Advantage
Retail Sales Analytics — End-to-End Data Cleaning, SQL Analysis & Insight Generation
📘 Project Summary

This project delivers an end-to-end retail analytics workflow using Python, SQL, and visualization techniques to uncover key business insights from a messy retail dataset.

The objective is to identify:

Revenue drivers

Discount effectiveness

Seasonal trends

Customer purchasing behaviours

Opportunities for retail strategy optimisation

The workflow replicates real-world analytics processes:
raw data → cleaning → validation → SQL modelling → analytics → visualization → actionable insights

🛠️ Tech & Skills Demonstrated
Tools

Python (Pandas, NumPy)

SQL (SQLite/PostgreSQL)

Excel (business reporting)

Matplotlib / Seaborn

Jupyter Notebook

Skills

Data cleaning & preprocessing

Data quality assessment

SQL analytical modelling

Exploratory data analysis

Statistical correlation analysis

Business insight generation

Visualization & storytelling

📁 Repository Structure
.
├── data/
│   ├── raw_sales.csv
│   └── cleaned_sales.csv
├── scripts/
│   ├── clean_data.py
│   └── eda_analysis.ipynb
├── sql/
│   ├── exploratory_queries.sql
│   └── advanced_aggregations.sql
├── visuals/
│   ├── revenue_distribution.png
│   ├── discount_vs_revenue_scatter.png
│   ├── monthly_category_heatmap.png
│   └── monthly_sales_trend.png
└── README.md

📦 Dataset Description

A mock retail transaction dataset containing:

Order_ID

Customer_Name

Email

Phone

Product_Category

Order_Date

Revenue (GBP)

Discount (%)

The dataset includes real-world issues, such as:

Missing emails

Duplicate phone numbers

Missing discounts

Duplicate transactions (e.g., IDs 101, 103, 104)

Mixed date formats

Mis-typed numerical fields

The objective is to simulate a realistic data-quality environment.

🔧 1. Data Cleaning (Python)

Cleaning performed via scripts/clean_data.py, including:

Data Quality Fixes

Removed duplicate rows for Order IDs 101, 103, 104

Standardized all dates → YYYY-MM-DD

Missing emails populated as: not_provided@email.com

Missing phone numbers replaced with 0000000000

Missing discounts set to 0.00%

Duplicate phone numbers flagged for CRM review

Revenue + discount fields cast to numeric formats

Trimmed whitespace, normalized categorical values

Output:

✔ cleaned_sales.csv — fully validated dataset

📊 2. Exploratory Data Analysis (EDA)

EDA performed in Python to examine:

Revenue distributions

Discount behaviour patterns

Outliers (IQR-based)

Customer segmentation by spend

Early trend detection

Correlation analysis (Revenue vs Discount)

Key Finding:
Discount percentage shows a strong positive correlation (r ≈ 0.828) with total revenue.

🗄️ 3. SQL Analysis

SQL scripts stored in /sql/.

Core SQL Queries

Total revenue per category

Average discount per category

Monthly sales trends

Advanced SQL Queries

Window functions for revenue ranking

RANK() OVER (ORDER BY SUM(Revenue) DESC)


Rolling 3-month revenue trend

ROWS BETWEEN 2 PRECEDING AND CURRENT ROW


Category-level seasonality breakdown

Discount elasticity exploration

Customer lifetime revenue segmentation

Outputs exported to Excel for business stakeholders.

📉 4. Visualizations

All visuals stored in /visuals/.

Included Charts

Scatter Plot — Discount % vs Revenue

Heatmap — Monthly revenue by category

Histogram — Distribution of transaction values

Line Chart — Monthly sales trend

These visualizations validate quantitative findings and support stakeholder communication.

💡 5. Key Insights (Quantified & Actionable)
1. Revenue Concentration

Furniture (£4,300) + Electronics (£4,200) = 83% of total revenue

Overreliance on two categories → high concentration risk

2. Discount Effectiveness

Strong correlation between discount rate and revenue (r ≈ 0.828)

Discounted categories (Furniture, Electronics) show highest uplift

Excessive discounts risk margin erosion

3. Seasonal Demand Patterns

Sales peak in January (£3,000) and October (£1,800)

Low-demand months → March, May, August

Seasonal category behaviour:

Electronics peak in winter

Clothing performs best in warm months

📌 6. Strategic Recommendations

✔ Reduce revenue concentration
→ Strengthen Clothing category or diversify inventory offerings

✔ Optimize discount strategy
→ Cap Furniture discounts at <20% to protect margins
→ Use pricing discipline to avoid over-reliance on promotions

✔ Mitigate seasonal dips
→ Launch targeted campaigns during historically low months
→ Introduce cross-category bundles aligned with peak seasons

✔ Forecasting & Inventory Alignment
→ Use past seasonal behaviour to optimize future stock levels

🚀 7. How to Run the Project
Install Dependencies
pip install -r requirements.txt

Run Data Cleaning Script
python scripts/clean_data.py

Run SQL Queries
sqlite3 sales.db < sql/exploratory_queries.sql
sqlite3 sales.db < sql/advanced_aggregations.sql

View Visualizations

Go to the /visuals folder.

🔮 8. Next Steps

Integrate Python + SQL into an automated pipeline

Add an interactive dashboard (Power BI / Tableau / Streamlit)

Add customer segmentation (clustering models)

Introduce profitability analysis (COGS-enabled data)

Implement sales forecasting models

Add Airflow/Prefect scheduling for automated reporting
