---
title: Get Standalone Transfer
api:
  file: openapi.json
  operationId: get-standalone-transfer
hidden: false
---

Retrieve the current status, provider information, and metadata for a specific transfer using its unique ID. This endpoint provides details on both forward (`SPLIT_TRANSFER`) and reverse (`SPLIT_TRANSFER_REVERSE`) standalone transfers.

## Path Parameters

| Field | Type | Required | Description |
| :---- | :---- | :---- | :---- |
| `transfer_id` | string | yes | The unique ID of the transfer (e.g., `TRF_7kB2mQ9xPnL4vR`). |

## Headers

| Field | Type | Required | Description |
| :---- | :---- | :---- | :---- |
| `PUBLIC-API-KEY` | string | yes | Your Public API Key. |
| `PRIVATE-SECRET-KEY` | string | yes | Your Private Secret Key. |

## Responses

```json Example Response 200 OK (Successful Forward Transfer)
{
  "id": "TRF_7kB2mQ9xPnL4vR",
  "recipient_id": "550e8400-e29b-41d4-a716-446655440000",
  "amount": {
    "value": 150.00,
    "currency": "USD"
  },
  "status": "SUCCEEDED",
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
    "response_message": "Transfer completed"
  },
  "created_at": "2026-02-16T10:30:00Z",
  "updated_at": "2026-02-16T10:30:15Z",
  "completed_at": "2026-02-16T10:30:15Z"
}
```

```json Example Response 200 OK (Successful Reverse Transfer)
{
  "id": "TRF_7kB2mQ9xPnL4vR",
  "recipient_id": "550e8400-e29b-41d4-a716-446655440000",
  "amount": {
    "value": 150.00,
    "currency": "USD"
  },
  "status": "REVERSED",
  "description": "Weekly marketplace earnings",
  "merchant_reference": "TRANSFER-2026-02-15-001",
  "reason": "ORDER_CANCELLED",
  "metadata": [
    {"key": "order_ids", "value": "ORD-123,ORD-124,ORD-125"}
  ],
  "provider_data": {
    "id": "adyen",
    "recipient_id": "SE322KT223222B5CM82WL9TB",
    "transfer_id": "REV_9646307938564031",
    "response_code": "000",
    "response_message": "Reversal completed"
  },
  "created_at": "2026-02-16T10:30:00Z",
  "updated_at": "2026-02-16T11:00:15Z"
}
```
