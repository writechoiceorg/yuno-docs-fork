---
title: Authenticate User
excerpt: ''
api:
  file: organization-management.json
  operationId: authenticate-user
deprecated: false
hidden: true
metadata:
  title: ''
  description: >-
    Authenticate a whitelabel user and request an Embed Token for secure frontend integration.
  robots: index
next:
  description: ''
---
This request authenticates a whitelabel user within your B2B organization and returns a short-lived JWT (Embed Token). This token is required to authorize the Organization Management dashboard or SDK within your own platform.

> 📘 Security
>
> Always call this endpoint from your secure backend to protect your private API keys.
