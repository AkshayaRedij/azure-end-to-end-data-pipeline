# 🎵 Azure End-to-End Spotify Data Engineering Pipeline

## 📌 Project Overview

This project demonstrates an end-to-end Azure Data Engineering pipeline that ingests Spotify data from Azure SQL Database, processes it using Azure Databricks, and stores curated data using the Medallion Architecture (Bronze, Silver, Gold).

The solution uses Azure Data Factory for orchestration, Azure Data Lake Storage Gen2 for storage, Azure Databricks with PySpark for transformations, Unity Catalog for governance, and Delta Live Tables (DLT) with Change Data Capture (CDC) for incremental processing.

---

## 🏗️ Architecture

<img width="1681" height="936" alt="ChatGPT Image Aug 4, 2026, 08_15_08 PM" src="https://github.com/user-attachments/assets/9672fc29-c22b-42d5-9e39-5da635644118" />



---

## 🚀 Tech Stack

| Service | Purpose |
|----------|----------|
| Azure SQL Database | Source System |
| Azure Data Factory | Data Ingestion & Orchestration |
| Azure Data Lake Storage Gen2 | Data Lake |
| Azure Databricks | Data Processing |
| PySpark | Data Transformation |
| Delta Lake | ACID Storage |
| Unity Catalog | Governance |
| Delta Live Tables | Streaming Pipeline |
| Auto Loader | Incremental File Processing |
| Change Data Capture (CDC) | Incremental Loading |
| Git & GitHub | Version Control |

---

# 📂 Project Structure

```text
azureproject
│
├── adf/
├── databricks/
├── architecture/
├── images/
└── docs/
```

---

# 🔄 Pipeline Workflow

```text
Azure SQL Database
        │
        ▼
Azure Data Factory
        │
        ▼
Azure Data Lake Bronze
        │
        ▼
Azure Databricks Auto Loader
        │
        ▼
Silver Layer
        │
        ▼
Delta Live Tables
        │
        ▼
Gold Layer
```

---

# 🥉 Bronze Layer

- Incremental ingestion
- Auto Loader
- Streaming reads
- Schema inference
- Checkpointing

---

# 🥈 Silver Layer

- Data cleansing
- Duplicate removal
- Standardization
- Data quality improvements
- Delta Tables

---

# 🥇 Gold Layer

- Delta Live Tables (DLT)
- Change Data Capture (CDC)
- Slowly Changing Dimension (SCD Type 2)
- Business-ready tables

---

# 📸 Project Screenshots

## Azure Data Factory Pipeline

<img width="1801" height="629" alt="Incremental_Injestion_adf_pipeline" src="https://github.com/user-attachments/assets/800e6e69-2b08-4f5e-b733-26f135e2d0d4" />
<img width="1540" height="630" alt="IncrementalLoop_adf_pipeline" src="https://github.com/user-attachments/assets/d54529cb-8d0a-4bd2-a4bd-d055873200f5" />
Orchestrates incremental data ingestion from Azure SQL Database to Azure Data Lake Storage.


---

## Azure Data Lake Containers

<img width="1640" height="570" alt="ADLS_Containers" src="https://github.com/user-attachments/assets/295d63e7-b995-4559-998b-3065683b8147" />
Implements Medallion Architecture using Bronze, Silver, and Gold containers.

---

## Databricks Workspace

<img width="1649" height="771" alt="Databricks Workspace" src="https://github.com/user-attachments/assets/f6c34d41-bb7d-4ce2-87ee-51fb37279cf3" />
Development environment used to build and manage notebooks, reusable modules, and Delta Live Tables transformations.

---

## External Locations

<img width="1666" height="541" alt="External_Locations" src="https://github.com/user-attachments/assets/09ba5224-7ed4-4df8-babc-0d2582bc30f2" />
Maps ADLS containers as external storage locations for Unity Catalog.

---

## Storage Credential

<img width="1658" height="435" alt="Storage_Credential" src="https://github.com/user-attachments/assets/7472b401-0425-4013-aa98-dc546eac4888" />
Securely authenticates Azure Databricks with Azure Data Lake Storage using Managed Identity.

---

## Unity Catalog

<img width="734" height="710" alt="Unity_Catalog" src="https://github.com/user-attachments/assets/925ccdf5-85ee-441d-b281-d4cea62ce710" />
Centralized governance layer for managing catalogs, schemas, permissions, and Delta tables.

---

## Delta Tables

<img width="1627" height="780" alt="Delta_Tables" src="https://github.com/user-attachments/assets/8d885cb1-b8cd-4d45-96a6-eade41951047" />
Stores curated datasets optimized for analytics and reporting.

---

## Bronze Layer – Auto Loader

<img width="1202" height="692" alt="Bronze Layer_Autoloader" src="https://github.com/user-attachments/assets/d33aaca1-b383-4c36-9dce-3826cd387981" />
Ingests raw Parquet files into the Bronze layer using Databricks Auto Loader.

---

## Silver Layer – Transformations

<img width="1201" height="766" alt="Silver Layer_Transformations" src="https://github.com/user-attachments/assets/1e1fca72-722f-4740-a3f8-610d1ee7cddd" />
Transforms raw data into clean and standardized Delta tables.

---

## Silver Layer – Delta Write

<img width="1155" height="287" alt="Checkpoint   Delta Write" src="https://github.com/user-attachments/assets/41bc0028-9688-405d-9bda-73b968a45bbb" />
Processes streaming data from Bronze to Silver with fault-tolerant checkpointing.

---

## Gold Layer – Delta Live Tables

<img width="1663" height="817" alt="Gold Layer (DLT_  CDC)" src="https://github.com/user-attachments/assets/0fe7838a-a545-4442-b407-4784db80380e" />
Creates curated business-ready tables using Delta Live Tables and Change Data Capture (CDC).

---

# 🎯 Features

- End-to-End Azure Data Pipeline
- Incremental Data Loading
- Streaming Data Processing
- Medallion Architecture
- Unity Catalog
- External Locations
- Storage Credentials
- Auto Loader
- Delta Lake
- Delta Live Tables
- CDC Pipeline
- SCD Type 2 Implementation

---

# 👤 Author

**Akshaya Redij**

Aspiring Azure Data Engineer
