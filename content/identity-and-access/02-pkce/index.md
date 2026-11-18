---
title: "PKCE"
description: "Bind the code exchange to the request that started it."
tags:
  - type/index
  - topic/pkce
---

## Concepts

- [[02-pkce/why-pkce|Why PKCE]] — Why OAuth added PKCE: nothing proves who presents the code.
- [[02-pkce/principle|PKCE Principle]] — PKCE binds the code to the client’s transaction with a verifier and its challenge.

## The flow

- [[02-pkce/pkce-flow|Flow with PKCE]] — The Authorization Code flow modified by PKCE.
- [[02-pkce/one-proof-two-requests|One Proof, Two Requests]] — One proof carried across `/authorize` and `/token`.

## Traces

- [[traces/authorize|/authorize Trace]] — What changes in the `/authorize` request.
- [[traces/callback|Browser Callback Trace]] — The browser return: the code is bound to the challenge.
- [[traces/token|/token Trace]] — What changes in the `/token` request.

---

%% footer %%

← [[01-oauth2/authorization-code-flow|Authorization Code Flow]] · [[identity-and-access/index|↑ Course home]] · [[02-pkce/why-pkce|Why PKCE]] →
