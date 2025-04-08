# 🛠️ Databricks Data Engineering Pipeline (Medallion Architecture)

This repository contains a structured data engineering pipeline built in **Databricks**, following the **Medallion Architecture** (Bronze, Silver, Gold layers). The pipeline processes raw data related to customers, products, and transactions and transforms it into business-ready insights, including daily sales reports.

---

## 🏗️ Architecture Overview

### 🔹 Bronze Layer
Raw ingestion of data in its original format from multiple file types:
- **File Formats:** CSV, JSON, Parquet
- **Source Entities:** `customer`, `product`, and `transaction`
- **Operations:** 
  - Load raw data into the Databricks file system
  - Create a **Bronze database**
  - Import raw files as Delta tables in the Bronze layer

### 🔸 Silver Layer
Cleansed, standardized, and enriched data:
- **Transformations:**
  - Casting data types
  - Handling nulls and duplicates
  - Creating relationships via keys
- **Structured into a Silver database** for analytical readiness

### 🟡 Gold Layer
Business-level aggregations and metrics:
- Daily sales summaries
- Daily sales by product category
- Gold tables are optimized for **Power BI reporting**

---

## 📊 Power BI Integration

Gold layer tables are connected to **Power BI** using:
- A **secret access token**
- The **Databricks cluster address**

This allows dynamic, real-time reporting of business metrics directly from Databricks into Power BI dashboards.

---

## 🚀 Getting Started

To run this pipeline in your Databricks workspace:

1. **Clone this repository:**
   ```bash
   git clone https://github.com/bahmangm/databricks-data-engineering-project.git


2. **Upload the notebooks to your Databricks workspace.**

3. **Execute the notebooks in the following order:**

### 🔹 Bronze Layer

- `Bronze_layer_DB_creation.ipynb`
- `Bronze_layer_customer_load.ipynb`
- `Bronze_layer_product_load.ipynb`
- `Bronze_layer_transaction_load.ipynb`

### 🔸 Silver Layer

- `Silver_layer_DB.ipynb`
- `silver_layer_customer_load.ipynb`
- `silver_layer_product_load.ipynb`
- `silver_layer_transactions_load.ipynb`

### 🟡 Gold Layer

- `gold_layer_db.ipynb`
- `gold_layer_daily_sales.ipynb`
- `gold_layer_daily_sales_by_category.ipynb`

---

### 🧰 Technologies Used

- **Databricks** – Unified data analytics platform for big data and AI  
- **Apache Spark** – Distributed data processing engine  
- **Delta Lake** – Storage layer that brings ACID transactions and scalable metadata  
- **PySpark** – Python API for Apache Spark  
- **SQL** – Language for querying and transforming structured data  
- **Power BI** – Business intelligence tool used to visualize and report on Gold layer data  
- **Notebook Interface** – Interactive development and orchestration environment in Databricks  

---

### 📌 Key Concepts

- **Medallion Architecture** – Organizes data pipelines into Bronze (raw), Silver (cleaned), and Gold (aggregated) layers  
- **Multi-format Ingestion** – Supports input files in CSV, JSON, and Parquet formats  
- **Data Transformation** – Cleansing, normalization, type casting, and relationship building  
- **Delta Tables** – Versioned, reliable data storage with ACID guarantees  
- **Notebook Orchestration** – Logical execution of layered notebooks in Databricks  
- **Power BI Integration** – Secure connection of Gold layer tables to Power BI via token and cluster address for real-time analytics  

