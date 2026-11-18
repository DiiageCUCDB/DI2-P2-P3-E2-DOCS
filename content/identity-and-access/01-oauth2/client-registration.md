---
title: "Client Registration"
description: "Registration fixes the rules that apply to the client."
tags:
  - type/concept
  - topic/oauth2
---

Caltech Web is registered under the `client_id` **`caltech-web`**. Its backend stores the tokens.

| | |
|---|---|
| **Client identity** | `client_id` identifies the application. A confidential client authenticates using the declared method. |
| **Redirect URI** | Register **exactly** `https://caltech.example/callback`. Compare this value to the request. |
| **Public client** | An SPA or a mobile application cannot protect an embedded secret. It uses the flow with [[02-pkce/index\|PKCE]]. |
| **Access scope** | The server knows the permitted scopes and the flow type allowed for this client. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Scope|Scope]] · [[reference/glossary#PKCE|PKCE]]
>
> **See also:** [[traces/authorize|/authorize Trace]] · [[07-hands-on/refusal-tests|Refusal Tests]] · [[03-openid-connect/id-token-validation|ID Token Validation]] · [[03-openid-connect/state-nonce-pkce|state, nonce, and PKCE]]

← [[01-oauth2/components-and-roles|Components and Roles]] · [[01-oauth2/index|↑ OAuth 2.0]] · [[01-oauth2/scopes-roles-rights|Scope, Role, and Record Permission]] →
