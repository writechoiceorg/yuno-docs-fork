---
title: Replace Account Group Permissions
api:
  file: organization-management.json
  operationId: replace-account-group-permissions
deprecated: false
hidden: true
---
Replaces all account group permission assignments for a user.

### Important Note

This is a **full replacement** — any existing account group permissions not included in the request will be removed.

### Validation Rules

- Each `account_group_id` must belong to the authenticated organization.
- Each `role_id` must exist and have `admin=false` and `staff=false`.
- Duplicate `account_group_id` entries are rejected.
- Sending an empty array `[]` removes all account group permissions for the user.
