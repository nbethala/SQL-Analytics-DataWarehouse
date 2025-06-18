
/*
===============================================================================
Python Script: Load Bronze Layer (Source -> Bronze)
===============================================================================
This Python script automates the process of loading external CSV files into the bronze schema within Microsoft SQL Server. It ensures data integrity and efficiency by performing the following operations:

1️⃣ Table Reset:
Truncates existing bronze tables to maintain clean and up-to-date data.

2️⃣ Optimized Bulk Loading:
Executes the BULK INSERT command to efficiently ingest CSV files into designated bronze tables in SQL Server.

This script is a key component of a data warehouse ETL pipeline, designed to streamline data ingestion and support scalable analytics.

Parameters:
    None. 
	  This script does not accept any parameters or return any values.

Usage Example:
    etl_bulk_loader_bronze.py 
    ===============================================================================
*/

import pyodbc
import pandas as pd

# Establish a Connection to SQL Server
conn = pyodbc.connect(
    "DRIVER={ODBC Driver 17 for SQL Server};"
    "SERVER=127.0.0.1;"
    "DATABASE=DataWarehouse;"
    "UID=SA;"
    "PWD=MyPass@word"
)
cursor = conn.cursor()

# Define the file paths directly (SQL Server locations)
csv_to_table = {
    "/var/opt/mssql/source_crm/cust_info.csv": "bronze.crm_cust_info",
    "/var/opt/mssql/source_crm/prd_info.csv": "bronze.crm_prd_info",
    "/var/opt/mssql/source_crm/sales_details.csv": "bronze.crm_sales_details",
    "/var/opt/mssql/source_erp/CUST_AZ12.csv": "bronze.erp_cust_az12",
    "/var/opt/mssql/source_erp/LOC_A101.csv": "bronze.erp_loc_a101",
    "/var/opt/mssql/source_erp/PX_CAT_G1V2.csv": "bronze.erp_px_cat_g1v2"
}

# Process each file and insert into the corresponding table
for csv_path, table_name in csv_to_table.items():

    # Step 1: TRUNCATE if the table exists
    truncate_query = f"TRUNCATE TABLE {table_name};"
    cursor.execute(truncate_query)
    conn.commit()
    print(f"🗑 Cleared table: {table_name}")


    # Step 2: Perform BULK INSERT
    bulk_insert_query = f"""
    BULK INSERT {table_name}
    FROM '{csv_path}'
    WITH (
        FIRSTROW = 2,
        FIELDTERMINATOR = ',',
        ROWTERMINATOR = '\n',
        TABLOCK
    );
    """

    try:
        cursor.execute(bulk_insert_query)
        conn.commit()

        print(f"✅ Successfully inserted: {csv_path} → {table_name}")
    except Exception as e:
        print(f"❌ Error inserting {csv_path}: {e}")

# Close database connection
conn.close()
