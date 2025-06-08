# sql-data-warehouse-project
Building a modern Data warehouse with SQL Server, including ETL processes, data modeling, and analytics. 


---
### SQL Data Warehouse Project

End-to-End Data Engineering Project Using Medallion Architecture


Here’s your project description presented in a clean, **structured** and **professional** Markdown format for your GitHub README:

---

# 📦 SQL Data Warehouse Project

### 🎯 End-to-End Data Engineering Using Medallion Architecture

---

## 🚀 Project Overview

This project delivers a complete **end-to-end SQL Data Warehouse solution** using the Medallion Architecture. It emphasizes robust data engineering practices, scalable ETL development, and advanced analytics, ultimately providing high-quality, business-ready data for BI and decision-making.

Simulating a real-world enterprise scenario with CRM and ERP datasets, the project walks through every step of the data pipeline—from raw ingestion to clean, analytical insights delivered through Power BI.

---

## 🔧 Key Components

### 🧱 1. Data Architecture – Medallion Model

The Data Warehouse is designed using the **Medallion Architecture**, separating data into clearly defined layers for transparency and efficiency:

| Layer  | Purpose                                                               |
| -------| --------------------------------------------------------------------- |
| Bronze | Raw data storage (e.g., ERP/CRM CSV files). Preserves data lineage.   |
| Silver | Cleansed, deduplicated, and standardized data. Structured and usable. |
| Gold   | Star Schema–based analytical model. Optimized for reporting and BI.   |

---

### 🔄 2. ETL Pipelines

Built using modular SQL scripts, the ETL process extracts, transforms, and loads data through each layer:

* Extract: Load raw CRM and ERP data from CSVs.
* Transform: Cleanse, standardize, and enrich data.
* Load: Move curated data through Bronze → Silver → Gold.

---

### 🧠 3. Data Modeling – Star Schema

A well-designed **Star Schema** supports fast and intuitive querying:

| Table           | Description                                                          |
| --------------- | -------------------------------------------------------------------- |
| `fact_sales`    | Central transaction table with sales metrics and foreign keys        |
| `dim_customers` | Customer demographics, regions, and segmentation (VIP, Regular, New) |
| `dim_products`  | Combined product + category metadata                                 |

Relational integrity is maintained with primary/foreign keys for reliable joins and performance.

---

### 📊 4. Advanced Analytics & KPIs

Custom **analytical views** were built in the Gold Layer to support strategic decision-making:

#### ✅ Customer-Level KPIs:

* Segmentation: VIP, Regular, New
* Customer lifespan (active months)
* Recency (last purchase period)
* Average Order Value (AOV)
* Total revenue per customer

#### ✅ Product-Level KPIs:

* Performance tiers: High / Mid / Low
* Average monthly revenue & order revenue
* Product lifespan
* Customer count & total sales per product

These insights empower marketing, sales, retention, and inventory decisions.

---

### 📈 5. Reporting Readiness (Power BI Integration)

Gold Layer outputs are **dashboard-ready** and structured for seamless reporting:

* ✅ Business-friendly column names
* ✅ Pre-aggregated & validated KPIs
* ✅ Zero need for additional transformations in BI tools

Designed for **low maintenance** and **high scalability**, ensuring quick adoption by reporting teams using Power BI or Tableau.

---

## 📁 Project Structure

```
SQL-Data-Warehouse-Project/
├── 0-Datasets/             # Raw CSV files (ERP & CRM)
├── 1-Docs/                 # Diagrams & metadata
├── 2-DDL & ETL Scripts/    # Modular ETL scripts (bronze/silver/gold)
├── 3-Tests/                # Data quality and validation scripts
├── 4-Analytics/            # Analytical SQL views & KPIs
├── README.md               # Project documentation
└── LICENSE                 # License information
```

---

