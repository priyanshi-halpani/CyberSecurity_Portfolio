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

## MITRE ATT&CK Mapping

| Activity Observed                                           | ATT&CK Tactic  | Analysis                                                                                                                  |
| ----------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Injecting malicious SQL queries through user input          | Initial Access | The attacker exploited insufficient input validation in the web application to manipulate backend database queries.       |
| Using UNION SELECT statements to interact with the database | Discovery      | The attacker gathered information about the database structure, including the number of columns and supported data types. |
| Identifying a column capable of displaying text data        | Discovery      | The attacker enumerated database query behavior to prepare for potential extraction of sensitive information.             |


## Key Learning

UNION-based SQL injection requires matching both the number of columns and compatible data types. Identifying a text-compatible column is an important step for extracting data from the database.

## Skills Practiced

* SQL Injection Testing
* UNION Attacks
* Data Type Identification
* Burp Suite
* Web Application Security

