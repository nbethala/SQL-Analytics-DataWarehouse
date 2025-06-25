#  Data Warehouse(SQL Server): ETL, Modeling & Analytics

A scalable, containerized data platform using SQL Server, Python, and Docker, architected with Medallion principles to enable high-quality analytics and robust data governance.

##  Project Overview

This project builds a modern data warehouse powered by SQL Server, Python-driven ETL pipelines, and Docker containers. Designed around the Medallion Architecture, data flows seamlessly from raw ingestion (Bronze) through transformation (Silver) to business-ready insights (Gold). The system automates multi-source integration from key systems like CRM and ERP.

---

##  Objectives

- Unify CRM and ERP data sources into a centralized SQL Server warehouse
- Automate ETL pipelines with modular Python scripts
- Structure data via Medallion layers (Bronze, Silver, Gold)
- Use Docker to ensure consistent, replicable development environments
- Deliver clean, analytics-ready datasets to downstream tools

---

---

## 📊 BI: Analytics & Reporting (Data Analysis)

**Objective:**  
Develop SQL-based analytics to deliver detailed insights into:

- **Customer Behavior:** Track user engagement, retention, and churn  
- **Product Performance:** Measure usage patterns, feature adoption, and support metrics  
- **Sales Trends:** Analyze revenue drivers, seasonal performance, and regional breakdowns

These insights are derived from curated Gold layer datasets and are optimized for visualization in BI tools such as Power BI or Tableau. 

---

## Data Architecture
This project establishes a modern data warehouse on SQL Server, architected using the Medallion Architecture with clearly defined Bronze, Silver, and Gold layers. Raw data is ingested into the Bronze layer for traceability and audit, then refined through robust ETL pipelines powered by Python scripting into the Silver layer, where data is cleansed, standardized, and integrated. The Gold layer surfaces curated, analytics-ready datasets that serve as the foundation for executive dashboards and advanced reporting. By enforcing modularity and lineage across the pipeline, the architecture enhances scalability, data quality, and the agility to adapt to evolving analytical needs—driving high-value, insight-driven decision-making across the enterprise.


![SQL_server_architecture](https://github.com/user-attachments/assets/7a732b84-68b9-49f3-86a9-5e40d43e014a)


## **Medallion Layers**

**Bronze Layer:** The Bronze layer captures raw data as-is from the source systems. Data is ingested from CSV Files into SQL Server Database.

**Silver Layer:** The Silver layer applies robust ETL transformations, standardizing and cleaning the data into analytical models.

**Gold Layer:** The Gold layer delivers curated, business-ready datasets optimized for reporting, dashboarding, and advanced analytics.

---

### **Data Flow**

![Data_Flow](https://github.com/user-attachments/assets/0f8dcebb-10bc-447a-9a63-6161d14e8289)

---

### **Technologies **
SQL (T-SQL) – Core language for data modeling, transformation, validation, and analytics

SQL Server – Relational database platform for data storage and warehousing

Python – ETL scripting using pandas, pyodbc, and custom workflow orchestration

Docker – Containerization of SQL Server instances and ETL environments for portability

Git – Version control for ETL scripts, SQL logic, and configuration files

---


## 📁 Repository Structure

```plaintext
data-warehouse-project/
│
├── Datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── Architecture_Maps/                  # Project documentation and architecture details
│   ├── Data_Integration_Model.drawio   # ETL techniques and integration methods
│   ├── SQL_Server_Architecture.drawio  # System architecture overview
│   ├── data_catalog.md                 # Dataset metadata and field descriptions
│   ├── Data_Flow.drawio                # End-to-end data flow
│   ├── Data_Model.drawio               # Logical and physical star schema
│   ├── naming-conventions.md           # Naming guidelines for consistent development
│
├── scripts/                            # SQL/Python scripts for ETL and transformations
│   ├── bronze/                         # Load raw data into Bronze layer
│   ├── silver/                         # Data cleansing and validation scripts
│   ├── gold/                           # Scripts for business logic and data modeling
│
├── QA_scripts/                         # Automated tests and data quality checks
│
├── README.md                           # This file
├── LICENSE                             # Project licensing details
├── .gitignore                          # Ignore config and metadata files


---

### **Project Outcomes**
Clear separation of ETL logic: Bronze (raw), Silver (cleansed), Gold (curated)
SQL-based data quality validation and analytical logic
Fully Dockerized local development setup
Modular ETL scripts reusable across datasets and sources
BI-ready outputs for reporting and forecasting initiatives

---

### **Future Enhancements**

Integrate task orchestration with Apache Airflow
Expand analytics coverage to additional business domains
Automate data catalog updates and field-level documentation
Optimize for real-time ingestion and near real-time reporting

















