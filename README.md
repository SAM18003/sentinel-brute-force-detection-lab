# Microsoft Sentinel SOC Lab - Brute Force Detection

## Project Overview
This project demonstrates a basic SOC Analyst L1 use case using Microsoft Sentinel. The lab focuses on collecting Windows Security Events from a Windows Server endpoint, creating a detection rule for multiple failed login attempts, and investigating the generated incident.

## Objective
To detect multiple failed Windows login attempts that may indicate brute-force activity, password guessing, or unauthorized login attempts.

## Tools Used
- Microsoft Azure
- Microsoft Sentinel
- Log Analytics Workspace
- Windows Server 2025 Datacenter
- Windows Security Events
- KQL
- MITRE ATT&CK

## Detection Rule
Rule Name: Multiple Failed Login Attempts

```kql
SecurityEvent
| where EventID == 4625
| summarize FailedAttempts = count() by Account, bin(TimeGenerated, 5m)
| where FailedAttempts >= 5
