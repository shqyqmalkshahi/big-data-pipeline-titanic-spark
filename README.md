# big-data-pipeline-titanic-spark
Built an end-to-end big data pipeline using Apache NiFi, Hadoop, Hive, Spark, and HBase to ingest, process, analyze, and persist machine learning results in a distributed environment.

# End-to-End Big Data Pipeline for Machine Learning (Titanic Dataset)

## Overview
This project implements a complete distributed data pipeline that integrates data ingestion, storage, processing, machine learning, and result persistence using modern big data technologies. The pipeline processes the Titanic dataset and demonstrates how scalable architectures can support real-world analytics workflows.

---

## Objective
The goal of this project is to design and implement a scalable, end-to-end data pipeline capable of:

- Automating data ingestion from external sources  
- Storing data in a distributed environment  
- Enabling structured querying and transformation  
- Training a machine learning model at scale  
- Persisting analytical results for future use  

---

## Business Problem
Organizations today must process large volumes of data efficiently while enabling real-time or near-real-time analytics. Traditional single-machine workflows are insufficient for handling scale, reliability, and performance requirements.

This project demonstrates how distributed systems can be used to build scalable pipelines that automate data processing and support advanced analytics such as machine learning.

---

## Dataset
- Titanic passenger dataset (binary classification problem)
- Features:
  - Passenger class (Pclass)
  - Gender (Sex)
  - Age
  - Fare
  - Embarkation port
- Target variable:
  - Survived (0 = No, 1 = Yes)

The dataset is retrieved dynamically via HTTP using Apache NiFi, demonstrating real-world data ingestion practices.

---

## Architecture Overview

The pipeline integrates multiple components of the Hadoop ecosystem:

- **Apache NiFi** → Data ingestion from external source  
- **HDFS** → Distributed storage layer  
- **Apache Hive** → Structured data access (SQL layer)  
- **Apache Spark (MLlib)** → Distributed machine learning  
- **Apache HBase** → NoSQL storage for model outputs  
- **YARN** → Resource management across cluster  

---

## Pipeline Workflow

1. **Data Ingestion**
   - NiFi retrieves dataset via HTTP request
   - Metadata is assigned and validated
   - Data is written into HDFS  

2. **Storage Layer**
   - Dataset stored in HDFS for distributed access  

3. **Data Structuring**
   - Hive table created for SQL-based querying  
   - Data loaded into managed Hive table  

4. **Machine Learning (Spark)**
   - Data loaded from Hive into Spark  
   - Feature engineering and preprocessing applied  
   - Logistic Regression model trained using Spark MLlib  
   - Predictions and probabilities generated  

5. **Evaluation & Persistence**
   - Model performance metrics calculated:
     - Accuracy ≈ 0.776  
     - AUC ≈ 0.798 :contentReference[oaicite:1]{index=1}  
   - Metrics stored in HBase for persistent access  

---

## Machine Learning Pipeline

- Model: Logistic Regression  
- Framework: Spark MLlib  
- Feature Engineering:
  - Categorical encoding (StringIndexer, OneHotEncoder)
  - Feature vector assembly (VectorAssembler)
- Train/Test Split: 70/30  

### Evaluation Metrics
- Accuracy → measures prediction correctness  
- AUC → measures classification performance across thresholds  

The results demonstrate that the model successfully learned patterns from the dataset and achieved reasonable predictive performance.

---

## Key Insights

- Distributed systems enable scalable data processing workflows  
- Integration of multiple tools is critical for real-world pipelines  
- Spark efficiently handles machine learning at scale  
- Proper data transformation is essential before modeling  
- End-to-end pipelines improve automation and reproducibility  

---

## System Design Highlights

- Fully distributed architecture  
- Fault-tolerant data storage (HDFS)  
- Separation of ingestion, storage, processing, and persistence layers  
- Integration of batch processing with machine learning  
- Use of NoSQL database (HBase) for fast metric retrieval  

---

## Business Value

- Demonstrates scalable data engineering pipeline design  
- Enables automated data ingestion and analytics  
- Supports large-scale machine learning workflows  
- Provides reusable architecture for real-world systems  
- Improves efficiency and reduces manual data processing  

---

## Challenges & Solutions

- **Resource limitations** → managed services carefully across VM  
- **Data type inconsistencies** → handled via casting in Spark  
- **HBase integration** → required Thrift server and HappyBase setup  
- **Pipeline coordination** → ensured proper sequencing of components :contentReference[oaicite:2]{index=2}  

---

## Project Structure

- `.ipynb / .py` → Spark ML pipeline  
- `.pdf` → full project report  
- `.json` → NiFi workflow configuration  
- `images/` → architecture diagrams  

---

## Architecture Diagram

(Recommended: add your NiFi / pipeline diagram here)

---

## Tools & Technologies

- Apache NiFi  
- Hadoop (HDFS)  
- Apache Hive  
- Apache Spark (MLlib)  
- Apache HBase  
- Python (PySpark, HappyBase)  
- YARN  

---

## Author
Shaghayegh Malekshahi  
Master’s in Data Science  
