# **  Bike Data Lakehouse Project**

## Overview
This project implements a **Data Lakehouse** using **Databricks**, **Delta Lake**, and the **Medallion Architecture (Bronze, Silver, Gold)**.
Raw CSV data is ingested, cleaned, transformed, and modeled into **analytics-ready datasets**, following modern data engineering best practices.

## Architecture
The project follows the Medallion Architecture:

- **Bronze**: Raw data ingestion (no transformations)
- **Silver**: Data cleaning, validation, and standardization
- **Gold**: Business-ready fact and dimension tables (star schema)

**Technologies**
- Databricks
- Delta Lake
- Unity Catalog
- PySpark & Spark SQL
- Databricks Jobs

**Architecture**

Data Sources (CSV files)
        ↓
Bronze Layer (Unity Catalog)
  - Schema: bronze
  - Volume: raw_sources
  - Tables: raw_*
        ↓
Silver Layer
  - Schema: silver
  - Cleaned & conformed tables
        ↓
Gold Layer
  - Schema: gold
  - Aggregated tables / dashboards


### Data Pipeline

- Ingest raw CSV files into Bronze Delta tables
- Clean and validate data in the Silver layer
- Build dimensional models in the Gold layer
- Orchestrate end-to-end execution using Databricks Jobs

**Credits**

This project is inspired by  Databricks learning project from Baraa Projects.
All credit for the original project concept and guidance goes to Baraa Projects.
[https://github.com/DataWithBaraa/databricks_bootcamp_2026](url)