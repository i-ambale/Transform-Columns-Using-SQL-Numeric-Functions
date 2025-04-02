# Transform Columns Using Numeric Functions in SQL
Overview
This repository demonstrates how to use numeric functions such as SQRT, LOG, and ROUND to transform columns in a table within a SQL database. The dataset used for this demonstration is the Access_to_Basic_Services table, which is part of the united_nations MySQL database.

The notebook is designed to provide hands-on experience with SQL queries for numerical transformations. However, it requires a local setup since it connects directly to a MySQL server and cannot run on cloud-based platforms like Google Colab.

Learning Objectives
By the end of this notebook, you should:

Understand how to apply numeric functions (SQRT, LOG, ROUND) in SQL queries.
Gain practical experience transforming numerical columns in a database table.
Learn how to connect to a MySQL database using Python libraries like mysql and pymysql.
Prerequisites

To run this notebook successfully, ensure the following:

MySQL Workbench is installed on your local machine.
The united_nations database is set up and contains the Access_to_Basic_Services table.
Python libraries mysql and pymysql are installed. You can install them using pip:
```
pip install mysql-connector-python pymysql
```
Basic knowledge of SQL and Python is required.
Dataset Description
The Access_to_Basic_Services table contains numerical data on access to basic services (e.g., water, electricity, sanitation) across different regions or countries. The exact structure of the table may include columns such as:

country_name
year
water_access_percentage
electricity_access_percentage
sanitation_access_percentage
This dataset will be used to demonstrate the application of numeric functions.

Connecting to the MySQL Database
To connect to the MySQL database, we use the mysql and pymysql libraries in Python.

Numeric Functions in SQL
Below are examples of how to use numeric functions to transform columns in the Access_to_Basic_Services table:
---
1. SQRT (Square Root)
The SQRT function calculates the square root of a numerical column. For example:
```
SELECT country_name, SQRT(water_access_percentage) AS sqrt_water_access
FROM Access_to_Basic_Services;
```
---
2. LOG (Logarithm)
The LOG function computes the natural logarithm of a numerical column. For example:
```
SELECT country_name, LOG(electricity_access_percentage) AS log_electricity_access
FROM Access_to_Basic_Services;
```
---
3. ROUND (Rounding Numbers)
The ROUND function rounds a numerical column to a specified number of decimal places. For example:

```
SELECT country_name, ROUND(sanitation_access_percentage, 2) AS rounded_sanitation_access
FROM Access_to_Basic_Services;
```
---
Notes
Ensure that the numerical columns in your dataset do not contain negative values when using SQRT or LOG, as these functions are undefined for negative numbers.
Always back up your database before running transformation queries to avoid accidental data loss.

Contact
For questions or feedback, please contact:

Email: your_email@example.com

GitHub: Your GitHub Profile

Thank you for exploring this repository! We hope it helps you deepen your understanding of SQL numeric functions and their applications.





