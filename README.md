# big-data-pipeline-titanic-spark
Built an end-to-end big data pipeline using Apache NiFi, Hadoop, Hive, Spark, and HBase to process and analyze Titanic data and deploy a distributed machine learning model.

# End-to-End Big Data Pipeline for Machine Learning (Titanic Dataset)

##  Overview
This project implements a complete big data pipeline using Apache NiFi, Hadoop (HDFS), Hive, Spark, and HBase to ingest, process, analyze, and store machine learning results.

---

##  Objective
To design a scalable data pipeline that automates data ingestion, distributed processing, machine learning, and persistent storage of results.

---

##  Architecture
- Apache NiFi → Data ingestion
- HDFS → Distributed storage
- Hive → SQL-based data access
- Spark → Distributed machine learning
- HBase → NoSQL storage for model metrics

---

##  Pipeline Workflow
1. Data ingestion using NiFi from external source
2. Storage in HDFS
3. Table creation and querying using Hive
4. Feature engineering and modeling using Spark MLlib
5. Evaluation metrics stored in HBase

---

##  Machine Learning
- Model: Logistic Regression
- Framework: Spark MLlib
- Metrics:
  - Accuracy ≈ 0.77
  - AUC ≈ 0.80

---

##  Key Insights
- Distributed systems enable scalable data processing
- Pipeline integration is critical for real-world data workflows
- Spark efficiently handles machine learning at scale

---

##  Business Value
This project demonstrates how modern data pipelines can automate data ingestion, analysis, and storage, supporting scalable analytics and real-time decision-making.

---

##  Project Structure
- `.py` / `.ipynb` → Spark ML pipeline
- `.docx` → Full project report
- `.json` → NiFi flow configuration
- `.csv` → Dataset

---

##  Author
Shaghayegh Malekshahi  
Master’s in Data Science – Bellevue University
