---
title: List Account Group Accounts
api:
  file: organization-management.json
  operationId: list-account-group-accounts
deprecated: false
hidden: true
---
Get all accounts of an account group.

### Path Parameters

| Param | Type | Validation |
| :---- | :---- | :---- |
| account_group_id | path | required, uuid4 |

### Example Response (200 OK)

```json
{
"data": [
  {
    "id": "f47ac10b-58cc-4372-a567-0e02b2c3d479",
    "name": "Acme Payments",
    "merchant_id": "zuora_submerchant_1",
    "created_at": "2026-03-05T08:00:00.000Z",
    "updated_at": "2026-03-05T08:00:00.000Z"
  }
],
"pagination": {
   "page": 1,
   "page_size": 20,
   "total_items": 142,
   "total_pages": 8,
   "has_next": true,
   "has_previous": false
 }
}
```
