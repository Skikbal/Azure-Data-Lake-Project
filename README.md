# Divvy Bike Data Lakehouse Project - Databricks & Delta Lake

This project demonstrates the implementation of a comprehensive data lakehouse solution using Databricks and Delta Lake, built upon the Divvy bike-sharing dataset. The project follows the medallion architecture (Bronze-Silver-Gold) and implements a star schema data warehouse for analytical reporting on bike trips, rider behavior, and payment transactions.

## Getting Started

These instructions will help you set up and run the data lakehouse pipeline using Databricks and Delta Lake.

### Dependencies
- Databricks Workspace with Spark cluster
- Delta Lake storage
- Sample Divvy bike-sharing dataset (CSV files)
- PySpark and Spark SQL

### Installation

1) Upload raw CSV datasets (riders.csv, trips.csv, stations.csv, payments.csv) to DBFS in Databricks
2) Create bronze layer by ingesting raw CSV data into Delta tables with proper schemas
3) Build silver layer by cleaning, deduplicating, and validating bronze data
4) Design and implement gold layer star schema with dimension and fact tables
5) Create registered Delta tables for easy SQL querying and analytics
6) Validate data quality and run analytical queries to verify business metrics

## Project Architecture

**Medallion Architecture Implementation:**
- **Bronze Layer**: Raw data ingestion from CSV files into Delta format
- **Silver Layer**: Cleaned, deduplicated, and validated data ready for transformation  
- **Gold Layer**: Star schema with optimized dimension and fact tables for analytics

## Project Instructions

### Data Pipeline Structure
```
CSV Files → Bronze (Raw Delta) → Silver (Clean Delta) → Gold (Star Schema)
```

### Star Schema Design
**Dimension Tables:**
- `dim_rider` - Rider demographics and account information
- `dim_station` - Bike station details and locations  
- `dim_date` - Comprehensive date dimension with time attributes

**Fact Tables:**
- `fact_trip` - Trip transactions with duration, stations, and rider metrics
- `fact_payment` - Payment transactions linked to riders and dates


## Built With

- **Databricks**: Unified analytics platform for big data and machine learning
- **Delta Lake**: Open-source storage layer providing ACID transactions
- **Apache Spark**: Distributed computing engine for large-scale data processing
- **PySpark**: Python API for Apache Spark
- **Spark SQL**: SQL interface for structured data processing 

## License

This project is licensed under the MIT License - see the [LICENSE.md](./LICENSE) file for details.

---
*This project demonstrates modern data engineering practices using cloud-native technologies and industry-standard architectures for scalable analytics solutions.*