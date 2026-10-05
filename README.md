# CadetX: Heavy Supplier, Inventory & Warehouse Analytics

![Status](https://img.shields.io/badge/Status-Week%201%20of%2012-blue)
![Python](https://img.shields.io/badge/Python-3.8+-green)
![SQL](https://img.shields.io/badge/SQL%20Server-T--SQL-orange)
![Power%20BI](https://img.shields.io/badge/Power%20BI-Dashboards-purple)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A **12-week data analytics project** analyzing supply-chain operations for heavy equipment suppliers, optimizing inventory management, warehouse efficiency, and demand forecasting using Python, SQL, and Power BI.

---

## 📊 Dataset Overview

| Metric | Value |
|--------|-------|
| **Time Period** | 2019-01-01 to 2025-03-20 (6+ years) |
| **Total Transactions** | 645,417 |
| **Customers** | 500 across 16 states |
| **Suppliers** | 8 vendors (OEM, Local, Distributor) |
| **Products** | 30 heavy equipment parts |
| **Branches** | 6 warehouses (North, West, South, East) |
| **Data Quality** | 99.6% complete (only 2,370 missing values out of 645K) |

---

## 🏢 Business Context

**Industry:** Heavy Equipment Suppliers (Hydraulics, Engines, Filters, Electrical, Transmission, etc.)

**Customer Base:**
- 500 customers: Retail, Fleet Owners, Government, Dealers, Corporate
- 16 states across India
- 6 industry segments

**Supply Chain Structure:**
- 8 suppliers: OEM, Local Vendors, Distributors
- 6 branch warehouses: North, West, South, East regions
- 30 product categories: Hydraulic, Engine, Filters, Electrical, Transmission, Cooling, Brakes, Seals, Attachments, Sensors, etc.

---

## 📈 Transaction Volume

| Category | Volume | Period |
|----------|--------|--------|
| **Sales Orders** | 20,000 | 2019-01-01 to 2024-12-31 |
| **Invoices** | 18,033 | 2019-01-03 to 2025-01-13 |
| **Purchase Orders** | 24,000 | 2019-01-01 to 2024-12-31 |
| **Purchase Order Lines** | 155,495 | Full period |
| **Sales Order Lines** | 130,402 | Full period |
| **Payments** | 19,257 | 2019-01-09 to 2025-03-20 |
| **Inventory Movements** | 237,230 | 2019-01-01 to 2025-01-28 |

**Key Finding:** 2,370 purchase orders still pending delivery (9.9% of total POs)

---

## 📁 Data Structure

### Master Data Tables

| Table | Rows | Purpose |
|-------|------|---------|
| `branches.csv` | 6 | Warehouse locations (North, West, South, East) |
| `customers.csv` | 500 | Customers (Retail, Fleet, Government, Dealer, Corporate) |
| `products.csv` | 30 | Heavy equipment parts (Hydraulic, Engine, Filters, etc.) |
| `suppliers.csv` | 8 | Vendors (OEM, Local, Distributor) |

### Transactional Data Tables

| Table | Rows | Period | Purpose |
|-------|------|--------|---------|
| `sales_orders_header.csv` | 20,000 | 2019-2024 | Customer orders |
| `sales_orders_lines.csv` | 130,402 | 2019-2024 | Order line items |
| `purchase_orders_header.csv` | 24,000 | 2019-2024 | Supplier POs (2,370 pending) |
| `purchase_orders_lines.csv` | 155,495 | 2019-2024 | PO details |
| `invoices.csv` | 18,033 | 2019-2025 | Customer invoices |
| `payments.csv` | 19,257 | 2019-2025 | Payment records |

### Operations Tables

| Table | Rows | Period | Purpose |
|-------|------|--------|---------|
| `inventory_master.csv` | 180 | Current | Stock levels per product/branch |
| `stock_ledger.csv` | 237,230 | 2019-2025 | IN/OUT/ADJUSTMENT movements |

---

## 🎯 12-Week Roadmap

```
WEEK 1-3: FOUNDATION (Data Cleaning & KPI Design)
  ✅ Load & profile 12 CSV files
  ✅ Data quality assessment (2,370 nulls in PO dates)
  ✅ Create data dictionary
  [ ] Design 20+ KPIs
  [ ] Build data pipeline
  Status: 🔄 IN PROGRESS

WEEK 4-6: CORE ANALYTICS (Product, Warehouse, Supplier)
  [ ] Fast/slow-moving products (30 SKUs to analyze)
  [ ] Warehouse space utilization (6 branches)
  [ ] Supplier reliability (8 vendors, 2,370 pending POs)
  [ ] Inventory turnover (237K movements analyzed)
  Status: ⏳ PLANNED

WEEK 7-9: PREDICTIVE ANALYTICS (Forecasting & Segmentation)
  [ ] Demand forecasting on 20K sales orders
  [ ] Stockout risk prediction
  [ ] Customer segmentation (500 customers, 6 industries)
  [ ] Inventory level forecasting
  Status: ⏳ PLANNED

WEEK 10-12: BI & STRATEGY (Dashboards & Recommendations)
  [ ] Product performance dashboard
  [ ] Inventory health monitor
  [ ] Warehouse efficiency tracker
  [ ] Supplier scorecard
  [ ] Demand forecast dashboard
  Status: ⏳ PLANNED
```

---

## 📊 Core KPIs to Build (20+)

### Product Analytics
- Fast-moving products (top 20% of 30 SKUs)
- Slow-moving & dead stock identification
- Inventory turnover ratio (turnover days)
- Product aging analysis
- ABC/Pareto classification
- Demand seasonality patterns

### Warehouse Operations (6 Branches)
- Space utilization rate (%)
- Throughput by branch (units/week)
- Warehouse efficiency score
- Operational bottleneck detection
- Branch performance benchmarking

### Supplier Performance (8 Vendors)
- On-time delivery rate (vs 2,370 pending)
- Lead time analysis
- Supplier reliability score
- Cost per unit by supplier
- Supplier concentration risk

### Customer Insights (500 Customers)
- Customer segmentation (5 types: Retail, Fleet, Gov, Dealer, Corporate)
- RFM analysis
- Customer lifetime value
- Churn risk prediction
- High-value customer identification

### Financial Metrics
- Inventory carrying cost
- Stockout cost impact
- Payment collection rate (19.2K payments on 18K invoices)
- Working capital efficiency
- Cost reduction opportunities

---

## 🤖 Models to Build

### 1. **Demand Forecasting** (Week 7)
- **Data:** 20,000 sales orders over 6 years
- **Method:** ARIMA / Exponential Smoothing
- **Target:** Product-level monthly demand
- **Accuracy Goal:** MAPE < 15%

### 2. **Stockout Risk Prediction** (Week 8)
- **Data:** 237,230 inventory movements
- **Method:** Logistic Regression / Random Forest
- **Target:** Binary (risk/no risk) for 30 products
- **Precision Goal:** > 85%

### 3. **Customer Segmentation** (Week 9)
- **Data:** 500 customers, RFM metrics
- **Method:** K-Means Clustering
- **Target:** 3-5 customer personas
- **Segments:** Retail, Fleet, Government, Dealer, Corporate

### 4. **Anomaly Detection** (Week 11)
- **Data:** 237K inventory movements
- **Method:** Isolation Forest
- **Target:** Unusual stock patterns
- **Goal:** Early warning system

---

## 📁 Repository Structure

```
cadetx-warehouse-analytics/
├── data/
│   ├── raw/                              # Original 12 CSV files
│   │   ├── branches.csv (6 rows)
│   │   ├── customers.csv (500 rows)
│   │   ├── products.csv (30 rows)
│   │   ├── suppliers.csv (8 rows)
│   │   ├── sales_orders_header.csv (20K rows)
│   │   ├── sales_orders_lines.csv (130K rows)
│   │   ├── purchase_orders_header.csv (24K rows)
│   │   ├── purchase_orders_lines.csv (155K rows)
│   │   ├── invoices.csv (18K rows)
│   │   ├── payments.csv (19K rows)
│   │   ├── inventory_master.csv (180 rows)
│   │   └── stock_ledger.csv (237K rows)
│   └── processed/                        # Cleaned datasets
│       ├── merged_dataset.csv
│       ├── product_metrics.csv
│       └── supplier_metrics.csv
├── notebooks/
│   ├── week-01-eda.ipynb                 # Data exploration (IN PROGRESS)
│   ├── week-02-cleaning.ipynb
│   ├── week-03-kpi-design.ipynb
│   ├── week-04-product-analysis.ipynb
│   └── ...
├── sql/
│   ├── 01-data-integration.sql
│   ├── 02-kpi-queries.sql
│   └── ...
├── dashboards/
│   ├── product-performance.pbix
│   ├── inventory-health.pbix
│   ├── warehouse-efficiency.pbix
│   ├── supplier-scorecard.pbix
│   └── demand-forecast.pbix
├── src/
│   ├── data_loader.py
│   ├── data_cleaning.py
│   ├── forecasting.py
│   └── utils.py
└── README.md
```

---

## 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/HARSHPANDEY9756/cadetx-warehouse-analytics.git

# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn jupyter sqlalchemy

# Load and explore data (Week 1)
jupyter notebook notebooks/week-01-eda.ipynb

# Run data cleaning pipeline
python src/data_cleaning.py

# Execute SQL queries
# sql/01-data-integration.sql
```

---

## 📊 Progress Tracking

```
Week 1 Status: 🔄 IN PROGRESS
├── ✅ Loaded all 12 CSV files (645,417 records)
├── ✅ Identified data quality (99.6% complete)
├── ✅ Mapped relationships between tables
├── ⏳ Data dictionary documentation
└── ⏳ Initial KPI framework

Overall Progress: [████░░░░░░░░░░░░░░] 20%
```

---

## 💡 Key Data Insights

**Pending Deliveries:** 2,370 purchase orders (9.9%) still awaiting delivery — potential supply chain risk

**Customer Distribution:** 500 customers across 5 types and 16 states

**Product Range:** 30 SKUs across 15 categories (Hydraulic, Engine, Filters, Electrical, Transmission, etc.)

**Data Completeness:** Only 2,370 missing values across 645K records = 99.6% quality

**Transaction History:** 6+ years of data (2019-2025) providing strong historical patterns

**Inventory Movement Frequency:** 237,230 transactions = ~1,093 per day average

---

## 🛠️ Tech Stack

| Component | Tools |
|-----------|-------|
| **Data Processing** | Python 3.8+, Pandas, NumPy |
| **Analysis** | Scikit-learn, Statsmodels |
| **Querying** | SQL Server, T-SQL |
| **Visualization** | Matplotlib, Seaborn, Power BI |
| **Notebooks** | Jupyter, Google Colab |
| **Version Control** | GitHub |

---

## 📋 Deliverables Checklist

**Analyses (20+):**
- [ ] Product performance ranking
- [ ] Fast/slow-moving identification
- [ ] Warehouse efficiency by branch
- [ ] Supplier reliability scoring
- [ ] Customer segmentation
- [ ] Demand pattern analysis
- [ ] Stockout risk modeling
- [ ] Inventory optimization
- [ ] Cost reduction opportunities
- [ ] Payment collection analysis

**Dashboards (5):**
- [ ] Product Performance Dashboard
- [ ] Inventory Health Monitor
- [ ] Warehouse Efficiency Tracker
- [ ] Supplier Scorecard
- [ ] Demand Forecast & Alerts

**Documentation:**
- [ ] Data Dictionary (field mappings)
- [ ] Methodology Document
- [ ] KPI Framework
- [ ] Strategic Recommendations

---

## 👤 Author

**Harsh Pandey** — Data Analyst  
📧 harshpandey6012@gmail.com | 📱 +91 73518 17506  
🔗 [GitHub](https://github.com/HARSHPANDEY9756) | [LinkedIn](https://linkedin.com/in/harshpandey)

---

## 📜 License

MIT License — See [LICENSE](LICENSE) file for details.

---

**Last Updated:** Week 1, Oct 2026 | **Status:** Data Exploration In Progress | **Next Update:** End of Week 1
