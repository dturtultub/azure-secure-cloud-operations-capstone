# Azure RBAC Least-Privilege Access Control

## Goal

Implement and validate least-privilege Azure access by assigning a test user Reader access at the resource group scope.

## Why this matters

Cloud administrators must grant users the minimum access needed to do their job. Assigning broad permissions at the subscription level creates unnecessary security risk.

This lab demonstrates scoped Azure RBAC access, role assignment validation, and the difference between resource permissions and directory administration roles.

## Skills demonstrated

- Microsoft Entra user creation
- Azure RBAC role assignment
- Resource group-level access control
- Reader role validation
- Least-privilege access design
- User Access Administrator role awareness
- Azure RBAC vs Microsoft Entra role separation

## Resources used

- Resource group: `rg-cloudops-governance-dev`
- Test user: `RBAC Test User`
- Assigned role: `Reader`
- Scope: Resource group

## Evidence

| Screenshot | What it proves |
|---|---|
| `screenshots/01-test-user-created.png` | Created a test identity with no initial privileged access. |
| `screenshots/02-resource-group-iam-scope.png` | Opened IAM at the resource group scope, not subscription-wide. |
| `screenshots/03-reader-role-assignment.png` | Selected the Reader role and assigned it to the test user. |
| `screenshots/04-role-assignment-validation.png` | Validated that the test user received Reader access at the resource group scope. |
| `screenshots/05-user-access-administrator-role-info.png` | Identified User Access Administrator as the role used to manage access assignments. |
| `screenshots/06-entra-admin-role-view.png` | Confirmed the test user had no Microsoft Entra administrative roles assigned. |

## Key design decision

The Reader role was assigned at the resource group scope instead of the subscription scope.

This follows least-privilege access design because the user only receives visibility into the specific resource group needed for the lab.

## Real-world explanation

In a real environment, a cloud administrator might need to let a support analyst view resources without allowing them to modify or delete anything.

Assigning Reader at the resource group scope gives visibility without granting unnecessary change permissions.

## What this proves

This lab proves the ability to:

- Create a test identity
- Assign Azure RBAC access at a specific scope
- Validate role assignments
- Apply least-privilege access principles
- Distinguish Azure resource permissions from Microsoft Entra administrative roles

## Resume bullet

Implemented least-privilege Azure RBAC by assigning and validating scoped Reader access at the resource group level, documenting access boundaries between Azure resource roles and Microsoft Entra administrative roles.

## Interview explanation

I created a test user and assigned the Reader role at a resource group scope instead of assigning broad subscription-level access. I validated the assignment from the IAM role assignments view and also checked that the user had no Microsoft Entra administrative roles. The key lesson was that Azure RBAC controls access to Azure resources, while Microsoft Entra roles control tenant and directory administration.

## Common mistake

A common mistake is confusing resource management permissions with access management permissions.

For example, Network Contributor can manage network resources, but it does not allow a user to assign Azure RBAC roles to other users.

To manage access assignments, a user needs Owner or User Access Administrator.