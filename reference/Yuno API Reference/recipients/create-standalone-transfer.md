---
title: Create Standalone Transfer
type: post
api:
  method: post
  url: /v1/split-marketplace/transfers
---

Create a forward transfer to distribute funds from your organization balance to your recipients independently of a payment.

### Recipient Validation

Before processing any transfer, we validate the recipient's connection with the payment provider. Ensure your recipient has an `ACTIVE` status and At least one `PENDING` or `SUCCEEDED` onboarding matching the `provider_id`.

## Request Body

| Field | Type | Required | Description |
| :---- | :---- | :---- | :---- |
| `account_id` | string | yes | The unique identifier of the account. |
| `recipient_id` | string | yes | The target recipient identifier. |
| `provider_id` | string | yes | The payment provider code to use (e.g., `adyen`, `stripe`). |
| `amount` | object | yes | Transfer amount and currency. |
| ↳ `value` | number | yes | The monetary value to transfer (must be positive). |
| ↳ `currency` | string | yes | ISO 4217 currency code (e.g., `USD`). |
| `description` | string | no | A human-readable description for the transfer (3-255 chars). This is sent to the provider. |
| `merchant_reference` | string | no | Merchant's unique identifier for idempotency and tracking. |
| `metadata` | array | no | Array of key-value objects for tracking (max 50 pairs). Internal use only. |

## Headers 

> [!IMPORTANT] 
> This endpoint requires the `X-Idempotency-Key` header to safely retry requests without creating duplicate transfers. We retain the key for 24 hours.

| Field | Type | Required | Description |
| :---- | :---- | :---- | :---- |
| `PUBLIC-API-KEY` | string | yes | Your Public API Key. |
| `PRIVATE-SECRET-KEY` | string | yes | Your Private Secret Key. |
| `X-Idempotency-Key` | string | yes | Unique key for request idempotency. |

## Response

```json Example Response 201 Created
{
  "id": "TRF_7kB2mQ9xPnL4vR",
  "recipient_id": "550e8400-e29b-41d4-a716-446655440000",
  "amount": {
    "value": 150.00,
    "currency": "USD"
  },
  "status": "PENDING",
  "description": "Weekly marketplace earnings",
  "merchant_reference": "TRANSFER-2026-02-15-001",
  "metadata": [
    {"key": "order_ids", "value": "ORD-123,ORD-124,ORD-125"},
    {"key": "period", "value": "2026-W07"},
    {"key": "seller_id", "value": "SELLER-999"}
  ],
  "provider_data": {
    "id": "adyen",
    "recipient_id": "SE322KT223222B5CM82WL9TB",
    "transfer_id": "TRF_8535296827453920",
    "response_code": "000",
    "response_message": "Transfer initiated"
  },
  "created_at": "2026-02-16T10:30:00Z",
  "updated_at": "2026-02-16T10:30:00Z"
}
```
