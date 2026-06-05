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

## MITRE ATT&CK Mapping

| Activity Observed                                                       | ATT&CK Tactic     | Analysis                                                                                                                     |
| ----------------------------------------------------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Exploiting a blind SQL injection vulnerability in the TrackingId cookie | Initial Access    | The attacker abused a web application vulnerability to interact with the backend database through crafted SQL queries.       |
| Enumerating the administrator password character by character           | Credential Access | The attacker extracted authentication credentials by leveraging conditional SQL queries and observing application responses. |
| Logging in with the recovered administrator credentials                 | Initial Access    | The attacker successfully authenticated using valid credentials obtained through the SQL injection attack.                   |

## Key Learning

Blind SQL injection can be exploited even when database errors and query results are hidden. Application behavior differences can leak sensitive information.

 Skills Practiced

* SQL Injection
* Burp Suite
* Web Application Testing
* Authentication Testing
