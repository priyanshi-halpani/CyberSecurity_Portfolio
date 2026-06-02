# Blind SQL Injection with Conditional Responses

**Lab:** PortSwigger Web Security Academy
**Status:** Completed ✅

 Objective

Exploit a blind SQL injection vulnerability in a tracking cookie to retrieve the administrator's password.

 Tools

* Burp Suite Community Edition
* Firefox

## Method

1. Identified a vulnerable `TrackingId` cookie.
2. Used conditional SQL queries to determine TRUE/FALSE responses.
3. Enumerated the administrator password character by character using `SUBSTRING()` and conditional checks.
4. Logged in as administrator using the recovered password.

 Key Learning

Blind SQL injection can be exploited even when database errors and query results are hidden. Application behavior differences can leak sensitive information.

 Skills Practiced

* SQL Injection
* Burp Suite
* Web Application Testing
* Authentication Testing
