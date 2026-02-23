# SOC Threat Monitoring Lab (Internship-Focused Version)

## Overview

This project demonstrates the design and validation of a hands-on
Security Operations Center (SOC) monitoring lab built using Splunk
Enterprise and a Windows-based virtual environment.

The objective of this lab was to simulate common attack behaviors and
validate detection logic across authentication activity, privilege
usage, and PowerShell execution.

## Lab Environment

-   Windows 10 Virtual Machine
-   Splunk Enterprise
-   Splunk Universal Forwarder
-   Security Log ingestion (Event IDs 4625, 4740, 4672)
-   PowerShell Operational Log ingestion (Event ID 4104)
-   ScriptBlock logging enabled via Group Policy

## Security Events Monitored

4625 -- Failed Logon Attempts\
4740 -- Account Lockouts\
4672 -- Privileged Logons\
4104 -- PowerShell ScriptBlock Execution

## Key Learning Objectives

-   Understand Windows authentication event flow
-   Configure Splunk Universal Forwarder for log ingestion
-   Enable and validate PowerShell ScriptBlock logging
-   Build detection logic using SPL queries
-   Design a SOC-style monitoring dashboard

## Detection Implemented

-   Brute-force attempt detection using Event ID 4625 trends
-   Account lockout tracking using Event ID 4740
-   Privileged account monitoring using Event ID 4672
-   PowerShell activity monitoring using Event ID 4104
-   Attacker IP and targeted user identification panels

## Validation Process

-   Simulated failed login attempts to generate 4625 events
-   Executed PowerShell web requests to produce 4104 events
-   Verified ingestion pipeline from Windows VM to Splunk
-   Tuned SPL queries to reduce false positives

## Dashboard Screenshots

Executive Summary and Authentication Monitoring:
screenshots/dashboard_overview_top.png

Investigation and Privileged Activity Monitoring:
screenshots/dashboard_overview_bottom.png

## Skills Demonstrated

-   Splunk SPL query development
-   Windows event log analysis
-   Log ingestion troubleshooting
-   SOC investigation workflow design
-   Attack simulation and validation

## Outcome

This project demonstrates foundational SOC analyst capabilities,
including detection engineering, event triage, and monitoring dashboard
design within a controlled lab environment.
