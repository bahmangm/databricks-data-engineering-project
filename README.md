# 🛠️ Databricks Data Engineering Pipeline (Medallion Architecture)

This repository contains a structured data engineering pipeline built in **Databricks**, following the **Medallion Architecture** (Bronze, Silver, Gold layers). The pipeline processes and transforms raw data related to customers, products, and transactions into meaningful daily sales insights.

---

## 🏗️ Architecture Overview

### 🔹 Bronze Layer
Raw ingestion of data in its original format. It includes:
- `customer`, `product`, and `transaction` data.

### 🔸 Silver Layer
Cleansed, normalized, and enriched data. Typical transformations include:
- Data type casting
- Handling missing or duplicate records
- Creating relationships between tables

### 🟡 Gold Layer
Business-level aggregations and insights. In this project:
- Daily sales metrics
- Daily sales by product category

---

## 🚀 Getting Started

To use this pipeline in your Databricks workspace:

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/databricks-medallion-pipeline.git
## 🚀 Getting Started

To use this pipeline in your Databricks workspace:

1. **Upload the notebooks to your Databricks workspace.**

2. **Execute the notebooks in the following order:**

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

## 🧰 Technologies Used

- **Databricks** – Unified data analytics platform
- **Apache Spark** – Distributed processing engine for big data
- **Delta Lake** – Storage layer providing ACID transactions and scalable metadata
- **PySpark** – Python API for Spark
- **SQL** – Used for querying and managing structured data
- **Notebook Interface** – Interactive development and execution environment

---

## 📌 Key Concepts

- **Medallion Architecture** – Organizing data pipelines into Bronze, Silver, and Gold layers
- **Data Ingestion** – Loading raw data into the Bronze layer
- **Data Cleansing & Transformation** – Standardizing and enriching data in the Silver layer
- **Data Aggregation** – Creating business-level summaries in the Gold layer
- **Delta Tables** – Versioned and reliable data storage with ACID guarantees
- **Notebook Orchestration** – Logical execution of notebooks in a layered order
