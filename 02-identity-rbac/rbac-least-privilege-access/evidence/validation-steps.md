# Validation Steps

## 1. Test user validation

Created a Microsoft Entra test user:

- Display name: `RBAC Test User`
- User type: `Member`

Evidence:

- `screenshots/01-test-user-created.png`

## 2. Scope validation

Opened Access control (IAM) from the resource group:

- Resource group: `rg-cloudops-governance-dev`

This confirmed the role assignment would be scoped to a resource group instead of the full subscription.

Evidence:

- `screenshots/02-resource-group-iam-scope.png`

## 3. Role assignment validation

Assigned the following Azure RBAC role:

- User: `RBAC Test User`
- Role: `Reader`
- Scope: `rg-cloudops-governance-dev`

Evidence:

- `screenshots/03-reader-role-assignment.png`

## 4. Assignment confirmation

Confirmed the role assignment appeared under IAM role assignments:

- Principal: `RBAC Test User`
- Type: `User`
- Role: `Reader`
- Scope: `This resource`

Evidence:

- `screenshots/04-role-assignment-validation.png`

## 5. Access delegation role review

Reviewed the User Access Administrator role.

This role is important because it allows management of access to Azure resources.

Evidence:

- `screenshots/05-user-access-administrator-role-info.png`

## 6. Microsoft Entra role separation

Checked the test user's Microsoft Entra assigned roles.

The user had no directory administrative roles assigned.

Evidence:

- `screenshots/06-entra-admin-role-view.png`

## Result

The lab successfully validated least-privilege Azure RBAC access at the resource group scope and showed that Azure RBAC roles are separate from Microsoft Entra administrative roles.