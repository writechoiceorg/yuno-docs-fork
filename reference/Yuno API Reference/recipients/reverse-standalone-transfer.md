---
title: Reverse Standalone Transfer
type: post
api:
  method: post
  url: /v1/split-marketplace/transfers/{transfer_id}/reverse
---

Reverse a specific standalone transfer. This endpoint allows you to fully or partially reverse a `SUCCEEDED` forward transfer. 

> [!NOTE] Difference between Reversals  
> This endpoint is used **only** for reversing standalone transfers created via the `/v1/split-marketplace/transfers` endpoint. 
> To reverse transfers that are directly linked to a payment lifecycle (`SPLIT_TRANSFER_REVERSAL`), use the `POST /v1/payments/{payment_id}/transactions/{transaction_id}/split-marketplace/transfer-reversal` endpoint instead.

## Path Parameters

| Field | Type | Required | Description |
| :---- | :---- | :---- | :---- |
| `transfer_id` | string | yes | The unique ID of the transfer flow to reverse. |

## Request Body

| Field | Type | Required | Description |
| :---- | :---- | :---- | :---- |
| `account_id` | string | yes | The unique identifier of the account. |
| `amount` | object | no | Used for **Partial Reversals**. Defaults to full amount if omitted. |
| ↳ `value` | number | no | The amount to reverse (must be `<=` the original transfer amount). |
| ↳ `currency` | string | no | The currency (must match the original transfer). |
| `reason` | string | no | The reason for the reversal. |
| `description` | string | no | A human-readable description for the reversal. |
| `merchant_reference` | string | no | Merchant's unique identifier for tracking this reversal. |

## Headers 

| Field | Type | Required | Description |
| :---- | :---- | :---- | :---- |
| `PUBLIC-API-KEY` | string | yes | Your Public API Key. |
| `PRIVATE-SECRET-KEY` | string | yes | Your Private Secret Key. |
| `X-Idempotency-Key` | string | yes | Unique key for request idempotency. |

## Response

```json Example Response 200 OK
{
  "id": "TRF_7kB2mQ9xPnL4vR",
  "recipient_id": "550e8400-e29b-41d4-a716-446655440000",
  "amount": {
    "value": 150.00,
    "currency": "USD"
  },
  "status": "PENDING",
  "reason": "ORDER_CANCELLED",
  "description": "Reversal due to order cancellation",
  "merchant_reference": "REVERSAL-2026-02-16-001",
  "provider_data": {
    "id": "adyen",
    "recipient_id": "SE322KT223222B5CM82WL9TB",
    "transfer_id": "REV_9646307938564031",
    "response_code": "000",
    "response_message": "Reversal initiated"
  },
  "created_at": "2026-02-16T10:30:00Z",
  "updated_at": "2026-02-16T11:00:00Z"
}
```
