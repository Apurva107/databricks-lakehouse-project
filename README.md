# End-to-End Data Lakehouse Implementation | Azure Databricks

## 📌 Project Overview
This project involves building a production-grade **Data Lakehouse** from scratch using **Azure Databricks**. Following the **Medallion Architecture**, the pipeline ingests raw datasets and systematically transforms them through Bronze, Silver, and Gold layers to create a reliable, high-performance data platform for business intelligence.



## 🛠️ Tech Stack
* **Platform:** Databricks
* **Data Governance:** Unity Catalog
* **Storage Format:** Delta Lake
* **Languages:** PySpark (Spark Python), Spark SQL
* **Orchestration:** Databricks Jobs & Workflows
* **Version Control:** Git (GitHub Integration)

---

## 🏗️ Architecture & Project Phases

### Phase 1: Project Initialization & Governance
* **Infrastructure:** Defined the environment architecture and connected GitHub for version control.
* **Governance:** Established **Unity Catalog** hierarchies including Bronze, Silver, and Gold schemas.
* **Storage:** Created Bronze Volumes for raw source landing and managed the ingestion of initial CSV datasets.

### Phase 2: Bronze Layer (Raw Ingestion)
* **Ingestion:** Developed automated notebooks to load raw CSV files into **Delta tables**.
* **Traceability:** Implemented source-system prefixing (e.g., `erp_`, `crm_`) to maintain clear data lineage.
* **Persistence:** Ensured full data capture in the Bronze layer to allow for historical reprocessing.

### Phase 3: Silver Layer (Data Cleansing & Refinement)
* **Data Quality:** Performed deduplication and handled null/missing values across all datasets.
* **Standardization:** Normalized date formats, string values (trimming/casing), and numeric types.
* **Integrity:** Standardized business keys to ensure seamless relational joins between disparate tables.
* **Documentation:** Added inline documentation and logic checks to ensure transformation transparency.

### Phase 4: Gold Layer (Dimensional Modeling)
* **Modeling:** Designed a **Star Schema** to transition from source-aligned data to business-ready entities.
* **Logic:** Built Dimension tables (`dim_`) and Fact tables (`fact_`) using optimized Spark SQL joins.
* **Usability:** Enriched Unity Catalog metadata with table/column descriptions and defined Primary/Foreign key relationships for downstream BI tools.



### Phase 5: Pipeline Orchestration & Automation
* **Workflow:** Created orchestration notebooks to manage the execution flow across all layers.
* **Automation:** Configured a **Databricks Job** to trigger the end-to-end pipeline.
* **Monitoring:** Established a daily schedule with integrated logging to track job status and performance.

---

## 🚀 Key Features
* **Medallion Design Pattern:** Ensures data quality increases as it moves through the layers.
* **Unity Catalog Integration:** Provides centralized access control and data lineage.
* **Production-Ready Automation:** Fully hands-off processing from raw file upload to final analytical table.

---
