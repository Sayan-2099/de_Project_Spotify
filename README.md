# End-to-End Azure Data Engineering Project
Project Overview

This project demonstrates an end-to-end Big Data Engineering pipeline built on Microsoft Azure using Databricks and Medallion Architecture (Bronze → Silver → Gold). The goal is to ingest raw data, process it reliably at scale, and produce analytics-ready datasets following industry best practices.

The implementation focuses on production-grade data engineering concepts such as orchestration, scalable transformations, ACID-compliant storage, and reusable analytics logic.

🏗️ Architecture Overview

The pipeline follows the Medallion Architecture pattern:

Bronze Layer: Raw data ingestion from source systems

Silver Layer: Data cleansing, standardization, and enrichment

Gold Layer: Aggregated, business-ready datasets for analytics

High-level flow:

Data Sources → Azure Data Factory → Azure Data Lake Gen2 → Azure Databricks → Bronze / Silver / Gold (Delta Tables)

🛠️ Tech Stack

Azure Data Factory – Data ingestion & orchestration

Azure Data Lake Storage Gen2 – Centralized data storage

Azure Databricks – Distributed data processing using PySpark

Delta Lake – ACID transactions, schema enforcement & versioning

Jinja – SQL templating for dynamic and reusable Gold-layer queries

🔄 Data Pipeline Breakdown
🔹 Bronze Layer

Ingests raw data from source systems

Stores data as Delta tables without heavy transformations

Acts as a historical, immutable data source

🔹 Silver Layer

Cleanses and standardizes data

Handles schema evolution and data quality checks

Produces refined datasets for downstream consumption

🔹 Gold Layer

Creates aggregated and analytics-ready datasets

Uses Jinja templating to parameterize SQL queries

Enables reusable and flexible analytical logic
