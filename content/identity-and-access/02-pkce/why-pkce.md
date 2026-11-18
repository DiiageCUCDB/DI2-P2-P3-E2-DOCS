---
title: "Why PKCE"
description: "Why OAuth added PKCE: nothing proves who presents the code."
tags:
  - type/concept
  - topic/pkce
---

*Proof Key for Code Exchange*: a proof tied to the code exchange.

| | |
|---|---|
| **The code travels** | The browser carries the code back to the client. The original code exchange includes no proof specific to this attempt. |
| **The problem** | If the code is intercepted, a public client has no durable secret to authenticate itself to the server. |
| **The added proof** | The client creates a random `code_verifier` for each attempt. Its initial request sends the hash, the `code_challenge`. |
| **The result** | The server can tie the code exchange to the originating transaction. Token types stay the same. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#code_challenge|code_challenge]] · [[reference/glossary#code_verifier|code_verifier]]
>
> **See also:** [[01-oauth2/authorization-code|The Authorization Code]]

← [[02-pkce/index|PKCE]] · [[02-pkce/principle|PKCE Principle]] →
