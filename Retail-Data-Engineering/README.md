# 🚀 Retail Data Engineering Pipeline
---

# 📌 Project Overview

This project demonstrates an end-to-end Azure Data Engineering pipeline that extracts Amazon product data from the SearchAPI REST API, stores raw JSON data in Azure Data Lake Storage, transforms nested JSON using Azure Data Factory Mapping Data Flow, and loads clean data into Azure SQL Database.

The pipeline also includes monitoring and error handling using Azure Data Factory.

---

# 🎯 Project Goal

Build an automated ETL pipeline that:


---

Technology Stack
- Azure SQL Database
- Azure Data Factory (ADF)
- Azure Data Lake Storage Gen2 (ADLS)
- Azure Databricks (PySpark)
- Power BI

---

Dataset



🛠 Technology Stack

Microsoft Fabric OneLake Lakehouse Fabric Pipelines PySpark Delta Tables Power BI DAX GitHub

📂 Dataset

The project uses five datasets.

Dataset Description Customers Customer master information Orders Customer purchase history Payments Payment transactions Support Tickets Customer service records Web Activities Website browsing activity

📁 Project Structure

ecommerce-customer360-fabric/ │ ├── assets/ │ ├── architecture.png │ ├── dashboard.png │ └── pipeline.png │ ├── datasets/ │ ├── customers.parquet │ ├── orders.parquet │ ├── payments.parquet │ ├── support_tickets.parquet │ └── web_activities.parquet │ ├── notebooks/ │ ├── 01_Bronze_Load.ipynb │ ├── 02_Silver_Transformation.ipynb │ ├── 03_Gold_Customer360.ipynb │ └── 04_Data_Validation.ipynb │ ├── powerbi/ │ ├── Customer360.pbip │ └── Dashboard.png │ ├── docs/ │ ├── Architecture.md │ ├── Data_Dictionary.md │ └── Dashboard_Explanation.md │ ├── README.md └── LICENSE

🥉 Bronze Layer The Bronze layer stores raw data exactly as received from the source system.

Activities Read Parquet files Validate schema Store raw data Preserve original records Bronze Tables

Bronze_customers Bronze_orders Bronze_payments Bronze_supporttickets Bronze_web

🥈 Silver Layer

The Silver layer performs data cleaning and transformation.

Transformations include:

Null handling Duplicate removal Standardizing values Data type conversion Date formatting Business rule implementation Derived columns Silver Tables

Silver_customers Silver_orders Silver_payments Silver_supporttickets Silver_web_act

🥇 Gold Layer The Gold layer combines all business entities into a Customer 360 analytical model.

Joined Tables

Customers Orders Payments Support Tickets Web Activities Output Table

gold_customer360 This table is used directly by Power BI.

📊 Power BI Dashboard The dashboard provides a complete business overview.

KPI Cards Total Customers Total Orders Total Revenue Average Order Value Payment Success Rate Support Tickets Interactive Filters Order Date Location Order Status Visualizations Revenue Trend Orders by Status Payment Status Revenue by Location Payment Method Analysis Most Viewed Pages Resolution Status

📈 Key Business Insights

The dashboard helps answer questions such as:

Which locations generate the highest revenue? Which payment methods are most popular? What is the payment success rate? Which customer devices are used the most? Which pages receive the highest traffic? Which support issues occur most frequently? What is the average order value? How many customers placed orders? 📐 Data Engineering Workflow Raw Data

↓

OneLake

↓

Fabric Pipeline

↓

Bronze Layer

↓

Silver Layer

↓

Gold Layer

↓

Power BI Dashboard 📊 DAX Measures Revenue Revenue = SUM(gold_customer360[amount]) Total Customers Total Customers = DISTINCTCOUNT(gold_customer360[customer_id]) Total Orders Total Orders = DISTINCTCOUNT(gold_customer360[order_id]) Average Order Value Average Order Value = AVERAGE(gold_customer360[amount]) Payment Success % Payment Success % = DIVIDE( CALCULATE( COUNTROWS(gold_customer360), gold_customer360[payment_status]="Success" ), COUNTROWS(gold_customer360) ) Support Tickets Support Tickets = DISTINCTCOUNT(gold_customer360[ticket_id])

🚀 Features

End-to-End Data Engineering Project Microsoft Fabric Pipeline Lakehouse Architecture Medallion Architecture PySpark Data Transformation Delta Tables Customer 360 Analytics Power BI Dashboard Interactive Filters Business KPIs

🎓 Skills Demonstrated

Data Engineering Microsoft Fabric Data Pipelines OneLake Lakehouse Delta Lake PySpark Data Transformation Data Cleaning Power BI DAX Data Visualization Business Intelligence


