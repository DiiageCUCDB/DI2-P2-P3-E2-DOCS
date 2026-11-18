---
title: "Issuer, Audience, Subject"
description: "Issuer, audience and subject in practice."
tags:
  - type/concept
  - topic/oidc
  - topic/jwt
---

Two tokens signed by the Security Server, each for its own audience.

```json
// ID Token
{"iss":"https://id.caltech.example",
 "aud":"caltech-web",
 "sub":"etu-0042"}

// Access token JWT
{"iss":"https://id.caltech.example",
 "aud":"https://api.caltech.example",
 "sub":"etu-0042", "scope":"dossier.read"}
```

| Claim | Question | Explanation |
|---|---|---|
| **`iss`** | Who issues it? | Must match the configured issuer. Here, both tokens come from the same Security Server. |
| **`aud`** | Who is it for? | Caltech checks `aud=caltech-web` in the ID Token. The API expects its own audience in the access token. |
| **`sub`** | Who is this about? | `sub=etu-0042` identifies Léa at this issuer. Another issuer has its own identifiers. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#iss, aud, sub, exp|iss, aud, sub, exp]] · [[reference/glossary#Claim|Claim]] · [[reference/glossary#ID Token|ID Token]]
>
> **See also:** [[03-openid-connect/three-tokens|Three Tokens, Three Audiences]] · [[03-openid-connect/token-contents|Token Contents]] · [[03-openid-connect/id-token-validation|ID Token Validation]] · [[03-openid-connect/discovery-jwks|Discovery and JWKS]]

← [[03-openid-connect/token-contents|Token Contents]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/discovery-jwks|Discovery and JWKS]] →
