# Winter Wheels Data Warehouse

Welcome to the repository for the **data warehouse with medallion architecture built in SQL Server** for the fictional company 'Winter Wheels'!  


This project showcases a comprehensive data warehousing solution, from building the structure of the data warehouse to cleaning and preparing 
data for easy, out of the box use for an end user for either analytics or machine learning.
Specifically demonstrated in this project are:
-**Knowledge of and comfort with medallion architecture data warehousing:** following the bronze, silver, and gold layering system to create a data warehouse
where it is not only easy to identify and fix any issues in the data flow, but is also simple for whoever is using the data to perform data analysis without 
having to struggle to understand, extract, or clean confusing data.

-**ETL Pipelines in SQL:** extracting, transforming, and loading data from source systems into the warehouse to end up with clean data files.

-**Data Modeling:** Developing fact and dimension tables optimized for analytical queries and easy to use schema.




Below are some key terms used in the data warehouse to help with its reading and use:




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
