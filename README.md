# AWS Serverless Data Pipeline  🚀

This repository contains an end-to-end, event-driven data engineering ecosystem built on AWS. It demonstrates the transition from manual infrastructure to a fully automated, resilient pipeline using serverless architecture.

## 🏗️ Architecture Overview
The pipeline follows a "Security-First" approach to automate the flow of data from ingestion to analytics:
1.  **Ingestion:** Raw data is uploaded to an **Amazon S3** Data Lake.
2.  **Trigger:** An S3 Event Notification triggers an **AWS Lambda** function (Python/Boto3).
3.  **Transformation:** **AWS Glue** performs ETL (Extract, Transform, Load) to process raw files into optimized formats.
4.  **Analytics:** **Amazon Athena** queries the processed data directly from S3 using standard SQL.

## 🛠️ Key Features
*   **IAM-Centric Security:** Granular Roles and Policies for secure service-to-service communication.
*   **Cost-Optimized Storage:** S3 Versioning and Intelligent-Tiering for high-durability big data storage.
*   **Event-Driven Automation:** Zero-latency triggers using **Boto3** and Lambda.
*   **Serverless ETL:** Low-code data transformations via **Glue Studio**, eliminating server management.
*   **Instant Analytics:** Schema discovery via Glue Crawlers for immediate SQL querying in Athena.



## 🚀 Getting Started
1.  **Configure IAM:** Set up roles for Lambda and Glue with S3 read/write permissions.
2.  **Setup S3:** Create buckets for `raw-data` and `transformed-data`.
3.  **Deploy Lambda:** Upload `src/lambda_function.py` and set an S3 trigger on the `raw-data` bucket.
4.  **Configure Glue:** Set up a Crawler to catalog the `transformed-data` and run the ETL job.
5.  **Query:** Use Amazon Athena to run SQL against your processed dataset.

---
*Developed during the AWS Data Engineering Masterclass.*
