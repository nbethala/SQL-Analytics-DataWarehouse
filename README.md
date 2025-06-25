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

### **Directory Structure**

data-warehouse-project/
│
├── Datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── Architecture_Maps/                  # Project documentation and architecture details
│   ├── Data_Integration_Model          # Draw.io file shows all different techniquies and methods of ETL
│   ├── SQL_Server_Architecture         # Draw.io file shows the project's architecture
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── Data_Flow.drawio                # Draw.io file for the data flow diagram
│   ├── Data_Model.drawio               # Draw.io file for data models (star schema)
│   ├── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── scripts/                            # SQL/Python scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── QA_scripts/                         # Test scripts and quality files
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository
├── .gitignore                          # Files and directories to be ignored by Git

---

### **Project Outcomes**
Unified and validated CRM/ERP data for faster business decisions

Scalable, container-based development environment

Reusable Python ETL and SQL analytics logic

BI-ready insights driving targeted business action

### **Future Enhancements**

Integrate orchestration tools like Apache Airflow

Expand to support additional data sources (e.g. APIs, flat files)

Enhance metadata documentation and data quality logging
















