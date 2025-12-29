Enterprise Sales Intelligence & GenAI Reporting Platform
📌 Project Overview

This project implements an end-to-end sales data engineering and analytics platform using Databricks Community Edition, Apache Spark, and Delta Lake, extended with a GenAI-powered executive reporting layer.

The solution follows the industry-standard Medallion Architecture (Bronze → Silver → Gold) to ingest raw transactional data, clean and transform it, compute business KPIs, and generate both BI dashboards and natural language business summaries for decision-makers.

🏗️ Architecture Overview

Medallion Architecture Flow

Raw CSV Data
   ↓
Bronze Layer (Raw Ingestion)
   ↓
Silver Layer (Cleaned & Standardized)
   ↓
Gold Layer (Business KPIs)
   ↓
BI Dashboards & GenAI Insights

🧱 Data Layers
🔹 Bronze Layer

Raw CSV data ingested into Delta tables

No business transformations applied

Metadata added:

ingestion_timestamp

data_source

Purpose: Preserve raw data for auditability and reprocessing.

🔹 Silver Layer

Data cleaned and standardized using PySpark

Invalid and cancelled records removed

Data types enforced

Deduplication applied

Purpose: Create reliable, analytics-ready datasets.

🔹 Gold Layer

Business-ready aggregated tables created using Spark SQL:

Daily revenue KPIs

Customer-level metrics

Country-wise sales performance

Purpose: Direct consumption by BI dashboards and GenAI modules.

📊 Key Business KPIs

Total Revenue

Total Orders

Average Order Value (AOV)

Daily Revenue Trend

Customer Revenue Contribution

Country-wise Sales Performance

📈 BI Dashboard

Built using Databricks SQL Dashboards, including:

KPI cards for executive overview

Line charts for revenue trends

Bar charts for country and customer performance

This enables self-service analytics for business users.

🤖 GenAI Integration

A GenAI layer is integrated to:
Convert structured KPI tables into natural language summaries

Generate executive-level business insights

Support data-driven decision making

Approach:

Gold KPIs converted into structured text prompts

Hugging Face LLM used for summary generation

Python-based prompt engineering


🛠️ Tech Stack
Category	Tools
Data Processing	Apache Spark (PySpark, Spark SQL)
Storage	Delta Lake
Platform	Databricks Community Edition
BI	Databricks SQL Dashboard
GenAI	Hugging Face Transformers
Language	Python, SQL


📂 Project Structure
enterprise-sales-intelligence-genai/
│
├── notebooks/
│   ├── 01_bronze_ingestion.ipynb
│   ├── 02_silver_transformation.ipynb
│   ├── 03_gold_kpis.ipynb
│   ├── 04_genai_insights.ipynb
│
├── dashboards/
│   └── bi_dashboard_screenshots/
│
├── architecture/
│   └── architecture_diagram.png
│
└── README.md

🚀 Future Enhancements

Incremental ingestion pipelines

Orchestration using Airflow

RAG-based GenAI using LangChain

External BI tools (Power BI / Tableau)

Enterprise governance using Unity Catalog

🎯 Key Learnings

Designed scalable Medallion architecture

Hands-on experience with Delta Lake

Advanced KPI modeling using Spark SQL

BI dashboard development

Practical application of GenAI for business insights

📌 Author

Ayush Khandelwal
Aspiring Data Engineer | Spark | SQL | Analytics | GenAI
