🍔 Food Delivery Analytics using Databricks Medallion Architecture

📌 Project Overview

This project demonstrates an end-to-end Data Engineering pipeline built using Databricks, PySpark, and Delta Lake by implementing the Medallion Architecture (Bronze → Silver → Gold).

The objective is to ingest messy data from multiple business sources, perform data quality checks and transformations, create analytics-ready tables, and build an interactive dashboard for business users.

🎯 Business Problem

A food delivery company receives data from multiple systems:

Customer Management System (CRM)
Orders & Payment System
Restaurant Partner Management

The exported files contain inconsistent formats, duplicate records, missing values, incorrect data types, invalid values, and incomplete business information.

The goal is to transform these raw datasets into trusted, analytics-ready data for reporting and decision-making.

🛠 Technologies Used
Technology	Purpose
Databricks	Data Engineering Platform
PySpark	Data Processing
Delta Lake	Data Storage
SQL	Data Analysis
Databricks Catalog	Data Management
Lakeview Dashboard	Visualization
GitHub	Version Control
