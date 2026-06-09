# Incident Investigation

## Incident Name
Multiple Failed Login Attempts

## Severity
Medium

## Purpose
Investigated the Microsoft Sentinel incident generated after multiple failed Windows login attempts were detected.

## Investigation Steps
Opened the incident in Microsoft Sentinel, reviewed the alert details, checked failed login activity, validated the event using KQL, and mapped the activity to MITRE ATT&CK Credential Access.

## Query Used

```kql
SecurityEvent
| where EventID == 4625
| project TimeGenerated, Computer, Account, Activity, IpAddress
| order by TimeGenerated desc
```

## Observation
Multiple failed login attempts were detected from the Windows endpoint SOC-WIN01. The activity matched the analytics rule condition and generated an incident.

## Learning
Incident investigation helps SOC analysts validate alerts, understand suspicious activity, and decide whether the incident should be escalated.
