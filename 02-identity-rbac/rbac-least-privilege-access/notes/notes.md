# RBAC vs Microsoft Entra Roles

## What I validated

I created a test user and assigned the Reader role at the resource group scope for `rg-cloudops-governance-dev`.

I then verified that the same user had no Microsoft Entra administrative roles assigned.

## Key lesson

Azure RBAC roles and Microsoft Entra roles are different permission systems.

- Azure RBAC roles control access to Azure resources.
- Microsoft Entra roles control access to tenant and directory administration features.

## Examples

### Azure RBAC roles
- Reader
- Contributor
- Owner
- User Access Administrator

### Microsoft Entra roles
- Global Administrator
- User Administrator
- Groups Administrator
- Security Administrator