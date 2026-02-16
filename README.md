# Retail Analytics Cloud Pipeline

## 📌 Project Overview

An end-to-end cloud data analytics pipeline built using:

- Snowflake (Data Warehouse)
- dbt (Transformations)
- Airflow (Orchestration)
- SQL (Star Schema + SCD Type 2)
- BI Views for Executive Reporting

This project simulates a real-world retail analytics architecture from raw ingestion to executive dashboards.

---

## 🏗 Architecture

Raw Data → Staging → SCD Type 2 Dimensions → Fact Table → Analytical Views → Dashboards

### Layers Implemented

### 🥉 Bronze Layer
- Raw customer data
- Cleaned staging table

### 🥈 Silver Layer
- SCD Type 2 Customer Dimension
- Automated via Streams & Tasks
- Surrogate key management

### 🥇 Gold Layer
- Sales Fact Table
- Date Dimension
- Revenue by Region
- Executive Dashboard Views

---

## ⚙️ Key Data Engineering Concepts Implemented

- Slowly Changing Dimensions (Type 2)
- Surrogate Keys
- Star Schema Modeling
- Snowflake Streams
- Snowflake Tasks
- Fact-Dimension Relationships
- Foreign Key Constraints
- Analytical View Creation

---

## 📊 Analytical Views Created

- VW_YEARLY_REVENUE
- VW_TIME_REVENUE_SUMMARY
- VW_REVENUE_BY_REGION
- VW_EXECUTIVE_DASHBOARD
- VW_FULL_DASHBOARD

---

## 📈 Example Insights

- Revenue by Region
- Monthly Sales Performance
- Average Order Value
- Total Customers
- Regional Revenue Trends

---

## 🚀 How to Run Snowflake Layer

Execute SQL files in this order:

1. 04_SCD_TYPE2_CUSTOMER.sql
2. 05_SCD_AUTOMATION.sql
3. 06_FACT_LAYER.sql
4. 07_DIM_DATE.sql
5. 99_PROJECT_FINAL.sql

---

## 🎯 What This Project Demonstrates

✔ Real-world warehouse design  
✔ Automation using Streams & Tasks  
✔ Star schema implementation  
✔ End-to-end analytical pipeline  
✔ Executive-level data mart creation  

---

## 👨‍💻 Author
Kartish Reddy
