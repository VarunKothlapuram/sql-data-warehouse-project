# sql-data-warehouse-project
Building a modern Data warehouse with SQL Server, including ETL processes, data modeling, and analytics. 


---
### SQL Data Warehouse Project

End-to-End Data Engineering Project Using Medallion Architecture


##🚀 Project Overview

This project delivers a complete end-to-end SQL Data Warehouse solution using the Medallion Architecture. It focuses on strong data engineering practices, scalable ETL development, and advanced analytics, ultimately providing high-quality data and insights for business intelligence and reporting.

The solution simulates a real-world enterprise scenario involving CRM and ERP datasets and showcases how to ingest, process, model, and analyze data across different stages — from raw ingestion to business-ready outputs.

##🔧 Key Components:

🧱 1. Data Architecture (Medallion Architecture)
The warehouse follows the Medallion Architecture pattern, dividing the system into three layers:

Bronze Layer (Raw Layer)
Stores raw data as-is from the source systems (e.g., CSV files). This layer serves as a historical archive and ensures traceability and auditability.

Silver Layer (Cleaned/Refined Layer)
Includes data that has been cleansed, deduplicated, standardized, and transformed into a more structured format, preparing it for downstream use.

Gold Layer (Business/Analytics Layer)
Contains business-ready tables modeled using a Star Schema. These tables are optimized for analysis, reporting, and consumption in BI tools like Power BI.

🔄 2. ETL Pipelines
Modular ETL (Extract, Transform, Load) pipelines were built using SQL to:

Extract data from ERP and CRM CSV files.

Perform data quality checks, cleansing, and standardization.

Load transformed data into respective layers (Bronze → Silver → Gold).

The scripts are structured into directories:
/bronze, /silver, and /gold for traceable and reusable development.

3. Data Modeling (Star Schema)
To support fast, intuitive querying and reporting, a Star Schema was developed in the Gold Layer:

Fact Table:

fact_sales: Central transaction table containing sales metrics.

Dimension Tables:

dim_customers: Contains customer demographics, location, and segmentation.

dim_products: Merges product information with category metadata.

All tables include primary and foreign key relationships for optimized joins and clarity.

📊 4. Advanced Analytics & KPIs
Several analytical SQL views were developed to surface actionable business insights. These views support:

✅ Customer-Level Analytics:
Customer segmentation (VIP, Regular, New)

Customer lifespan (active months)

Recency (last purchase)

Average order value

Total revenue per customer

✅ Product-Level Analytics:
Product segmentation (High, Mid, Low performers)

Average monthly revenue

Average order revenue

Product lifespan

Total customers and sales per product

These KPIs enable strategic decisions in marketing, retention, product development, and supply chain management.

📈 5. Reporting Readiness (Power BI Integration)
The final views from the Gold Layer are fully optimized for consumption in tools like Power BI or Tableau:

No additional transformation is needed at the dashboard level.

Business-friendly naming conventions and pre-computed metrics ensure accuracy and clarity.

Ensures scalability and minimal maintenance effort for reporting teams.

