# Ecommerce-sales-report
## Overview

This project implements an end-to-end Ecommerce reporting pipeline that ingests data from AWS, processes it using a medallion architecture (Bronze, Silver), and produces curated reporting tables for analytics and business insights.
## Data Source

The data for this project is sourced from AWS services:

- **Cloud Provider:** Amazon Web Services (AWS)
- **Storage:** Amazon S3
- **Data Type:** Streaming / Incremental data
- **Domains:**
  - Customer details
  - Product details
  - Sales transactions
  - Seller information

## Data Source

The data for this project is sourced from AWS services:

- **Cloud Provider:** Amazon Web Services (AWS)
- **Storage:** Amazon S3
- **Data Type:** Streaming / Incremental data
- **Domains:**
  - Customer details
  - Product details
  - Sales transactions
  - Seller information
    
## Pipeline Architecture

The pipeline follows a layered data architecture:

- **Bronze Layer:** Raw data ingestion from AWS
- **Silver Layer:** Cleansed and standardized datasets
- **Gold Layer:** Materialized views for reporting and analytics



<img width="1574" height="766" alt="image" src="https://github.com/user-attachments/assets/41b911dc-b3c5-44cd-a5b0-3a96fb487bd4" />

<## Pipeline Components

- **Job Orchestration:** Databricks Jobs
- **Pipelines:** Delta Live Tables (DLT)
- **Processing Engine:** Apache Spark
- **Storage Format:** Delta Lake

## Data Flow

1. Data is ingested from AWS S3 into Bronze streaming tables.
2. Bronze tables capture raw, schema-on-read data.
3. Silver tables apply transformations, validations, and deduplication.
4. Final curated datasets are published as materialized views for reporting.

## Technologies Used

- AWS (S3, IAM)
- Databricks
- Apache Spark
- Delta Lake
- Delta Live Tables (DLT)
- SQL
- Python

## Job Execution

- Jobs are executed manually or via schedule.
- Pipeline execution status and lineage are monitored through Databricks Jobs UI.
- Successful runs generate refreshed reporting tables.

## Future Enhancements

- Add data quality expectations and alerts
- Enable automated scheduling
- Integrate BI dashboards (Power BI / Tableau)
- Implement CI/CD for pipeline deployments

<img width="1493" height="626" alt="image" src="https://github.com/user-attachments/assets/1d855ff9-36b8-4f2d-889a-c4ae5a6b2698" />

