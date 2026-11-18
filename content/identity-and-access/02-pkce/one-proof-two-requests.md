---
title: "One Proof, Two Requests"
description: "One proof carried across `/authorize` and `/token`."
tags:
  - type/concept
  - topic/pkce
---

The trace uses placeholder labels. Real values are random.

| Moment | What happens |
|---|---|
| **At the start · keep V** | Caltech keeps the `code_verifier` **V** in the transaction state. The browser carries only the challenge **C** to `/authorize`. |
| **On return · bind the code to C** | The Security Server binds code **A** to challenge **C** when it issues it. The browser carries only the returned code and `state`. |
| **At `/token` · send A and V** | Caltech sends **A** and **V**. The server looks up **C** from **A** and checks the result of S256 applied to **V**. |
| **Observable result** | With the expected proof and all other checks valid, the server issues the tokens. A missing or invalid proof is rejected. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#code_verifier|code_verifier]] · [[reference/glossary#state|state]]

← [[02-pkce/pkce-flow|Flow with PKCE]] · [[02-pkce/index|↑ PKCE]] · [[traces/authorize|/authorize Trace]] →
