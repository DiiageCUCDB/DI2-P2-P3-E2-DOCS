---
title: "Authorization Code Flow"
description: "The historical reference flow that lets Caltech obtain an access token for the API."
tags:
  - type/flow
  - topic/oauth2
---

Historical reference flow. It lets Caltech obtain an access token for the API.

```mermaid
sequenceDiagram
    participant N as Browser
    participant C as Client Caltech
    participant S as Security Server
    participant A as API Caltech
    N->>C: GET /dossier
    C-->>N: 302 to /authorize
    N->>S: GET /authorize (client_id, scope, state)
    S-->>N: Léa authenticates, then 302 with code
    N->>C: GET /callback (code, state)
    Note over C,S: Direct exchange between servers
    C->>S: POST /token (code)
    S-->>C: Access token (+ optional refresh token)
    C->>A: API call with the access token
```

> [!warning] Limitation
> Nothing in the code exchange proves it is presented by the client that requested it → [[02-pkce/why-pkce|Why PKCE]].

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#PKCE|PKCE]]
>
> **See also:** [[02-pkce/pkce-flow|Flow with PKCE]] · [[03-openid-connect/oidc-flow|OIDC Flow]] · [[reference/oauth-flows|OAuth Flows and Uses]]

← [[01-oauth2/authorization-code|The Authorization Code]] · [[01-oauth2/index|↑ OAuth 2.0]] · [[02-pkce/index|PKCE]] →
