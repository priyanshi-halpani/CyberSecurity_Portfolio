# Password Brute Force via Password Change

**Lab:** PortSwigger Web Security Academy
**Status:** Completed ✅

## Objective

Exploit weaknesses in the password change functionality to perform a brute-force attack and gain unauthorized access to a user account.

## Tools

* Burp Suite Community Edition
* Firefox

## Method

1. Analyzed the password change feature.
2. Identified that the application handled password verification insecurely.
3. Used Burp Suite to intercept and modify requests.
4. Performed a brute-force attack against the password validation mechanism.
5. Identified the correct password and successfully accessed the target account.

## Key Learning

Password change functionality must implement proper authentication checks and rate limiting. Weak validation logic can allow attackers to brute-force credentials through account management features.

## Skills Practiced

* Authentication Testing
* Brute Force Testing
* Burp Suite
* Access Control Assessment
* Web Application Security

