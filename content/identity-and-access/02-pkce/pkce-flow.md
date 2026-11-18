---
title: "Flow with PKCE"
description: "The Authorization Code flow modified by PKCE."
tags:
  - type/flow
  - topic/pkce
---

The initial request carries the hash. The client presents the original value during the exchange.

```mermaid
sequenceDiagram
    participant N as Browser
    participant C as Caltech Client
    participant S as Security Server
    participant A as API Caltech
    N->>C: GET /dossier
    C-->>N: 302 to /authorize
    N->>S: GET /authorize (code_challenge)
    S-->>N: Léa authenticates, then code bound to the challenge
    N->>C: GET /callback (code, state)
    Note over C,S: Direct exchange between servers
    C->>S: POST /token (code, code_verifier)
    S-->>C: Access token after PKCE verification
    C->>A: API call with the access token
```

Compare with [[01-oauth2/authorization-code-flow|Authorization Code Flow]].

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Authorization code|Authorization code]]
>
> **See also:** [[01-oauth2/authorization-code-flow|Authorization Code Flow]] · [[03-openid-connect/oidc-flow|OIDC Flow]] · [[reference/oauth-flows|OAuth Flows and Uses]]

← [[02-pkce/principle|PKCE Principle]] · [[02-pkce/index|↑ PKCE]] · [[02-pkce/one-proof-two-requests|One Proof, Two Requests]] →
