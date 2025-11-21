# 🛒 SynthCart E-Commerce Analytics Platform: Olist & DummyJSON Data Project

An end-to-end data platform built for SynthCart, a rapidly growing American electronics retailer, to transform raw e-commerce data into actionable business intelligence.

---

## 🚀 Project Goal

To establish a **robust, automated, and scalable data pipeline** using the **Medallion Architecture (Bronze -> Silver -> Gold)**, serving a fully functional **Power BI Dashboard** for data-driven decision-making in sales optimization, customer behavior understanding, and inventory management.

---

## 🛠️ Technical Stack

| Category | Tool / Technology | Purpose |
| :--- | :--- | :--- |
| **Data Lake** | **MinIO** | S3-compatible object storage for raw and processed data layers. |
| **Ingestion & Workflow** | **Apache Airflow** | Workflow Orchestration for managing and scheduling the Medallion pipeline DAGs. |
| **Processing** | **Python (PySpark/Pandas)** | Data Cleaning, Transformation, and Enrichment. |
| **Data Warehouse** | **PostgreSQL** | Storage for the final, aggregated Gold Layer tables. |
| **BI & Visualization** | **Power BI** | Business Intelligence dashboarding for executive-level insights. |
| **Version Control** | **GitHub** | Code collaboration, versioning, and CI/CD foundation. |

---

## 📊 Data Architecture (Medallion Layers)

| Layer | Source Data | Transformation Focus | Output Storage | Team |
| :--- | :--- | :--- | :--- | :--- |
| **Bronze** (Raw) | Olist CSVs (Batch) & DummyJSON API (Real-time Simulation) | As-is ingestion; minimal structure applied. | MinIO S3 (Raw Bucket) | DE Team |
| **Silver** (Cleaned) | Bronze Layer | Cleaning, validation, type casting, enrichment (Olist + DummyJSON join). | MinIO S3 (Parquet Format) | DE Team |
| **Gold** (Aggregated) | Silver Layer | Business-level aggregation, creation of **Star Schema** (Fact/Dimension tables). | **PostgreSQL Data Warehouse** | DE Team |

---

## 🎯 Key Deliverables

### Data Engineering (DE) Team
* A complete, automated **Airflow Pipeline** with three dependent DAGs (Bronze $\rightarrow$ Silver $\rightarrow$ Gold).
* Scripts for data ingestion, cleaning, transformation, and loading into PostgreSQL.
* **Star Schema** data model (e.g., `fact_orders`, `dim_customers`, `dim_products`).

### Data Analysis (DA) Team
* A comprehensive **Power BI Dashboard** with **7 pages** of insights covering:
    * Executive Sales Overview
    * Customer Insights
    * Product Performance Analysis
    * Logistics & Fulfillment
    * Seller & Review Analysis [ Saud Ijaz ]
    * Payment Methods Analysis
    * Geographic Deep Dive
* Documentation of the data model and DAX measures.

---

## 🧑‍💻 Team Contribution Snapshot

| Team | Member | Core Responsibility Area |
| :--- | :--- | :--- |
| **Data Engineering** | Muhammad Awais | Infrastructure & Environment Setup (MinIO, PostgreSQL, Airflow) |
| **Data Engineering** | Afnan Khan | Bronze Layer: Raw Data Ingestion (Batch & API) |
| **Data Engineering** | Farheen Muzaffar | Silver Layer: Data Cleaning, Conforming, and Enrichment |
| **Data Engineering** | Ghazal E Ashar | Gold Layer: Aggregation and Loading into PostgreSQL DW |
| **Data Analysis** | **Saud Ijaz** | Dashboard Page: **Seller & Review Analysis** |
| **Data Analysis** | *...and 6 other DA members* | Dashboard Development & Data Exploration |
