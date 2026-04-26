# Cost Cleanup

## Resources created

- Resource group: `rg-cloudops-governance-dev`
- Main storage account: `stcloudopsgovdt`
- Policy assignment: `require-department-tag-governance`
- Budget: `budget-cloudops-subscription-safety`

## Temporary resources

A test storage account was created during break/fix validation to prove Azure Policy enforcement.

The test resource should be deleted after screenshot evidence is captured.

## Cost risk

Low.

This module uses a standard storage account and does not use virtual machines, premium storage, Bastion, NAT Gateway, Application Gateway, or other higher-cost resources.

## Cleanup steps

To fully clean up this module:

1. Delete temporary test storage accounts.
2. Confirm only required resources remain in `rg-cloudops-governance-dev`.
3. If finished with the module, delete the resource group.
4. Remove the policy assignment if it remains visible under Azure Policy.
5. Keep or delete the budget depending on whether more Azure work will continue.

## Important notes

Deleting a resource group deletes the resources inside it.

Azure budgets are alerts, not hard spending limits.

Expensive Azure resources must still be deleted, stopped, or deallocated manually.