# Data Warehouse(SQL Server): ETL, Modeling & Analytics
Building a modern data warehouse leveraging SQL Server, this project focuses on designing and implementing robust ETL processes, developing efficient data models, and establishing a scalable analytics framework. The initiative aims to centralize disparate data sources, ensure high data quality, and enable real-time insights through streamlined reporting and visualization. By integrating best practices in data engineering, the solution empowers stakeholders with reliable, actionable intelligence to support strategic decision-making and long-term data governance.

## Data Architecture
This project establishes a modern data warehouse on SQL Server, architected using the Medallion Architecture with clearly defined Bronze, Silver, and Gold layers. Raw data is ingested into the Bronze layer for traceability and audit, then refined through robust ETL pipelines powered by Python scripting into the Silver layer, where data is cleansed, standardized, and integrated. The Gold layer surfaces curated, analytics-ready datasets that serve as the foundation for executive dashboards and advanced reporting.


![SQL_server_architecture](https://github.com/user-attachments/assets/7a732b84-68b9-49f3-86a9-5e40d43e014a)


