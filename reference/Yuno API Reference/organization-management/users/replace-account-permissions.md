---
title: Replace Account Permissions
api:
  file: organization-management.json
  operationId: replace-account-permissions
deprecated: false
hidden: true
---
Replaces all account permission assignments for a user.

### Important Note

This is a **full replacement** — any existing account permissions not included in the request will be removed.

### Validation Rules

- Each `account_id` must belong to the authenticated organization.
- Each `role_id` must exist and have `admin=false` and `staff=false`.
- Duplicate `account_id` entries are rejected.
- Sending an empty array `[]` removes all account permissions for the user.
