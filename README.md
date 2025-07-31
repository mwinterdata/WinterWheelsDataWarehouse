# Winter Wheels Data Warehouse


Welcome to the repository for the **data warehouse with medallion architecture built in SQL Server** for the fictional company 'Winter Wheels'.  

This project showcases a comprehensive data warehousing solution, from building the structure of the data warehouse to cleaning and preparing data for 
Designed as a portfolio project that highlights industry best practics in data engineering and analytics.

This project involves:

Data Architecture: Designing a Modern Data Warehouse Using Medallion Architecture Bronze, Silver, and Gold layers.
ETL Pipelines: Extracting, transforming, and loading data from source systems into the warehouse.
Data Modeling: Developing fact and dimension tables optimized for analytical queries.
Analytics & Reporting: Creating SQL-based reports and dashboards for actionable insights.
🎯 This repository is an excellent resource for professionals and students looking to showcase expertise in:

SQL Development
Data Architect
Data Engineering
ETL Pipeline Developer
Data Modeling
Data Analytics


Bronze Rules
All names must start with the source system name, and table names must match their original names without renaming.
<sourcesystem>_<entity>
<sourcesystem>: Name of the source system (e.g., crm, erp).
<entity>: Exact table name from the source system.
Example: crm_customer_info → Customer information from the CRM system.

Glossary of Category Patterns
Pattern	Meaning	Example(s)
dim_	Dimension table	dim_customer, dim_product
fact_	Fact table	fact_sales
report_	Report table	report_customers, report_sales_monthly
Column Naming Conventions
Surrogate Keys
All primary keys in dimension tables must use the suffix _key.
<table_name>_key
<table_name>: Refers to the name of the table or entity the key belongs to.
_key: A suffix indicating that this column is a surrogate key.
Example: customer_key → Surrogate key in the dim_customers table.
Technical Columns
All technical columns must start with the prefix dwh_, followed by a descriptive name indicating the column's purpose.
dwh_<column_name>
dwh: Prefix exclusively for system-generated metadata.
<column_name>: Descriptive name indicating the column's purpose.
Example: dwh_load_date → System-generated column used to store the date when the record was loaded.
