---
title: Embed Token (Authentication)
api:
  file: organization-management.json
  operationId: authenticate-user
deprecated: false
hidden: true
---
Authenticates a whitelabel user and returns a JWT embed token. Follows OAuth 2.0 conventions.

### Security

- All authentication failures return a generic error (`LOGIN_FAILED` / "Unable to authenticate the specified user") to prevent entity enumeration.
- The endpoint validates that the user belongs to the organization identified by the API keys.
- Only organizations with the whitelabel property enabled can use this endpoint.

### Token Details

- The JWT includes a `login_method: "whitelabel"` claim to distinguish it from SAML/WorkOS tokens.
- Token expiration: 24 hours (86400 seconds).
- The user must be **ACTIVE** and not deleted.
