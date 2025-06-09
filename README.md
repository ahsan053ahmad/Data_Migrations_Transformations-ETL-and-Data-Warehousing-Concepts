# Data_Migrations_Transformations-ETL-and-Data-Warehousing-Concepts

This repository contains my submission for a data engineering assignment focused on data migration and transformation. The task involved extracting data from multiple CSV files, cleaning and transforming the data using Python and Pandas, and preparing it for loading into a data warehouse-style format using SQLite.

---

### Business Problem

Organizations collect data from disparate systems and formats. These data need to be consolidated, transformed, and structured before they can be used for business intelligence and analytics. This lab simulates a data migration task, moving raw operational data into a normalized, analysis-ready format—illustrating the backbone of many enterprise ETL pipelines.

---

### Dataset Overview

The project worked with sample e-commerce transaction data, including:

- `customer.csv` – Customer information
- `product.csv` – Product details
- `sales.csv` – Order-level data including product, quantity, and timestamps

---

### Project Objectives

- Extract raw data from CSVs using Pandas
- Clean and standardize data formats
- Design a star schema using SQLite with dimension and fact tables
- Implement surrogate keys for dimension tables
- Create a `sales_fact` table linked to all dimension tables
- Perform validation queries using SQL

---

### Solution Approach

1. **Data Inspection & Cleaning**
   - Loaded CSVs into Pandas DataFrames
   - Cleaned missing or duplicate values
   - Parsed dates and standardized categorical fields

2. **Schema Design**
   - Created dimension tables for `Customer`, `Product`, and `Time`
   - Generated surrogate keys using index or `uuid`
   - Created a central `Sales_Fact` table with foreign keys

3. **Transformation & Migration**
   - Used Pandas joins to relate dimensions with the sales data
   - Populated fact table with clean, joined, and key-mapped records
   - Inserted all data into a local SQLite database

4. **Validation Queries**
   - Queried top customers and product sales
   - Analyzed order volume over time
   - Verified referential integrity across all tables

---

### Business Value

This lab simulates how data engineering supports business analytics:

- Enables OLAP-style queries through proper schema design
- Improves data quality through transformation and validation
- Supports scalable ETL strategies using surrogate keys and normalization

---

### Challenges Encountered

- Managing surrogate keys across multiple dimension tables
- Ensuring no loss of transactional granularity in the fact table
- Aligning data types across joined tables

---


