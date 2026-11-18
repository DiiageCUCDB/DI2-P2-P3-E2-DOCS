---
title: "Refresh, Revocation, Logout"
description: "Renewing, revoking and ending a session."
tags:
  - type/concept
  - topic/oidc
---

The browser, the application, and the Security Server have **distinct states**.

| | |
|---|---|
| **Refresh** | The client sends the refresh token to `/token`. The server checks its validity and its binding to the client. |
| **Rotation** | On each accepted use, the server may replace the refresh token. A reused old token can signal a compromise. |
| **Log out** | Close the Caltech session. Also decide what to do with the Security Server session and the remote tokens. |
| **Revoke** | The effect on an already-issued access token depends on the validation strategy and its lifetime. |

Reference: RFC 7009 (see [[reference/references|References]]).

---

%% footer %%

> [!info] Related
> **See also:** [[03-openid-connect/three-tokens|Three Tokens, Three Audiences]]

← [[03-openid-connect/api-authorization|API-Side Authorization]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[04-federation/index|Identity Federation]] →
