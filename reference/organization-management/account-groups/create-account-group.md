---
title: Create Account Group
api:
  file: organization-management.json
  operationId: create-account-group
deprecated: false
hidden: true
---
Creates a new group (sub-organization).

### Request Body

| Field | Type | Required | Validation | Description |
| :---- | :---- | :---- | :---- | :---- |
| name | string | yes | min=1, max=255 | Account group name. |
| merchant_id | string | yes | min=1, max=255 | Unique identifier used by the merchant in their systems |

### Example Request

```json
{
  "name": "Acme Payments",
  "merchant_id": "fintech"
}
```

### Example Response (201 Created)

```json
{
  "id": "f47ac10b-58cc-4372-a567-0e02b2c3d479",
  "name": "Acme Payments",
  "merchant_id": "zuora_submerchant_1",
  "created_at": "2026-03-05T08:00:00.000Z",
  "updated_at": "2026-03-05T08:00:00.000Z"
}
```
