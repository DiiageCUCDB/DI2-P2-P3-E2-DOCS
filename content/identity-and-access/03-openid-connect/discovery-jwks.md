---
title: "Discovery and JWKS"
description: "How the client discovers the endpoints and the public keys."
tags:
  - type/concept
  - topic/oidc
  - topic/jwt
---

Discovery provides the addresses. The **JWKS** is the issuer's set of public keys.

1. **Configuration** — fix the trusted issuer. Read the OIDC discovery document for that issuer over HTTPS.
2. **Metadata** — check that the `issuer` field matches. Use `authorization_endpoint`, `token_endpoint`, and `jwks_uri`.
3. **Public keys** — read the advertised JWKS, select a compatible key via `kid`, and verify the signature. Plan for cache refresh.

> [!note]
> `/userinfo` is optional in this flow. If used, compare its `sub` to the one in the ID Token.

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Discovery and JWKS|Discovery and JWKS]] · [[reference/glossary#ID Token|ID Token]] · [[reference/glossary#OIDC|OIDC]] · [[reference/glossary#iss, aud, sub, exp|iss, aud, sub, exp]]
>
> **See also:** [[03-openid-connect/three-tokens|Three Tokens, Three Audiences]] · [[03-openid-connect/token-contents|Token Contents]] · [[03-openid-connect/iss-aud-sub|Issuer, Audience, Subject]] · [[03-openid-connect/id-token-validation|ID Token Validation]]

← [[03-openid-connect/iss-aud-sub|Issuer, Audience, Subject]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/id-token-validation|ID Token Validation]] →
