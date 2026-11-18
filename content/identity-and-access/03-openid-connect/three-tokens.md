---
title: "Three Tokens, Three Audiences"
description: "Decide where each token travels before deciding where to store it."
tags:
  - type/concept
  - topic/oidc
  - topic/jwt
---

Decide where each token **travels** before deciding where to **store** it.

| Object | Audience | Role |
|---|---|---|
| **ID Token** | Caltech client | Describes Léa's authentication. Used to open the session. |
| **Access token** | API Caltech | The client presents it to the API to request access within the granted scope. |
| **Refresh token** | `/token` | Allows requesting a new access token, according to the applicable policy and lifetime. |
| **Caltech session** | Browser | With a backend, the browser receives a **session cookie**. The tokens stay server-side. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#ID Token|ID Token]] · [[reference/glossary#Scope|Scope]]
>
> **See also:** [[03-openid-connect/token-contents|Token Contents]] · [[03-openid-connect/iss-aud-sub|Issuer, Audience, Subject]] · [[03-openid-connect/id-token-validation|ID Token Validation]] · [[03-openid-connect/discovery-jwks|Discovery and JWKS]] · [[03-openid-connect/refresh-revocation-logout|Refresh, Revocation, Logout]]

← [[03-openid-connect/messages|OIDC Messages]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/token-contents|Token Contents]] →
