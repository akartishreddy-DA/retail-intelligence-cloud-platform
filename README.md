Retail Intelligence Cloud Platform
🚀 Overview

Retail Intelligence Cloud Platform is an end-to-end cloud data warehouse project built on Snowflake.

It simulates how a retail organization designs and automates a modern analytics platform to enable historical tracking, revenue analysis, and executive decision-making.

This project demonstrates real-world data engineering practices including:

Dimensional modeling (Star Schema)

Slowly Changing Dimension (SCD Type 2)

Snowflake Streams & Tasks automation

Fact and dimension layer design

Analytical view creation for BI consumption

🏗 Architecture

Data Flow

Raw Retail Data
→ Snowflake Staging Layer
→ Dimension & Fact Modeling
→ Automated SCD Processing (Stream + Task)
→ Analytics Views
→ Executive-Level Reporting

🧱 Data Warehouse Design
Star Schema Implementation
Fact Table

FACT_SALES

SALE_ID (Surrogate Key)

CUSTOMER_SK (Foreign Key)

SALE_DATE

SALE_AMOUNT

DATE_SK (Date Dimension Key)

Dimension Tables

DIM_CUSTOMER_SCD

Surrogate Key (CUSTOMER_SK)

Business Key (CUSTOMER_ID)

Historical tracking fields

EFFECTIVE_FROM

EFFECTIVE_TO

IS_CURRENT flag

Implements SCD Type 2 for full customer history tracking.

DIM_DATE

Date surrogate key

Year, Month, Quarter

Day of Week

Month Name

🔄 SCD Type 2 Implementation

The customer dimension tracks attribute changes over time using:

Surrogate keys

EFFECTIVE_FROM / EFFECTIVE_TO timestamps

IS_CURRENT flag

Automated change detection via Stream

This enables:

Accurate historical reporting

Customer attribute versioning

Time-aware fact joins

⚙️ Automation (Snowflake Native)

Implemented using Snowflake-native features:

Stream: CUSTOMER_GOLD_STREAM

Task: SCD_CUSTOMER_TASK

The automated task:

Detects changes in source data

Expires previous dimension records

Inserts new versions

Runs on a scheduled basis (CRON-based execution)

This simulates production-grade warehouse automation.

📊 Analytical Views

The following views power reporting and BI tools:

VW_YEARLY_REVENUE

VW_TIME_REVENUE_SUMMARY

VW_REVENUE_BY_REGION

VW_EXECUTIVE_DASHBOARD

VW_FULL_DASHBOARD

These support:

Revenue trend analysis

Regional performance tracking

Order volume monitoring

Average order value calculation

Executive KPI reporting

📂 Project Structure
retail-intelligence-cloud-platform/
│
├── docs/
│   └── retail_intelligence_architecture.drawio
│
├── snowflake_sql/
│   ├── 01_SCD_TYPE2_CUSTOMER.sql
│   ├── 02_SCD_AUTOMATION.sql
│   ├── 03_FACT_LAYER.sql
│   ├── 04_DIM_DATE.sql
│   └── 05_PROJECT_DASHBOARDS.sql
│
├── .gitignore
└── README.md

🛠 Technologies Used

Snowflake

SQL

Dimensional Modeling

Data Warehousing Concepts

SCD Type 2

Streams & Tasks Automation

🎯 Key Learning Outcomes

Designed a complete star schema from scratch

Implemented SCD Type 2 manually and via automation

Built a fact layer with surrogate key joins

Created production-style analytical views

Simulated enterprise-grade warehouse maintenance

👨‍💻 Author

Kartish Reddy Anugu
