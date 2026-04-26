# Cost Cleanup

## Cost risk

Low.

This lab used identity and role assignment configuration only. It did not create virtual machines, disks, gateways, load balancers, or other billable compute/network resources.

## Resources created

- Test user: `RBAC Test User`
- Azure RBAC role assignment:
  - Role: `Reader`
  - Scope: `rg-cloudops-governance-dev`

## Cleanup options

If the lab is complete and no longer needed:

1. Remove the Reader role assignment from `RBAC Test User`.
2. Delete the `RBAC Test User` account.
3. Keep the resource group if it is still used by other capstone modules.

## Important note

Deleting the test user does not automatically remove the learning value from the screenshots, but it is cleaner to remove unused identities after evidence is captured.