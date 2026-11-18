---
title: "The Authorization Code"
description: "The authorization code is a relay between the browser exchange and the direct exchange."
tags:
  - type/concept
  - topic/oauth2
---

The code first travels through the browser. The tokens reach the client through `/token`.

| | |
|---|---|
| **Front channel** | The browser takes Léa to `/authorize` and brings the code back to the client's redirect URI (the *callback*). |
| **Authorization code** | Temporary single-use value tied to the request. The client presents it to the server to obtain the tokens. |
| **Back channel** | The Caltech backend calls `/token` directly over HTTPS. The response contains the tokens intended for the client. |
| **`state` parameter** | Caltech generates it for the request and verifies it on return. It ties the response to the browser's transaction. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Authorization code|Authorization code]] · [[reference/glossary#Back channel|Back channel]] · [[reference/glossary#Front channel|Front channel]] · [[reference/glossary#state|state]]
>
> **See also:** [[02-pkce/why-pkce|Why PKCE]]

← [[01-oauth2/scopes-roles-rights|Scope, Role, and Record Permission]] · [[01-oauth2/index|↑ OAuth 2.0]] · [[01-oauth2/authorization-code-flow|Authorization Code Flow]] →
