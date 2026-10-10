CadetX — Heavy Supplier, Inventory & Warehouse Analytics

A 12-week data science project focused on supplier performance, inventory optimization, warehouse operations, and demand forecasting.

The goal is to reduce dead stock, prevent stockouts, and improve supplier reliability across six warehouses.

Project Overview

MetricDescriptionTime Period2019–2025Customers500 across 16 statesSuppliers8 vendorsProducts30 SKUsWarehouses6 branchesPurchase Orders24,000Pending Deliveries2,370 (9.9%)Data Completeness99.6% reported 

Data quality note: The dataset summary reports 2,370 missing values, mostly related to purchase-order dates. Validate this figure against the actual dataset before drawing conclusions.

Dataset and Data Model

The project connects customers, products, suppliers, sales, purchase orders, invoices, payments, branches, inventory, and stock movements.

erDiagram CUSTOMERS ||--o{ SALES_ORDERS_HEADER : places SALES_ORDERS_HEADER ||--|{ SALES_ORDERS_LINES : contains PRODUCTS ||--o{ SALES_ORDERS_LINES : sold_as SALES_ORDERS_HEADER ||--o| INVOICES : billed_by INVOICES ||--o{ PAYMENTS : settled_by SUPPLIERS ||--o{ PURCHASE_ORDERS_HEADER : receives PURCHASE_ORDERS_HEADER ||--|{ PURCHASE_ORDERS_LINES : contains PRODUCTS ||--o{ PURCHASE_ORDERS_LINES : bought_as BRANCHES ||--o{ INVENTORY_MASTER : stocks PRODUCTS ||--o{ INVENTORY_MASTER : tracked_in BRANCHES ||--o{ STOCK_LEDGER : records PRODUCTS ||--o{ STOCK_LEDGER : moves 

12-Week Project Roadmap

[ ] Week 1 — Dataset exploration and exploratory data analysis

[ ] Week 2 — Data cleaning and missing-value treatment

[ ] Week 3 — SQL database design and data validation

[ ] Week 4 — Supplier performance analysis

[ ] Week 5 — Inventory health and dead-stock analysis

[ ] Week 6 — Stockout and replenishment analysis

[ ] Week 7 — Warehouse performance comparison

[ ] Week 8 — Demand forecasting

[ ] Week 9 — Inventory optimization models

[ ] Week 10 — KPI dashboard development in Power BI

[ ] Week 11 — Model evaluation and business recommendations

[ ] Week 12 — Final report, documentation, and deployment

These are Markdown checkboxes. They can be ticked in GitHub's editor, but they do not provide a persistent interactive progress dashboard.

Key KPIs

Supplier on-time delivery rate

Purchase-order fulfillment rate

Average supplier lead time

Supplier defect rate

Inventory turnover ratio

Days of inventory on hand

Stockout rate

Dead-stock value

Inventory carrying cost

Reorder-point accuracy

Forecast accuracy

Warehouse fulfillment rate

Order cycle time

Backorder rate

Customer order fulfillment rate

Outstanding invoice value

Days sales outstanding

Branch-level inventory utilization

Fill rate

Purchase-order aging

KPIs will be calculated from validated source data; no unverified results are assumed.

Models to Build

Demand forecasting using statistical and machine-learning methods

Supplier reliability scoring

Inventory segmentation using ABC analysis

Reorder-point and safety-stock estimation

Stockout risk prediction

Dead-stock identification

Inventory optimization recommendations

Quick Start

1. Clone the repository

git clone https://github.com/HARSHPANDEY9756/cadetx-warehouse-analytics.git cd cadetx-warehouse-analytics 

2. Create a virtual environment

python -m venv .venv 

Windows PowerShell:

.\.venv\Scripts\Activate.ps1 

3. Install dependencies

python -m pip install --upgrade pip pip install pandas numpy scikit-learn statsmodels matplotlib seaborn jupyter sqlalchemy 

4. Explore the dataset

jupyter notebook notebooks/week-01-eda.ipynb 

5. Run the data-cleaning pipeline

python src/data_cleaning.py 

Prerequisites: Python 3.8 or later, the project dataset, and the notebook and script files referenced above. If your project uses SQL Server, configure the database connection separately.

Technology Stack

Programming: Python

Data analysis: Pandas, NumPy

Machine learning: Scikit-learn, Statsmodels

Visualization: Matplotlib, Seaborn, Power BI

Database: SQL Server, T-SQL, SQLAlchemy

Development: Jupyter Notebook, Google Colab

Version control: Git, GitHub

Repository Structure

cadetx-warehouse-analytics/ ├── data/ ├── notebooks/ │ └── week-01-eda.ipynb ├── src/ │ └── data_cleaning.py ├── README.md └── requirements.txt 

Adjust this structure to match the files actually present in your repository.

Project Progress

Track completed milestones using the roadmap above. Add validated charts, model results, and Power BI screenshots as the project develops.

Author

Harsh Pandey
Data Science Analyst

GitHub: https://github.com/harshpandey97

LinkedIn: https://www.linkedin.com/in/harsh-pandey-395a10237

Email: harshpandey6012@gmail.com

License

This project is intended to be released under the MIT License. See LICENSE if the license file exists in the repository.

