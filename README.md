# Real-Time Insurance Claims Data Pipeline

![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?logo=snowflake&logoColor=white)
![DBT](https://img.shields.io/badge/dbt-FF694B?logo=dbt&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)
![Airbyte](https://img.shields.io/badge/Airbyte-0097D8?logo=airbyte&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black)

---

## 📌 Project Overview
This project demonstrates a **beginner-friendly real-time data pipeline** for **insurance claims data**.  
We simulate real-time insurance customer and claim data, move it from a **NoSQL database (MongoDB)** to a **cloud warehouse (Snowflake)** using **Airbyte**, transform the data with **DBT**, and finally visualize insights with **PowerBI**.

This pipeline gives you a **clear blueprint of how modern data engineering projects work**, without being overwhelming, making it ideal for beginners.

<img width="1341" height="1091" alt="Insurance" src="https://github.com/user-attachments/assets/bf07757b-58f9-4c7a-a0a9-948eec56d31a" />

---

## ⚡ Tech Stack
- **MongoDB** → NoSQL OLTP database  
- **Airbyte** → ETL/ELT connector (Ingest data to warehouse)  
- **Snowflake** → Cloud Data Warehouse  
- **DBT** → SQL-based data transformations  
- **Python** → Data simulation and helpers  
- **PowerBI** → Data visualization  

---

## ✅ Key Features
- Generate **realistic insurance customers and claims data**  
- Stream data from MongoDB to Snowflake using **Airbyte**  
- Clean and transform raw data with **DBT**  
- Build **Visualizations** in PowerBI  
- Beginner-friendly, hands-on, step-by-step pipeline  

---

## 📂 Repository Structure

```text
insurance-nosql-pipeline/
├── data-generator/                        # Simulated JSON data generator
│   ├── Simulator.py
├── ins_dbt/                               # DBT project
│   └── models/
│   │   ├── claims_summary.sql
│   │   ├── stg_claims.sql
│   │   ├── source.yml
├── README.md
```

---

## 🚀 Getting Started

1. Clone this repo and install dependencies:

```bash
1. Start MongoDB (Atlas free tier).

2. Run Python script to generate sample insurance data.

3. Configure Airbyte to sync MongoDB → Snowflake.

4. Initialize DBT project and run transformations.

5. Connect PowerBI to Snowflake to create dashboards.
```
---

## ⚙️ Step-by-Step Implementation

### 1. MongoDB Setup
- Use **Atlas free tier**.  
- Import `customers.json` and `claims.json` collections.  
- MongoDB acts as the **source OLTP database** for the pipeline.  

### 2. Data Simulation
- `Simulator.py` creates **fake insurance customer & claims records**.  
- Supports **hundreds of rows** for testing and learning.  
- All data is in **JSON format**, easy to ingest.  

### 3. Airbyte Setup
- Run **Airbyte UI** locally via Docker.  
- Create **source** (MongoDB) and **destination** (Snowflake).  
- Configure **sync frequency**.  
- Data is automatically moved from **MongoDB → Snowflake**.  

### 4. Snowflake Warehouse
- Create **database, schema, and tables** in Snowflake.  
- Airbyte sync creates **raw tables automatically**.  
- Snowflake acts as the **central OLAP warehouse**.  

### 5. DBT Transformations
- Initialize **DBT project** connected to Snowflake.  
- Create **staging models** `stg_claims` → clean raw data.  
- Create **final summary model** (`claims_summary`) → aggregates claims by month, type, and fraud.  

### 6. PowerBI Dashboard
- Connect to **Snowflake** (`claims_summary` table).  
- Create visualizations.
- Makes insights **clear, visual, and business-ready**.  

---

## 📊 Final Deliverables
- **Real-time insurance data pipeline**  
- **MongoDB collections → source OLTP**  
- **Snowflake warehouse tables → OLAP**  
- **Transformed DBT models → clean & aggregated data**  
- **Interactive dashboards → PowerBI**  

---

**Author:** *Jaya Chandra Kadiveti*  
**LinkedIn:** [Jaya Chandra Kadiveti](https://www.linkedin.com/in/jayachandrakadiveti/)  
**Contact:** [Kadivetijayachandra@gmail.com](mailto:Kadivetijayachandra@gmail.com)

