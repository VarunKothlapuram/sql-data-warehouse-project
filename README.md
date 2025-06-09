---

#  SQL Data Warehouse Project

### 🎯 End-to-End Data Engineering Using Medallion Architecture

---

## 🚀 Project Overview

This project delivers a complete **end-to-end SQL Data Warehouse solution** using the Medallion Architecture. It emphasizes robust data engineering practices, scalable ETL development, and advanced analytics, ultimately providing high-quality, business-ready data for BI and decision-making.

Simulating a real-world enterprise scenario with CRM and ERP datasets, the project walks through every step of the data pipeline—from raw ingestion to clean, analytical insights delivered through Power BI.

---

## 🔧 Key Components

###  1.Data Integration
---
I explored the data sources to understand their content and interrelationships. Then designed a Data Integration Diagram to visualize the source systems and how they connect, making it easy to grasp the structure at a glance.

![image](https://github.com/user-attachments/assets/e46b6f64-b217-4394-a512-794635bd1fcf)


---

###  2. Data Architecture – Medallion Model

The Data Warehouse is designed using the **Medallion Architecture**, separating data into clearly defined layers for transparency and efficiency:

| Layer  | Purpose                                                               |
| -------| --------------------------------------------------------------------- |
| Bronze | Raw data storage (e.g., ERP/CRM CSV files). Preserves data lineage.   |
| Silver | Cleansed, deduplicated, and standardized data. Structured and usable. |
| Gold   | Star Schema–based analytical model. Optimized for reporting and BI.   |

![image](https://github.com/user-attachments/assets/fe21e514-fa89-47de-b842-6eb1423ae765)

---

###  3. ETL Pipelines

Built using modular SQL scripts, the ETL process extracts, transforms, and loads data through each layer:

* Extract: Load raw CRM and ERP data from CSVs.
* Transform: Cleanse, standardize, and enrich data.
* Load: Move curated data through Bronze → Silver → Gold.

---

###  4. Data Modeling – Star Schema

A well-designed **Star Schema** supports fast and intuitive querying:

| Table           | Description                                                          |
| --------------- | -------------------------------------------------------------------- |
| `fact_sales`    | Central transaction table with sales metrics and foreign keys        |
| `dim_customers` | Customer demographics, regions, and segmentation (VIP, Regular, New) |
| `dim_products`  | Combined product + category metadata                                 |

Relational integrity is maintained with primary/foreign keys for reliable joins and performance.

![image](https://github.com/user-attachments/assets/f35bc20b-4acf-4217-88ab-3fb15fc907b2)


---

###  5. Advanced Analytics & KPIs

Custom analytical views were built in the Gold Layer to support strategic decision-making:

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

### 📈 6. Reporting Readiness (Power BI Integration)

Gold Layer outputs are **dashboard-ready** and structured for seamless reporting:

* ✅ Business-friendly column names
* ✅ Pre-aggregated & validated KPIs
* ✅ Zero need for additional transformations in BI tools

Designed for **low maintenance** and **high scalability**, ensuring quick adoption by reporting teams using Power BI or Tableau.

---

## 📁 Project Structure

Data-Warehouse-Project/
│
├── 0-Datasets/                         # Raw datasets used for the project (ERP and CRM data)
│
├── documents/                        # Project documentation and architecture details
│   ├── data_architecture.png           # Draw.io file shows the project's architecture
│   ├── data_integration.png            # Draw.io file shows how the data files are related
│   ├── data_models.png                 # Draw.io file for data models (star schema)
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── Scripts/                # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── tests/                            # Test scripts and quality files
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository

---

