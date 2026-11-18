---
title: "API-Side Authorization"
description: "The API enforces its own authorization."
tags:
  - type/concept
  - topic/oidc
---

Example: reading a student record with a JWT access token.

```http
GET /api/dossiers/42
Authorization: Bearer <masked-access-token>
```

API checks:

1. signature · `iss` · `aud` · expiration
2. scope `dossier.read`
3. business rule on the requested record

| Code | Meaning |
|---|---|
| **401** | The token is missing, expired, or invalid, for example issued for another audience. |
| **403** | The token is valid. The scope is missing or the business rule forbids access to the record. |
| **200** | The token and the business permissions allow reading this resource. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Scope|Scope]] · [[reference/glossary#iss, aud, sub, exp|iss, aud, sub, exp]] · [[reference/glossary#JWT|JWT]]
>
> **See also:** [[01-oauth2/scopes-roles-rights|Scope, Role, and Record Permission]] · [[04-federation/federation-and-rights|Federation Identifies, Caltech Decides]] · [[00-introduction/authn-authz-session|Authentication, Authorization, Session]] · [[01-oauth2/why-delegate|Why Delegate Access?]]

← [[03-openid-connect/state-nonce-pkce|state, nonce, and PKCE]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/refresh-revocation-logout|Refresh, Revocation, Logout]] →
