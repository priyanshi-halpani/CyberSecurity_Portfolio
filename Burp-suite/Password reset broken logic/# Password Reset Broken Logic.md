# Password Reset Broken Logic

**Lab:** PortSwigger Web Security Academy
**Status:** Completed ✅

## Objective

Exploit flaws in the password reset functionality to gain unauthorized access to another user's account.

## Tools

* Burp Suite Community Edition
* Firefox

## Method

1. Analyzed the password reset workflow.
2. Intercepted and modified requests using Burp Suite.
3. Identified a logic flaw in the password reset process.
4. Manipulated the reset mechanism to bypass intended security controls.
5. Successfully reset the target user's password and accessed the account.

## Key Learning

Password reset functionality must validate user identity securely. Logic flaws in account recovery processes can allow attackers to take over accounts without knowing the original password.

## Skills Practiced

* Authentication Testing
* Account Takeover Techniques
* Burp Suite
* Web Application Security
* Business Logic Testing


