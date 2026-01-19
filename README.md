# Azure Databricks Medallion Architecture Project

This repository contains an **Azure Databricks project** implementing **Slowly Changing Dimensions (SCD1 & SCD2)** on a **Medallion Architecture** (Bronze → Silver → Gold).  
It demonstrates real-world ETL workflows using Databricks notebooks, Delta Lake tables, and modular pipelines.

---

## 🛠️ Tech Stack
- **Azure Databricks** – Data engineering and transformation  
- **Delta Lake** – ACID-compliant storage for SCD management  
- **Azure Data Lake Storage (ADLS Gen2)** – Raw, curated, and gold data storage  
- **Python / PySpark** – Transformation logic  
- **GitHub / Azure DevOps** – Version control and collaboration  

---

## 📁 Repository Structure

ADB_REPO/
├── notebooks/ # Databricks notebooks for SCD1 and SCD2 logic
│ ├── bronze_ingest.py # Load raw/source data into Bronze layer
│ ├── silver_transform_scd1.py # SCD1 transformations for Silver layer
│ └── silver_transform_scd2.py # SCD2 transformations for Silver layer
├── delta_tables/ # Delta table definitions for each layer
├── scripts/ # Utility scripts (helpers, UDFs)
├── configs/ # Configurations, paths, and parameters
├── README.md # This file
└── requirements.txt # Python dependencies


---

## 🚀 Project Overview

This project implements a **Medallion Architecture** for structured data pipelines:

1. **Bronze Layer** – Raw ingestion from source systems  
2. **Silver Layer** – Cleaned and transformed data; implements **SCD1 & SCD2** logic  
   - **SCD1:** Overwrite existing records with updated attributes  
   - **SCD2:** Track historical changes by creating new versions of records  
3. **Gold Layer** – Aggregated and analytics-ready datasets for reporting/BI  

**Highlights:**
- Modular Databricks notebooks for reusability  
- Delta Lake for ACID transactions and versioning  
- Parameterized pipelines for easy configuration  
- CI/CD-ready through GitHub integration  

---

## 📌 How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/pranavprasanth14/ADB_REPO.git


💡 Author

Pranav Prasanth – Azure Data Engineering & Databricks enthusiast, passionate about building scalable, production-grade cloud data solutions.

#AzureDatabricks #SCD1 #SCD2 #MedallionArchitecture #DeltaLake #DataEngineering #Python #PySpark
