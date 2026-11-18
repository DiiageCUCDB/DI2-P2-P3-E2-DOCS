---
title: "OIDC Flow"
description: "The flow with identity: Caltech receives an ID Token."
tags:
  - type/flow
  - topic/oidc
---

OAuth 2.0 and PKCE stay in place. The client receives the proof of identity when it exchanges the code.

```mermaid
sequenceDiagram
    participant N as Browser
    participant C as Caltech Client
    participant S as Security Server
    participant A as API Caltech
    N->>C: GET /dossier
    C-->>N: 302 to /authorize
    N->>S: GET /authorize (openid, nonce, challenge)
    S-->>N: 302 to the callback after authentication
    N->>C: GET /callback (code, state)
    Note over C,S: Direct server-to-server exchange
    C->>S: POST /token (code, code_verifier)
    S-->>C: ID Token + access token
    C->>A: API call with the access token
    C-->>N: Caltech session and record displayed
```

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#PKCE|PKCE]]
>
> **See also:** [[01-oauth2/authorization-code-flow|Authorization Code Flow]] · [[02-pkce/pkce-flow|Flow with PKCE]] · [[reference/oauth-flows|OAuth Flows and Uses]] · [[03-openid-connect/messages|OIDC Messages]] · [[04-federation/two-oidc-transactions|Two OIDC Transactions]]

← [[03-openid-connect/why-oidc|Why OIDC]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/messages|OIDC Messages]] →
