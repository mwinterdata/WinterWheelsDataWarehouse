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


---------------------------


**Quick Guide:**

-This repository is split into 'datasets' containing all of the data used within the data warehouse, and 'workflow' showing the workflow in an easy to read and work through format. If
Winter Wheels was a real company and this data warehouse was going to be regularly refreshed and updated, I would separate this workflow by layers as well as separate out the tests (and
make them more comprehensive), as well as add refresh automations to reflect the frequency that the external data was updated. Hopefully however this adjusted format allows for a much reduced
appraisal time.

-The datasets for this project come from two sources; the CRM (Customer Relationship Management) and ERP (Enterprise Resource Planning) folders. Throughout the 
bronze and silver layers of the data warehouse it will be made clear which of these the data is coming from with 'crm_' or 'erp_', followed by the original names of these data tables 
in the external system e.g. 'crm_cust_info'.

-Following the medallion architecture structure, the bronze layer is exclusively for landing the data in our database from the external CRM and ERP sources, the silver
layer is for cleaning, standardising, and augmenting the data as necessary (e.g. to add key columns to allow for joins and schema creation), and our gold layer is for 
preparing the data for easy business use.

-Added technical columns for meta-data such as the data a record was created in the silver layer to help identify any issues in the future are indicated wit 'dwh_'

-Views in the gold layer are labelled either 'dim_' for dimensions or 'fact_' for facts to help end business users easily identify their use.
