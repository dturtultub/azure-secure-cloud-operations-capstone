{\rtf1\ansi\ansicpg1252\cocoartf2868
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Resource Tagging + Azure Policy Cost Organization\
\
## Goal\
\
Build a governance foundation for a secure Azure cloud operations environment using standardized tags, Azure Policy enforcement, break/fix validation, and cost monitoring.\
\
## Why this matters\
\
Azure environments can become messy and expensive if resources are created without ownership, department, environment, project, or cost-center metadata.\
\
This module demonstrates how a cloud administrator can organize resources, enforce required tags, validate policy behavior, and monitor cost risk.\
\
## Skills demonstrated\
\
- Azure resource group organization\
- Resource tagging standards\
- Azure Policy assignment\
- Policy scope control\
- Deny-based governance enforcement\
- Break/fix troubleshooting\
- Cost analysis\
- Budget alert configuration\
\
## Resources created\
\
- Resource group: `rg-cloudops-governance-dev`\
- Main storage account: `stcloudopsgovdt`\
- Azure Policy assignment: `require-department-tag-governance`\
- Budget: `budget-cloudops-subscription-safety`\
\
## Tagging standard\
\
| Tag | Value |\
|---|---|\
| Department | IT |\
| Environment | Dev |\
| Owner | CloudOpsAdmin |\
| CostCenter | CloudOpsLab |\
| Project | azure-secure-cloud-operations-capstone |\
\
## Evidence\
\
| Screenshot | What it proves |\
|---|---|\
| `screenshots/01-resource-group-tags.png` | Created a governance resource group with standardized tags. |\
| `screenshots/02-storage-account-tags.png` | Applied the same tagging standard to a storage account. |\
| `screenshots/03-policy-assignment-require-department-tag.png` | Assigned Azure Policy to require the Department tag. |\
| `screenshots/04-policy-compliance-view.png` | Checked policy compliance after assignment. |\
| `screenshots/05-missing-department-tag-denied.png` | Verified that a resource missing the required Department tag was denied. |\
| `screenshots/06-policy-fix-success-with-required-tag.png` | Verified that adding the required Department tag allowed deployment. |\
| `screenshots/07-cost-analysis-subscription-view.png` | Reviewed Azure cost analysis while monitoring lab spend. |\
| `screenshots/08-budget-alert-subscription-safety.png` | Created a monthly budget alert to reduce surprise cost risk. |\
\
## Break/fix scenario\
\
A test storage account was intentionally created without the required `Department` tag.\
\
Azure denied the deployment with `RequestDisallowedByPolicy` because the assigned Azure Policy required the tag.\
\
The issue was fixed by creating the resource again with the required `Department` tag.\
\
## What this proves\
\
This module proves the ability to create a basic Azure governance baseline using tags, Azure Policy, cost analysis, and budget alerts.\
\
It also proves practical troubleshooting ability by intentionally causing a policy failure, identifying the reason, and fixing the deployment.\
\
## Resume bullet\
\
Implemented an Azure governance baseline using standardized resource tags, Azure Policy enforcement, break/fix validation, and budget alerts to improve ownership, cost visibility, and deployment control.\
\
## Interview explanation\
\
I created a governance baseline for an Azure environment by applying standardized tags to a resource group and storage account. I then assigned Azure Policy at the resource group scope to require the Department tag. To validate that the policy worked, I intentionally attempted to deploy a storage account without the required tag, confirmed Azure denied the deployment, then fixed the issue by adding the required tag. I also reviewed cost analysis and created a budget alert to reduce cost risk.\
\
## Key lesson\
\
Tags classify resources.\
\
Azure Policy enforces rules.\
\
A Deny policy blocks noncompliant deployments.\
\
Cost Analysis shows spend.\
\
Budgets alert on spend but do not automatically stop all spending.}