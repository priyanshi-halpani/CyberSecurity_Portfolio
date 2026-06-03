# Web Traffic Monitoring Dashboard (Splunk)

## Project Overview

This project demonstrates the creation of a Splunk dashboard for monitoring and analyzing web server traffic logs. The dashboard provides visibility into request volumes, response status codes, client activity, and geographic traffic distribution to support web monitoring and security analysis.

## Objectives

* Monitor overall web traffic activity.
* Analyze HTTP response status codes.
* Identify frequently accessed resources.
* Track client IP address activity.
* Visualize geographic sources of web traffic.

## Dashboard Components

### Traffic Overview

The dashboard provides a summary of key web traffic metrics:

* Total Web Requests: **2,000**
* Successful Responses (2xx): **1,168**
* Client Errors (4xx): **376**
* Server Errors (5xx): **167**

These metrics help assess application performance and user activity.

### Top Requested URIs

A bar chart displays the most frequently requested URLs, allowing analysts to identify popular resources and potentially suspicious access patterns.

### Top Users by IP Address

A pie chart visualizes the most active client IP addresses generating web requests. This helps identify high-volume users and unusual traffic sources.

### Geographic Traffic Analysis

A choropleth map displays web traffic distribution by country using IP geolocation. This provides insight into user locations and highlights regions generating the highest traffic volume.

## Key Findings

* The web server processed 2,000 requests during the selected period.
* Successful responses accounted for the majority of web activity.
* Several client and server errors were observed, indicating requests for unavailable resources and potential application issues.
* Certain URIs received significantly more traffic than others, making them high-value resources for monitoring.
* Traffic originated from multiple geographic locations, with some countries contributing substantially higher request volumes.

## Skills Demonstrated

* Splunk Dashboard Development
* SPL Query Writing
* Web Log Analysis
* HTTP Status Code Monitoring
* Traffic Pattern Analysis
* Geolocation Visualization
* Security Monitoring
* Data Visualization
