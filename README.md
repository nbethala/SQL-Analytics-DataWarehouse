# Data Warehouse(SQL Server): ETL, Modeling & Analytics
Building a modern data warehouse leveraging SQL Server, this project focuses on designing and implementing robust ETL processes, developing efficient data models, and establishing a scalable analytics framework. The initiative aims to centralize disparate data sources, ensure high data quality, and enable real-time insights through streamlined reporting and visualization. 

## Data Architecture
This project establishes a modern data warehouse on SQL Server, architected using the Medallion Architecture with clearly defined Bronze, Silver, and Gold layers. Raw data is ingested into the Bronze layer for traceability and audit, then refined through robust ETL pipelines powered by Python scripting into the Silver layer, where data is cleansed, standardized, and integrated. The Gold layer surfaces curated, analytics-ready datasets that serve as the foundation for executive dashboards and advanced reporting. By enforcing modularity and lineage across the pipeline, the architecture enhances scalability, data quality, and the agility to adapt to evolving analytical needs—driving high-value, insight-driven decision-making across the enterprise.


![SQL_server_architecture](https://github.com/user-attachments/assets/7a732b84-68b9-49f3-86a9-5e40d43e014a)



Bronze Layer: The Bronze layer captures raw data as-is from the source systems. Data is ingested from CSV Files into SQL Server Database.

Silver Layer: The Silver layer applies robust ETL transformations, standardizing and cleaning the data into analytical models.

Gold Layer: The Gold layer delivers curated, business-ready datasets optimized for reporting, dashboarding, and advanced analytics.



