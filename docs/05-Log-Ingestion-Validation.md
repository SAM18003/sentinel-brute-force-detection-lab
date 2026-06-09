# Log Ingestion Validation

## Workspace Name
LAW-SOC-LAB

## Endpoint Name
SOC-WIN01

## Purpose
Validated successful Windows Security Event ingestion into Microsoft Sentinel using KQL.

## Query Used

```kql
SecurityEvent
| take 10
```

## Result
Windows Security logs from SOC-WIN01 were successfully received in LAW-SOC-LAB.

## Learning
Log ingestion validation confirms that the endpoint is successfully sending security logs to Microsoft Sentinel for monitoring and investigation.
