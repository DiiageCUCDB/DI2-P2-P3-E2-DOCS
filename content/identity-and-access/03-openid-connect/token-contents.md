---
title: "Token Contents"
description: "What the ID token, access token and refresh token contain."
tags:
  - type/concept
  - topic/oidc
  - topic/jwt
---

A **claim** is a piece of information declared in a token, with a name and a value.

| | |
|---|---|
| **Token** | Value the server issues to the client. Its use depends on the token type and the intended audience. |
| **JWT · format** | A signed JWT groups a header, claims, and a signature. The signature makes it possible to verify the integrity and origin of this representation. |
| **Claims** | `iss`: issuer · `aud`: audiences · `sub`: subject · `exp`: the instant from which the token expires. |
| **Bearer** | The client presents the access token in the `Authorization` header. Possessing the token is enough to present it, hence the importance of protecting it. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#iss, aud, sub, exp|iss, aud, sub, exp]] · [[reference/glossary#Claim|Claim]] · [[reference/glossary#JWT|JWT]] · [[reference/glossary#Bearer token|Bearer token]]
>
> **See also:** [[03-openid-connect/three-tokens|Three Tokens, Three Audiences]] · [[03-openid-connect/iss-aud-sub|Issuer, Audience, Subject]] · [[03-openid-connect/id-token-validation|ID Token Validation]] · [[03-openid-connect/discovery-jwks|Discovery and JWKS]]

← [[03-openid-connect/three-tokens|Three Tokens, Three Audiences]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/iss-aud-sub|Issuer, Audience, Subject]] →
