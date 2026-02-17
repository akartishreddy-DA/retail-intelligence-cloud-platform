# Retail Intelligence Cloud Platform

## 📌 Project Overview

Retail Intelligence Cloud Platform is an end-to-end retail analytics solution built on Snowflake.  

This project simulates how a retail organization designs a cloud-based data warehouse to support executive decision-making, historical tracking, and performance analytics.

It demonstrates modern data engineering practices including dimensional modeling, SCD Type 2 implementation, automated warehouse updates, and executive-level reporting.

---
## Architecture

![Architecture Diagram](docs/architecture_diagram.png)

### Data Flow

Raw Retail Data  
→ Snowflake Staging Layer  
→ Star Schema (Fact & Dimensions)  
→ Automated SCD Processing  
→ Analytical Views  
→ Executive Dashboard  

---

## 🧱 Data Warehouse Design

### Star Schema Implementation

### Fact Table
- **FACT_SALES**
  - Sale ID
  - Customer Surrogate Key
  - Sale Date
  - Sale Amount

### Dimension Tables
- **DIM_CUSTOMER_SCD** (Slowly Changing Dimension Type 2)
- **DIM_DATE**

---

## 🔄 SCD Type 2 Implementation

The customer dimension tracks historical changes using:

- EFFECTIVE_FROM
- EFFECTIVE_TO
- IS_CURRENT flag
- Surrogate Key (CUSTOMER_SK)

This enables full historical reporting and customer attribute versioning.

---

## ⚙️ Automation (Snowflake Native)

Implemented using:

- **Stream** → `CUSTOMER_GOLD_STREAM`
- **Task** → `SCD_CUSTOMER_TASK`

The task automatically:
- Detects changes in customer data
- Closes previous records
- Inserts new versions

This simulates production-grade automated warehouse maintenance.

---

## 📊 Analytical Views

The following views power executive reporting:

- `VW_YEARLY_REVENUE`
- `VW_TIME_REVENUE_SUMMARY`
- `VW_REVENUE_BY_REGION`
- `VW_EXECUTIVE_DASHBOARD`
- `VW_FULL_DASHBOARD`

These provide:

- Revenue by year and month
- Regional sales performance
- Order volume analysis
- Average order value
- Customer metrics

---

## 📂 Project Structure


---

## 👨‍💻 Author
Kartish Reddy Anugu
