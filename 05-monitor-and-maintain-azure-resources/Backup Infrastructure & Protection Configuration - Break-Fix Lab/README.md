# Backup Infrastructure & Protection Configuration - Break-Fix Lab

## Lab Overview

This break/fix lab focused on building, validating, intentionally breaking, and troubleshooting an Azure backup environment aligned with AZ-104 administration tasks.

The environment used both a **Recovery Services vault** for Azure VM backup and a **Backup vault** for Azure managed disk protection. Custom backup policies, retention settings, incremental snapshots, managed identities, RBAC permissions, recovery points, and restore workflows were configured and validated before introducing failures.

After establishing a healthy baseline, multiple backup dependencies were intentionally disrupted to reproduce real administrative issues involving protection state, managed identity, RBAC, resource locks, backup schedules, and retention settings. Each failure was investigated using Azure Backup job details, error messages, IAM role assignments, backup-instance status, and recovery-point evidence before applying the minimum required fix and validating recovery.

## Lab Highlights

- Built and validated an Azure backup environment using both a **Recovery Services vault** and a **Backup vault**
- Configured **Enhanced Azure VM backup** with custom scheduling, retention, and Instant Restore settings
- Configured **Azure Disk Backup** using incremental snapshots and a dedicated snapshot resource group
- Implemented **system-assigned managed identity** and least-privilege RBAC with `Disk Backup Reader` and `Disk Snapshot Contributor`
- Validated VM-level and disk-level backup protection through manual backup jobs and recovery points
- Restored a managed disk from a recovery point and reviewed the **OS disk swap** recovery workflow
- Intentionally introduced failures involving backup protection state, managed identity, RBAC, resource locks, schedules, and retention
- Diagnosed failures using Azure Backup job details, error codes, IAM role assignments, backup-instance status, and recovery-point evidence
- Applied minimum-impact fixes and revalidated successful backup operations

## Objectives

- Build a healthy Azure backup environment using a **Recovery Services vault** and a **Backup vault**
- Configure and validate **Azure VM backup** and **Azure managed disk backup**
- Create custom backup policies for scheduling, retention, and Instant Restore
- Configure a dedicated snapshot resource group for Azure Disk Backup recovery points
- Use a **system-assigned managed identity** with least-privilege RBAC permissions
- Validate backup jobs, recovery points, incremental snapshots, and restore operations
- Intentionally break key backup dependencies to reproduce realistic administrative failures
- Troubleshoot issues involving protection state, managed identity, RBAC, resource locks, schedules, and retention
- Apply the minimum required fix for each incident and confirm successful recovery
- 
## Azure Resources and Services Used

- **Azure Virtual Machine** — `vm-backup-01`
- **Recovery Services vault** — `rsv-az104-backup`
- **Backup vault** — `bv-az104-backup`
- **Backup policies** — `vm-daily-lab`, `disk-daily-lab`
- **Managed OS disk** and **incremental snapshots**
- **Snapshot resource group** — `rg-az104-backup-snapshots`
- **System-assigned managed identity**
- **Azure RBAC** — `Disk Backup Reader`, `Disk Snapshot Contributor`
- **Azure Resource Locks**
- **Backup Jobs, Recovery Points, and Managed Disk Restore**

## Healthy Baseline Configuration

- Recovery Services Vault
- Backup Vault
- VM backup policy
- Disk backup policy
- Managed identity + RBAC
- Snapshot resource group
- Successful backup validation
- Successful restore validation

## Break/Fix Incidents

### Incident 1 - VM Backup Protection Disabled
### Incident 2 - Backup Vault Managed Identity Disabled
### Incident 3 - Missing Disk Backup Reader
### Incident 4 - Missing Disk Snapshot Contributor
### Incident 5 - Snapshot Deletion Blocked by Resource Lock
### Incident 6 - VM Backup Policy Schedule Misconfiguration
### Incident 7 - Disk Backup Retention Misconfiguration

## Key Dependency Chains

## Key Lessons Learned
