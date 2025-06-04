# 🚀 Azure Data Engineering Project: End-to-End ETL Pipeline

Azure Data Engineering Project: End-to-End ETL Pipeline
This project showcases a modern end-to-end Data Engineering pipeline built on Microsoft Azure, designed to ingest, transform, and serve data for analysis and reporting. The architecture follows the Medallion Architecture (Bronze → Silver → Gold) model, implementing real-world data engineering concepts using the Azure ecosystem.

---

###📌 Project Objective

To build a scalable, secure, and efficient data pipeline that:

Ingests data from external sources
Transforms and cleans the data using PySpark
Stores data in a structured format for analysis
Enables rich visualizations for decision-making

---

###🧱 Architecture Overview
         [External API Source]
                  |
          Azure Data Factory (ADF)
                  |
        Azure Data Lake Storage Gen2
        ┌──────────┬──────────┬──────────┐
     [Bronze Layer][Silver Layer][Gold Layer]
                  |
          Azure Databricks (PySpark)
                  |
        Azure Synapse Analytics (SQL Pools)
                  |
             Power BI Dashboard


###🔧 Tools & Technologies


| Tool                  | Purpose                              |
|-----------------------|--------------------------------------|
| **Azure Data Factory** | Data ingestion from APIs             |
| **Azure Data Lake Gen2** | Scalable cloud storage              |
| **Azure Databricks**   | Data cleaning and transformation     |
| **PySpark**            | Distributed data processing          |
| **Delta Lake**         | Storage layer with ACID compliance   |
| **Azure Synapse Analytics** | Data warehousing and SQL queries  |
| **Power BI**           | Data visualization and reporting     |

---

##🗂️ Project Breakdown


###1️⃣ Data Ingestion (Bronze Layer)
- Extracted data from an external HTTP API using Azure Data Factory.
- Stored raw data in Azure Data Lake Storage Gen2 in a structured folder format.


###2️⃣ Data Transformation (Silver Layer)
- Created a secure connection between Azure Data Lake and Databricks using Microsoft Entra ID (App ID, Secret, Tenant ID).
- Used PySpark to clean, filter, and transform the raw data.
- Implemented **incremental loading** using SCD Type 1 (Upsert logic) for optimized performance.
 

###3️⃣ Data Serving (Gold Layer)
- Loaded transformed data into **Azure Synapse Analytics** using `OPENROWSET()` and **external tables**.
- Enabled fast, structured access for analytical querying.

  
###4️⃣ Reporting and Dashboard
- Connected **Power BI** to Synapse Analytics.
- Built a real-time, interactive dashboard to visualize the final business insights.


###💡 Key Learnings
- Understanding the Medallion Architecture in real-world data workflows.
- Connecting Azure services securely using managed identities and service principals.
- Handling incremental data loads for scalable ETL.
- Query optimization in Synapse using external tables and views.
- Delivering insights through Power BI dashboards.

---

###📸 Project Demo
- [Azure Data Factory Documentation](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Azure Databricks Quickstart](https://learn.microsoft.com/en-us/azure/databricks/)
- [Delta Lake Guide](https://delta.io/)
- [Synapse Analytics Overview](https://learn.microsoft.com/en-us/azure/synapse-analytics/)
- [Power BI Docs](https://learn.microsoft.com/en-us/power-bi/)

---


## 🤝 Acknowledgements

A special thanks to [Ansh Lamba](https://www.linkedin.com/in/anshlamba/) for his guidance and content that inspired this project build.
