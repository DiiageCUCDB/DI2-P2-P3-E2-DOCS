---
title: "OIDC Messages"
description: "The messages that change when OpenID Connect is added."
tags:
  - type/concept
  - topic/oidc
---

The OIDC request adds `openid` and `nonce` to `/authorize`. The response adds the ID Token to `/token`.

```text
At /authorize
scope=openid%20dossier.read
nonce=<nonce-A>

In the /token response
{"access_token":"<masked>",
 "id_token":"<masked signed JWT>"}

In the ID Token claims
{"sub":"etu-0042", "nonce":"<nonce-A>"}
```

| Element | Role |
|---|---|
| **`openid`** | Enables the identity request. `dossier.read` remains dedicated to the permission to access the API. |
| **`nonce`** | Caltech finds in the ID Token the value it generated for this attempt. |
| **ID Token** | Identity result. After validation, Caltech can open Léa's session. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#ID Token|ID Token]] · [[reference/glossary#nonce|nonce]] · [[reference/glossary#OIDC|OIDC]]
>
> **See also:** [[03-openid-connect/oidc-flow|OIDC Flow]]

← [[03-openid-connect/oidc-flow|OIDC Flow]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/three-tokens|Three Tokens, Three Audiences]] →
