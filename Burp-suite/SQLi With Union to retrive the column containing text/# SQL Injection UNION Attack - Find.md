# SQL Injection UNION Attack - Finding a Column Containing Text

**Lab:** PortSwigger Web Security Academy
**Status:** Completed ✅

## Objective

Identify which column in the database query can hold text data using a UNION-based SQL injection attack.

## Tools

* Burp Suite Community Edition
* Firefox

## Method

1. Determined the number of columns returned by the original query.
2. Used a UNION SELECT statement with NULL values.
3. Replaced NULL values with a text string one column at a time.
4. Observed the application's response to identify the column that displayed text.
5. Successfully completed the lab by finding a column that accepted string data.

## Key Learning

UNION-based SQL injection requires matching both the number of columns and compatible data types. Identifying a text-compatible column is an important step for extracting data from the database.

## Skills Practiced

* SQL Injection Testing
* UNION Attacks
* Data Type Identification
* Burp Suite
* Web Application Security

