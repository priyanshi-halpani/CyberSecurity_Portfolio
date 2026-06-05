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


## MITRE ATT&CK Mapping

This attack scenario aligns with the MITRE ATT&CK framework as follows:

| Activity Observed                                                             | ATT&CK Tactic     | ATT&CK Technique       |
| ----------------------------------------------------------------------------- | ----------------- | ---------------------- |
| Repeated password guessing attempts against the password change functionality | Credential Access | Brute Force (T1110)    |
| Discovery of valid credentials through successful password guessing           | Credential Access | Brute Force (T1110)    |
| Successful authentication using the identified credentials                    | Initial Access    | Valid Accounts (T1078) |

### Analysis

During this lab, the password change functionality was abused to repeatedly test password values until the correct credential was identified. This behavior maps to **Brute Force (T1110)** under the **Credential Access** tactic because the attacker attempts to obtain valid credentials through repeated authentication attempts.

Once valid credentials were discovered and used to access the target account, the activity aligned with **Valid Accounts (T1078)** under the **Initial Access** tactic, as legitimate credentials were used to gain access to the application.


## Key Learning

Password change functionality must implement proper authentication checks and rate limiting. Weak validation logic can allow attackers to brute-force credentials through account management features.

## Skills Practiced

* Authentication Testing
* Brute Force Testing
* Burp Suite
* Access Control Assessment
* Web Application Security

