---
title: "/token Trace"
description: "What changes in the `/token` request."
tags:
  - type/trace
  - topic/pkce
---

The `/token` endpoint receives a direct request from the client.

```http
POST /token
Content-Type: application/x-www-form-urlencoded
Authorization: Basic <masked-credentials>

grant_type=authorization_code
&code=<code-A>
&redirect_uri=https%3A%2F%2Fcaltech.example%2Fcallback
&code_verifier=<verifier-A>
```

| | |
|---|---|
| **Client identity** | The example uses `client_secret_basic` for the confidential client. A public client presents its `client_id`. |
| **Code consumption** | Checks the client, the URI, expiry, single use and PKCE. Consumes the code **atomically**. |
| **What Caltech receives** | An access token and, if the server issues one, a refresh token. |

Next: [[03-openid-connect/index|OpenID Connect]].

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#OIDC|OIDC]] · [[reference/glossary#PKCE|PKCE]]
>
> **See also:** [[traces/authorize|/authorize Trace]] · [[traces/callback|Browser Callback Trace]] · [[07-hands-on/reading-a-trace|Reading a Trace]]

← [[traces/callback|Browser Callback Trace]] · [[02-pkce/index|↑ PKCE]] · [[03-openid-connect/index|OpenID Connect]] →
