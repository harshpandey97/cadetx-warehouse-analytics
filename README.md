CadetX
Dataset Data model Roadmap KPIs Models Quick start
Heavy supplier, inventory & warehouse analytics
A 12-week data science project on how heavy equipment parts move through 6 warehouses, 8 suppliers and 500 customers. The goal: less dead stock, fewer stockouts, more reliable suppliers.
See project progress Run it locally
Dock board: rows per table
Bar length is logarithmic so small master tables stay visible.
Dataset overview
Time period
2019 – 2025
Customers
500 in 16 states
Suppliers
8 vendors
Products
30 SKUs
Branches
6 warehouses
Total records
–
2,370 of 24,000 purchase orders are still pending delivery 9.9% at risk
Data is 99.6% complete, with 2,370 missing values (mostly PO dates).
How the tables connect
Orders flow to invoices and payments; purchase orders flow from suppliers into branch stock, and every movement lands in the stock ledger.
erDiagram
    CUSTOMERS ||--o{ SALES_ORDERS_HEADER : places
    SALES_ORDERS_HEADER ||--|{ SALES_ORDERS_LINES : contains
    PRODUCTS ||--o{ SALES_ORDERS_LINES : sold_as
    SALES_ORDERS_HEADER ||--o| INVOICES : billed_by
    INVOICES ||--o{ PAYMENTS : settled_by
    SUPPLIERS ||--o{ PURCHASE_ORDERS_HEADER : receives
    PURCHASE_ORDERS_HEADER ||--|{ PURCHASE_ORDERS_LINES : contains
    PRODUCTS ||--o{ PURCHASE_ORDERS_LINES : bought_as
    BRANCHES ||--o{ INVENTORY_MASTER : stocks
    PRODUCTS ||--o{ INVENTORY_MASTER : tracked_in
    BRANCHES ||--o{ STOCK_LEDGER : records
    PRODUCTS ||--o{ STOCK_LEDGER : moves
12-week roadmap
0 of 0 tasks done 0%
Tick a task to update the progress. Your ticks are kept in this browser only.
20+ KPIs we will build
Models to build
Quick start
Copy# Clone
git clone https://github.com/HARSHPANDEY9756/cadetx-warehouse-analytics.git
cd cadetx-warehouse-analytics

# Install dependencies
pip install pandas numpy scikit-learn statsmodels matplotlib seaborn jupyter sqlalchemy

# Explore the data (Week 1)
jupyter notebook notebooks/week-01-eda.ipynb

# Run the data cleaning pipeline
python src/data_cleaning.py
Tech stack
Python 3.8+PandasNumPy Scikit-learnStatsmodelsSQL Server / T-SQL Power BIMatplotlibSeaborn JupyterGoogle ColabGitHub
Harsh Pandey
Data Science Analyst
harshpandey6012@gmail.com · +91 73518 17506
GitHub · LinkedIn · MIT License