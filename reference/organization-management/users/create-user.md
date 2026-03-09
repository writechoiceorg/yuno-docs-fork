---
title: Create User
api:
  file: organization-management.json
  operationId: create-user
deprecated: false
hidden: true
---
Creates a new user with optional initial permissions.

> 📘 Note
> The user must be created with at least one permission assignment: either account permissions, account group permissions, or both.

### Validation Rules

- Each `account_id` and `account_group_id` must belong to the authenticated organization.
- Each `role_id` must exist and have `admin=false` and `staff=false`.
- Duplicate entries within the same array are rejected.
