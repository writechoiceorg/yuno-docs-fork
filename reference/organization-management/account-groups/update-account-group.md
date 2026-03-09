---
title: Update Account Group
api:
  file: organization-management.json
  operationId: update-account-group
deprecated: false
hidden: true
---
Updates an account group.

### Path Parameters

| Param | Type | Validation |
| :---- | :---- | :---- |
| account_group_id | path | required, uuid4 |

### Example Request

```json
{
  "name": "e-commerce",
  "merchant_id": "Medellín"
}
```

### Example Response (200 OK)

```json
{
  "id": "f47ac10b-58cc-4372-a567-0e02b2c3d479",
  "name": "Acme Payments",
  "merchant_id": "zuora_submerchant_1",
  "created_at": "2026-03-05T08:00:00.000Z",
  "updated_at": "2026-03-06T08:00:00.000Z"
}
```
