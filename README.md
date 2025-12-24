# enterprise-sales-intelligence-genai

⸻

End-to-End Sales Data Engineering & Analytics Platform

📌 Project Overview

This project demonstrates an end-to-end data engineering pipeline for sales analytics using Databricks Community Edition, Apache Spark, Delta Lake, and SQL-based BI dashboards, extended with GenAI-driven business insights.

The pipeline follows industry-standard Medallion Architecture (Bronze → Silver → Gold) to ingest raw sales data, clean and transform it, compute business KPIs, and visualize insights for stakeholders.

⸻

🏗️ Architecture Overview

Medallion Architecture:

Raw CSV Data
     ↓
Bronze Layer (Raw Ingestion)
     ↓
Silver Layer (Cleaned & Enriched Data)
     ↓
Gold Layer (Business KPIs)
     ↓
BI Dashboard & GenAI Insights


🧱 Data Layers Explained

🔹 Bronze Layer
	•	Raw sales CSV ingested as Delta tables
	•	No transformations
	•	Added metadata columns:
	•	ingestion_timestamp
	•	data_source

Purpose: Preserve raw data for audit and reprocessing.

⸻

🔹 Silver Layer
	•	Cleaned and structured data
	•	Removed nulls and invalid records
	•	Correct data types applied
	•	Derived columns (e.g., order date, revenue)

Purpose: Create reliable, analytics-ready data.

⸻

🔹 Gold Layer

Business-ready aggregated tables:
	•	Daily revenue KPIs
	•	Customer-level KPIs
	•	Product performance KPIs
	•	Country-wise revenue metrics

Purpose: Directly consumed by BI tools and decision makers.

⸻

📊 Key Business KPIs
	•	Total Revenue
	•	Total Orders
	•	Average Order Value (AOV)
	•	Daily Revenue Trend
	•	Top Products by Revenue
	•	Customer Revenue Contribution
	•	Country-wise Sales Performance

⸻

📈 BI Dashboard

Built using Databricks SQL Dashboard:
	•	KPI cards for executive overview
	•	Line charts for revenue trends
	•	Bar charts for product & country performance

This enables self-service analytics for business users.

⸻

🤖 GenAI Integration

GenAI is used to:
	•	Convert KPI outputs into executive-level summaries
	•	Generate natural language business insights
	•	Support decision-making using structured sales data

Technologies:
	•	HuggingFace LLM
	•	Python-based prompt engineering


🛠️ Tech Stack


Category
Tools
Data Processing
Apache Spark (PySpark)
Storage
Delta Lake
Platform
Databricks Community Edition
Querying
Spark SQL
BI
Databricks SQL Dashboard
GenAI
HuggingFace Transformers
Language
Python, SQL


📂 Project Structure


sales-data-engineering/
│
├── notebooks/
│   ├── 01_bronze_ingestion.ipynb
│   ├── 02_silver_transformation.ipynb
│   ├── 03_gold_kpis.ipynb
│   ├── 04_genai_insights.ipynb
│
├── dashboards/
│   └── sales_bi_dashboard_screenshots/
│
├── data/
│   └── sample_sales.csv
│
├── architecture/
│   └── architecture_diagram.png
│
└── README.md


🚀 Future Enhancements
	•	Incremental ingestion using Auto Loader
	•	Unity Catalog integration (enterprise setup)
	•	Power BI / Tableau integration
	•	RAG-based GenAI using LangChain
	•	Orchestration using Airflow

⸻

🎯 Key Learnings
	•	Designed scalable medallion architecture
	•	Hands-on Delta Lake operations
	•	KPI modeling for analytics
	•	Real-world BI dashboard creation
	•	Applied GenAI for business summarization

⸻

📌 Author

Ayush Khandelwal
Aspiring Data Engineer | Data Analytics | Spark | SQL | GenAI
