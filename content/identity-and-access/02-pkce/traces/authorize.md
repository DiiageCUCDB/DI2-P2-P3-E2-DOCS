---
title: "/authorize Trace"
description: "What changes in the `/authorize` request."
tags:
  - type/trace
  - topic/pkce
---

Caltech opens a sign-in transaction bound to the browser session.

```http
GET /authorize?response_type=code
  &client_id=caltech-web
  &redirect_uri=https%3A%2F%2Fcaltech.example%2Fcallback
  &scope=dossier.read
  &state=<state-A>
  &code_challenge=<challenge-A>
  &code_challenge_method=S256
```

| Actor | Action |
|---|---|
| **Client** | Generates the transaction values and keeps the PKCE verifier **out of the URL**. |
| **Security Server** | Checks the client, the exact URI, the flow, the scopes and the challenge before continuing. |
| **What the browser sees** | The S256 challenge. The backend keeps the `code_verifier` until the direct call to `/token`. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#PKCE|PKCE]] · [[reference/glossary#Scope|Scope]] · [[reference/glossary#code_verifier|code_verifier]]
>
> **See also:** [[traces/callback|Browser Callback Trace]] · [[traces/token|/token Trace]] · [[07-hands-on/reading-a-trace|Reading a Trace]] · [[01-oauth2/client-registration|Client Registration]]

← [[02-pkce/one-proof-two-requests|One Proof, Two Requests]] · [[02-pkce/index|↑ PKCE]] · [[traces/callback|Browser Callback Trace]] →
