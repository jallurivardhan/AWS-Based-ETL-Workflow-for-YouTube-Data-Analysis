# AWS-Based ETL Workflow for YouTube Data Analysis

This project demonstrates how to build an **end-to-end ETL data pipeline** on **Amazon Web Services (AWS)** to process and analyze **YouTube data** efficiently.  
It highlights how cloud-based data engineering can automate data ingestion, transformation, and analysis using a fully **serverless** and **scalable** architecture.

---

## 🎯 Project Overview
The goal of this project is to show how raw data from YouTube (in CSV format) can be automatically:
1. **Extracted** from source systems  
2. **Transformed** into clean, optimized formats (Parquet)  
3. **Loaded** into a centralized data lake on AWS  
4. **Queried and Visualized** using Athena and QuickSight  

This project is ideal for showcasing your skills in **AWS Data Engineering**, **ETL pipeline design**, and **Data Analytics**.

---

## 🧱 Architecture Diagram
![Data Architecture Diagram](Data_Architecture_Diagram.png)

### 🔍 Workflow Explanation
- **Source Systems**: Provide raw YouTube CSV datasets.  
- **Amazon S3**: Acts as a Data Lake — with separate zones for Raw, Processed, and Analytics data.  
- **AWS Glue (PySpark)**: Performs data cleaning, transformation, and format conversion from CSV to Parquet.  
- **AWS Lambda**: Automates Glue job execution when new data arrives in S3.  
- **AWS Glue Data Catalog**: Stores metadata for structured querying.  
- **Amazon Athena**: Runs SQL queries directly on processed data stored in S3.  
- **Amazon QuickSight**: Visualizes insights such as top channels, engagement trends, and viewership metrics.  
- **AWS IAM**: Manages secure access across all services.

➡️ The entire pipeline is **serverless**, **scalable**, and follows a **pay-per-query** model — no servers to manage and costs only when used.

---

## 🧰 AWS Services Used
| Service | Role |
|----------|------|
| **Amazon S3** | Data storage (raw, processed, and analytics layers) |
| **AWS Glue (PySpark)** | ETL job for data transformation and schema definition |
| **AWS Lambda** | Automation trigger for Glue ETL |
| **AWS Glue Data Catalog** | Metadata store for Athena queries |
| **Amazon Athena** | Serverless SQL engine for data analysis |
| **Amazon QuickSight** | Visualization and dashboarding |
| **AWS IAM** | Secure role-based access management |

---

## 📊 Implementation Summary
1. **Upload Raw Data:**  
   Upload YouTube CSV files into the **S3 raw zone** using a simple Python uploader.  

2. **Transform Data with Glue:**  
   Run the **AWS Glue PySpark job** to clean and convert CSV → Parquet format in the **S3 processed zone**.  

3. **Query with Athena:**  
   Use **Athena** to explore processed data directly from S3 using SQL.  

4. **Visualize with QuickSight:**  
   Create dashboards showing:  
   - Top 10 channels by views  
   - Category-wise engagement (likes/comments)  
   - Trending uploads by publish date  

---

## 📈 Key Outcomes
- Built a **serverless data lake pipeline** using AWS services.  
- Reduced storage costs using Parquet compression.  
- Enabled **real-time querying** via Athena.  
- Designed a **dashboard-ready dataset** for YouTube analytics.  

---

## 🧩 Skills Demonstrated
- AWS Data Engineering (S3, Glue, Lambda, Athena, QuickSight)  
- ETL Pipeline Design and Automation  
- PySpark Data Transformation  
- SQL-based Analytics  
- Cloud Architecture & Data Lake Design  

---

## 🚀 Future Improvements
- Integrate **AWS Step Functions** for orchestration  
- Add **Data Quality checks** using AWS Deequ  
- Implement **CI/CD** for Glue and Lambda jobs using GitHub Actions  
- Build real-time data ingestion with **Kinesis Firehose**  

