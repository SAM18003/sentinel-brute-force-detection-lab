# Cleanup and Cost Control

## Resource
SOC-WIN01 Windows VM

## Purpose
Stopped the Azure Windows VM after completing the lab to avoid unnecessary resource usage and reduce cloud cost.

## Action Taken
Stopped the VM after completing testing, log validation, analytics rule creation, and incident investigation.

## Important Note
Stopping the VM helps reduce compute charges, but storage disks, public IPs, Log Analytics data ingestion, and other Azure resources may still create small charges depending on configuration.

## Learning
Cloud lab resources should be stopped, deleted, or monitored after use to avoid unexpected billing.
