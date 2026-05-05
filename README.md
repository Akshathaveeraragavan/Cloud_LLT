*TEAM MEMBERS*
1. RA2512051010007 - V.AKSHATHA - Data Engineering
2. RA2512052010002 – LAKSHMI MANJUSHA – Data Science
3. RA2512052010008 – K SAI MAHESHWARI - Data Science
4. RA2512052010009 – SEPURI SAI SOWMYA- Data Science
5. RA2512052010043 – INDU - Data Science

*FRAMEWORKS / TOOLS USED*
1. Programming Language: Python 3
2. Big Data Framework: Apache Spark (Structured Streaming)
3. Storage System: Hadoop HDFS
4. Data Processing: PySpark
5. Security & Access Control: Apache Ranger (RBAC – 4 roles with defined permissions)
6. Metadata Management: Apache Atlas
7. Visualization: Streamlt
8. Machine Learning (if included): Scikit-learn / TensorFlow / Keras

*PROJECT OVERVIEW*

We built a complete pipeline that handles:
* Data ingestion
* Real-time processing
* Storage (Data Lake)
* Data warehouse queries
* Security & governance
* Dashboard visualization

*ABOUT THE PROJECT WORKFLOW*

**1. Data Ingestion (Kafka Simulation)**

We created 4 kafka topics for each of this data :
* Web logs
* Transactions
* Customer reviews
* Social media
  
All this data is collected using a Kafka-like system.

**2. Stream Processing (Spark Streaming)**

We processed incoming data in real-time using Spark Streaming.

Applied transformations on each data such as removing null values , adding new columns (like revenue, hour, etc.) and removing duplicates.

This helps in fast processing of live data.

**3. Data Lake (3 Layers Architecture)**

We stored data in 3 layers - Medallion architecture:
* Bronze (Raw Data) → Original data
* Silver (Cleaned / Processed Data) → Clean and structured
* Gold (Aggregated / Curated Data) → Ready for analysis
  
This makes data easy to manage and analyze.

**4. Data Warehouse (Hive Simulation)**

We created tables and performed queries like:
* Total revenue by status
* Payment method usage
* Ratings count
  
HiveQL helps analysts get insights using SQL-like queries.

**5. Machine Learning (Customer Churn Prediction)**

Built a ML model using Random Forest to predict Whether a customer will leave (churn)
*Output:*

High accuracy

Feature importance (which factors matter most)

**6. Security (Apache Ranger)**

We implemented:

Role-Based Access Control (RBAC) and Data masking (hide sensitive info)

RBAC - 4 roles and their accessibility:
* Data Engineer - access all data 
* Data Scientist - masked customer_id + processed(silver) and curated data(gold)
* Business Analyst - Only curated layer (gold) data 
* External users → no access

**7. Data Governance (Apache Atlas)**

We tracked:
* Data sources
* Data lineage (where data comes from → where it goes)
* Metadata

Atleas ensures transparency and control.

**8. MDM (Master Data Management)**

We created a Single Customer View by merging: CRM data and E-commerce data

Each customer gets: Unique ID

Segment (New, Regular, VIP)

**9. Workflow Automation (Airflow)**

We simulated a pipeline workflow:

Data ingestion → Processing → Storage → ML → Reporting

Tasks run in sequence with dependencies.


*FINAL OUTPUT*

We created a dashboard using Streamlit showing:
* Revenue analysis
* Payment distribution
* Customer ratings
* Sentiment analysis
* Customer segmentation
* ML feature importance

DASHBOARD - <img width="1795" height="985" alt="image" src="https://github.com/user-attachments/assets/a31d7c1a-1b4e-4089-bf91-1792109aba24" />

**HOW THIS WORFLOW SOLVED THE 4 PROBLEMS ASKED**

**1. SLOW REPORTING**

Issue: Data was not processed fast enough.

Solution: We used Spark Streaming to process data in real-time, making reporting faster.

**2. NO SINGLE CUSTOMER VIEW**

Issue: Customer data was scattered across systems.

Solution: We used MDM (Master Data Management) to create a unified customer profile.

**3.DATA ENGINEERS AND ANALYSTS STRUGGLE TO ANALYSE THE DATA**

Issue: Data engineers and analysts struggled to work with raw data.

Solution: We used a 3-layer Data Lake architecture:
* Bronze → Raw
* Silver → Clean
* Gold → Ready for analysis

**4. SECURITY CONCERNS**

Issue: Sensitive data was not protected.

Solution: We implemented:
* Apache Ranger → Role-based access + data masking
* Apache Atlas → Data governance and tracking


