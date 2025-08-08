# AWS Serverless ETL Pipeline for Real-Time Data Processing

This project demonstrates the design and implementation of a fully **serverless ETL pipeline** on AWS to ingest, transform, store, catalog, and analyze **real-time transactional JSON data**. The pipeline leverages key AWS services like **S3**, **Lambda**, **Glue**, **Athena**, and **QuickSight** to provide a robust, scalable, and cost-efficient data processing workflow.

---

## 📌 Features

- **Event-driven architecture** using S3 triggers
- **Serverless data transformation** with AWS Lambda (JSON → Parquet)
- **Centralized Data Lake** storage in Amazon S3
- **Automated data cataloging** with AWS Glue Crawlers
- **Serverless querying** with Amazon Athena
- **Interactive graphs for visualization** using AWS QuickSight

---

## ⚙️ Architecture Overview

1. **Data Ingestion**  
   JSON files are uploaded to an S3 bucket, which triggers an AWS Lambda function.

2. **Data Transformation**  
   The Lambda function parses the incoming JSON, converts it to **Parquet** format, and stores the result in a separate S3 bucket (Data Lake).

3. **Data Cataloging**  
   AWS Glue Crawlers scan the Parquet files and update the Data Catalog for structured querying.

4. **Data Analysis**  
   Athena queries the cataloged data using SQL-like syntax.

5. **Data Visualization**  
   Athena query results are visualized in AWS QuickSight with interactive graphs.

---

## 🧰 AWS Services:

| Service        | Purpose                                    |
|----------------|--------------------------------------------|
| Amazon S3      | Raw data ingestion & Data Lake storage     |
| AWS Lambda     | Serverless ETL logic (JSON → Parquet)      |
| AWS Glue       | Schema inference & data cataloging         |
| Amazon Athena  | Querying structured data                   |
| AWS QuickSight | Visualizating the graphs            |
