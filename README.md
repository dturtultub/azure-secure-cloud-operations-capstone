# Secure Azure Cloud Operations Capstone

## Goal

This project builds a secure Azure cloud operations environment designed to demonstrate practical cloud administration, governance, identity, networking, monitoring, backup, and troubleshooting skills.

The purpose is to organize core cloud administration concepts into a smaller set of high-quality Azure operations modules that can be explained clearly in interviews.

## Project sections

| Section | Purpose |
|---|---|
| 01-governance-cost | Tags, Azure Policy, cost organization, budgets, naming standards |
| 02-identity-rbac | Microsoft Entra ID, Azure RBAC, least-privilege access |
| 03-networking | VNets, subnets, NSGs, NICs, routing, private access |
| 04-compute | Virtual machines, cloud-init, extensions, availability |
| 05-storage | Storage accounts, access control, lifecycle rules |
| 06-monitoring-logs | Azure Monitor, Log Analytics, alerts, diagnostic settings |
| 07-backup-recovery | Backup, restore, recovery planning |
| 08-troubleshooting | Break/fix scenarios and validation |
| 09-final-capstone | Final architecture diagram and operational summary |

## Build philosophy

This project avoids toy labs and focuses on tasks that resemble real Azure administrator work.

Each module is designed to show practical implementation, validation evidence, cleanup notes, and a real-world explanation of why the configuration matters.

## Completed modules

### 01-governance-cost/resource-tagging-policy-cost-organization

Built a governance and cost-control foundation using standardized resource tags, Azure Policy enforcement, policy validation, cost visibility, and budget evidence.

### 02-identity-rbac/rbac-least-privilege-access

Implemented least-privilege Azure RBAC by assigning and validating scoped Reader access at the resource group level, while documenting the difference between Azure resource roles and Microsoft Entra administrative roles.

### 03-networking/nsg-and-nic-basics

Built a secure Azure networking foundation with a virtual network, application subnet, subnet-level Network Security Group, custom inbound rules, and private network interfaces.

## Planned modules

### 06-monitoring-logs/azure-monitor-metrics-alerting

Planned module for Azure Monitor, Log Analytics, basic KQL queries, alert rules, and action groups.

### 07-backup-recovery/recovery-services-vault-vm-backup

Planned module for Recovery Services vaults, VM backup, restore options, and recovery validation.

### 05-storage/storage-account-secure-access-lifecycle

Planned module for storage account access control, blob containers, lifecycle management, soft delete, and secure access patterns.

### 04-compute/linux-vm-cloud-init-admin-baseline

Planned module for Linux VM deployment, cloud-init configuration, admin setup, and validation evidence.

## Portfolio value

This capstone demonstrates hands-on Azure administration across governance, identity, networking, monitoring, backup, and troubleshooting.

The goal is to show practical cloud operations skills that can be reviewed in GitHub and explained in technical interviews.
