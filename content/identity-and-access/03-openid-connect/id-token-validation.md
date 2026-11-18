---
title: "ID Token Validation"
description: "The client validates the ID Token before creating the session."
tags:
  - type/concept
  - topic/oidc
  - topic/jwt
---

The course flow **always verifies the signature**.

```text
Header: alg=<algorithm>, kid=<key>
Claims relevant to the client:
iss   <configured issuer>
sub   <subject identifier>
aud   caltech-web
exp   <expiration>
iat   <issuance>
nonce <nonce-A>
```

| Check | Detail |
|---|---|
| **Origin and integrity** | Verify the signature with a key from the trusted issuer and an allowed algorithm. |
| **Issuer and audience** | Compare `iss`, check `aud`, and check `azp` where applicable. Verify that `sub` is present. |
| **Freshness and link to the flow** | Check `exp`, `iat`, and the expected `nonce`. **Create the session after these checks.** |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#iss, aud, sub, exp|iss, aud, sub, exp]] · [[reference/glossary#nonce|nonce]]
>
> **See also:** [[03-openid-connect/three-tokens|Three Tokens, Three Audiences]] · [[03-openid-connect/token-contents|Token Contents]] · [[03-openid-connect/iss-aud-sub|Issuer, Audience, Subject]] · [[03-openid-connect/discovery-jwks|Discovery and JWKS]] · [[07-hands-on/refusal-tests|Refusal Tests]] · [[03-openid-connect/state-nonce-pkce|state, nonce, and PKCE]] · [[01-oauth2/client-registration|Client Registration]]

← [[03-openid-connect/discovery-jwks|Discovery and JWKS]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/state-nonce-pkce|state, nonce, and PKCE]] →
