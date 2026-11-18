---
title: "Browser Callback Trace"
description: "The browser return: the code is bound to the challenge."
tags:
  - type/trace
  - topic/pkce
---

The Security Server completes authentication before issuing the code.

```http
HTTP/1.1 302 Found
Location: https://caltech.example/callback
  ?code=<code-A>&state=<state-A>
```

State associated with the code on the server side:

```text
client_id · redirect_uri · subject · scopes
challenge · expiry · usage status
```

| Actor | Action |
|---|---|
| **Caltech side** | Retrieves the local transaction and compares `state` before exchanging the code. |
| **Security Server side** | Creates a short-lived, single-use code bound to this request. |
| **On rejection** | The client handles the error response tied to its transaction. An invalid URI is not used to redirect the error. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#state|state]]
>
> **See also:** [[traces/authorize|/authorize Trace]] · [[traces/token|/token Trace]] · [[07-hands-on/reading-a-trace|Reading a Trace]]

← [[traces/authorize|/authorize Trace]] · [[02-pkce/index|↑ PKCE]] · [[traces/token|/token Trace]] →
