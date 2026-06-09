# Analytics Rule Creation

## Rule Name
Multiple Failed Login Attempts

## Severity
Medium

## Status
Enabled

## MITRE ATT&CK Tactic
Credential Access

## Purpose
Created a Microsoft Sentinel analytics rule to detect multiple failed Windows login attempts that may indicate brute-force activity or password guessing.

## Query Used

```kql
SecurityEvent
| where EventID == 4625
| summarize FailedAttempts = count() by Account, bin(TimeGenerated, 5m)
| where FailedAttempts >= 5
```

## Rule Frequency
Run query every 5 minutes

## Rule Period
Last 5 minutes data

## Rule Threshold
Trigger alert if query returns more than 0 results

## Incident Creation
Enabled

## Learning
Analytics rules help SOC analysts detect suspicious activity by converting security log patterns into alerts and incidents.
