# SSH Authentication Monitoring Dashboard (Splunk)

## Project Overview

This project demonstrates the creation of a Splunk dashboard for monitoring SSH authentication activity. The dashboard provides visibility into login behavior, authentication failures, invalid user attempts, and potential brute-force attacks.

## Objectives

* Monitor SSH authentication events.
* Detect suspicious login activity.
* Identify potential brute-force attacks.
* Visualize attack sources using geolocation data.

## Dashboard Components

### Authentication Overview

The dashboard displays key authentication metrics including:

* Total SSH Events: **1,200**
* Successful Logins: **306**
* Failed Logins: **305**
* Invalid User Attempts: **286**

These metrics provide a high-level view of authentication activity and help identify unusual login patterns.

### Brute-Force Detection

A dedicated panel highlights source IP addresses responsible for repeated authentication failures. Multiple failed attempts from the same IP address may indicate brute-force activity and require further investigation.

### Failed Login Analysis

A bar chart visualizes accounts or sources associated with failed authentication attempts, helping identify commonly targeted users and attack patterns.

### Geolocation Analysis

The dashboard uses IP geolocation to map the geographic origin of suspicious authentication attempts. This helps analysts identify attack hotspots and understand the distribution of threat activity.

## Key Findings

* Failed login attempts were nearly equal to successful logins, indicating elevated authentication failure rates.
* A significant number of invalid user attempts suggest reconnaissance or automated attack activity.
* Multiple source IP addresses generated repeated authentication failures consistent with brute-force behavior.
* Attack traffic originated from several countries, with the United States generating the highest number of observed events.

## Skills Demonstrated

* Splunk Dashboard Development
* SPL Query Writing
* Log Analysis
* SSH Authentication Monitoring
* Brute-Force Detection
* Security Monitoring
* Threat Hunting
* Geolocation Analysis
