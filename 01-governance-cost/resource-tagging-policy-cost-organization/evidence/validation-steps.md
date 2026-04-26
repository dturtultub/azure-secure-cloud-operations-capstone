# Validation Steps

## 1. Resource group validation

Created resource group:

- `rg-cloudops-governance-dev`

Applied standardized governance tags:

- Department=IT
- Environment=Dev
- Owner=CloudOpsAdmin
- CostCenter=CloudOpsLab
- Project=azure-secure-cloud-operations-capstone

Evidence:

- `screenshots/01-resource-group-tags.png`

## 2. Storage account validation

Created a low-cost storage account inside the governance resource group.

Applied the same tagging standard to the storage account.

Evidence:

- `screenshots/02-storage-account-tags.png`

## 3. Azure Policy validation

Assigned Azure Policy at the resource group scope.

Policy assignment:

- `require-department-tag-governance`

Policy definition:

- `Require a tag on resources`

Required tag:

- `Department`

Policy effect:

- Deny

Evidence:

- `screenshots/03-policy-assignment-require-department-tag.png`
- `screenshots/04-policy-compliance-view.png`

## 4. Break/fix validation

Attempted to create a test storage account without the required `Department` tag.

Result:

- Azure denied the deployment.
- Error code: `RequestDisallowedByPolicy`
- Policy responsible: `require-department-tag-governance`

Evidence:

- `screenshots/05-missing-department-tag-denied.png`

Fixed the issue by creating the storage account again with the required `Department` tag.

Evidence:

- `screenshots/06-policy-fix-success-with-required-tag.png`

## 5. Cost validation

Reviewed Azure Cost Analysis to monitor spend.

Evidence:

- `screenshots/07-cost-analysis-subscription-view.png`

Created a monthly budget alert to reduce surprise cost risk.

Budget:

- `budget-cloudops-subscription-safety`

Evidence:

- `screenshots/08-budget-alert-subscription-safety.png`

## Result

The governance module successfully demonstrates standardized tagging, policy enforcement, break/fix validation, and cost monitoring.