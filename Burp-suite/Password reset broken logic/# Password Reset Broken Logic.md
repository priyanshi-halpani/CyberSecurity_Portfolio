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

## Mitre Attack Analysis

This lab demonstrates an attacker abusing a vulnerable password reset process to gain unauthorized access to another user's account.

## MITRE ATT&CK Mapping

|## MITRE ATT&CK Mapping

| Activity Observed                                         | ATT&CK Tactic     | Analysis                                                                                                                         |
| --------------------------------------------------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Exploiting a weakness in the password reset functionality | Initial Access    | The attacker abused a flaw in the password reset workflow to gain unauthorized access to the application.                        |
| Manipulating authentication-related functionality         | Credential Access | The attacker modified password reset requests and bypassed intended authentication controls to take over another user's account. |
| Accessing the victim account after resetting the password | Initial Access    | After successfully resetting the victim's password, the attacker authenticated and gained unauthorized access to the account.    |


The attack begins by identifying a flaw in the password reset workflow. By manipulating requests and abusing weak validation logic, an attacker can reset another user's password without proper authorization.

After successfully changing the victim's password, the attacker can log in and gain access to the account. This demonstrates how weaknesses in account recovery mechanisms can lead to account takeover.

## Key Learning

Password reset functionality must validate user identity securely. Logic flaws in account recovery processes can allow attackers to take over accounts without knowing the original password.

## Skills Practiced

* Authentication Testing
* Account Takeover Techniques
* Burp Suite
* Web Application Security
* Business Logic Testing


