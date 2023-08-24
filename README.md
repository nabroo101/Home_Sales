# Home Sales Analysis 

## Overview
This project analyzes home sales data, focusing on different characteristics such as price, view rating, bedrooms, bathrooms, and more. Various queries have been run to extract insights, and the data has been handled through different formats for optimization, including caching and parquet.

## Technologies Used
- Apache Spark
- SQL

## Key Features

### 1. Creating Temporary Views
Using Spark, temporary views of the DataFrame were created to facilitate the SQL queries.

### 2. Caching Data
The data was cached to improve the query runtime. Caching made the queries run faster compared to the initial run without caching.

### 3. Utilizing Parquet
The data was written and read in parquet format, partitioned by the "date_built" field. This led to even more significant improvements in query performance.

### 4. Runtime Comparisons
The runtimes for the queries were compared across different methods:
- Without caching: 1.7 seconds
- With caching: 1.34 seconds
- With parquet: 0.39 seconds

### 5. Uncaching Data
A command was used to uncache the table after completing the operations, ensuring no residual data was left in the cache.

## Files and Queries
The project includes several significant queries, some of which are:
- Calculating the average price for a four-bedroom house sold each year.
- Finding the average price of homes meeting specific criteria.
- Extracting the "view" rating for homes priced above a certain threshold.

## Conclusion
This project demonstrates efficient ways to handle and analyze large datasets using Spark and SQL. By using caching and parquet formatting, significant improvements were achieved in query runtime.

## Commands to Run the Project
Ensure that Apache Spark is installed and configured in your environment, then run the Python script containing the SQL queries and Spark commands.
