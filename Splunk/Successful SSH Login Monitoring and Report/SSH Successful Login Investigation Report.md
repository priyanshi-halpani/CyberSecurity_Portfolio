# SSH Successful Login Investigation Report

## 1. Incident Summary

A Splunk alert was created to detect successful SSH login activity from authentication logs. During testing, the alert identified successful login events and triggered as expected. An investigation was performed to validate the alert and review the authentication activity.

## 2. Alert Details

| Field           | Value                          |
| --------------- | ------------------------------ |
| Alert Name      | SSH Successful Login Detection |
| Monitoring Tool | Splunk Enterprise              |
| Source IP       | ::1                            |
| Username        | kali                           |
| Alert Type      | Scheduled (Every 5 Minutes)    |

### Detection Query

```spl
source="/home/kali/report.log" host="kali" sourcetype="incident report" "Accepted password"
| rex field=_raw "from (?<src_ip>\S+)"
| stats count as "Successful Login" by src_ip
```

## 3. Investigation

To generate authentication events, multiple failed SSH login attempts were performed followed by successful authentication using valid credentials.

The authentication logs were collected and monitored in Splunk. A detection rule was created to identify successful SSH login events and an alert was configured to run every five minutes.

After the alert triggered, the logs were reviewed to validate the event. The investigation confirmed that successful SSH logins had occurred from the source IP address ::1, which represents the local machine (IPv6 loopback address).

The authentication activity was reviewed to determine whether any suspicious behavior occurred after the successful login. No malicious post-authentication activity was observed during testing.

## 4. Timeline

| Event                          | Description                                             |
| ------------------------------ | ------------------------------------------------------- |
| Failed Authentication Attempts | Multiple failed SSH login attempts generated            |
| Successful Authentication      | User successfully authenticated using valid credentials |
| Log Collection                 | Authentication logs ingested into Splunk                |
| Alert Triggered                | Detection rule identified successful login activity     |
| Investigation Performed        | Logs reviewed and activity validated                    |

## 5. Findings

* Multiple failed authentication attempts were observed.
* Two successful SSH login events were detected.
* Authentication activity originated from the source IP ::1.
* The pattern of failed attempts followed by successful authentication may indicate password guessing or brute-force behavior.
* No suspicious activity was identified after successful authentication during the investigation period.

## 6. MITRE ATT&CK Mapping

| Activity Observed              | ATT&CK Tactic     |
| ------------------------------ | ----------------- |
| Multiple failed login attempts | Credential Access |
| Successful SSH authentication  | Initial Access    |

## 7. Recommendations

* Use strong and unique passwords.
* Monitor authentication logs regularly.
* Review repeated failed login attempts for suspicious activity.


## 8. Conclusion

This project demonstrated how Splunk can be used to monitor and investigate SSH authentication activity. Successful login events were detected using a custom SPL query and validated through log analysis. The exercise provided practical experience with security monitoring, alert creation, event investigation, and baisc incident reporting.
