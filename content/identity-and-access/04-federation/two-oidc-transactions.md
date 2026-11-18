---
title: "Two OIDC Transactions"
description: "Federation chains two OIDC transactions."
tags:
  - type/flow
  - topic/federation
---

Transaction **A** for Caltech. Transaction **B** with the external identity provider.

```mermaid
sequenceDiagram
    participant C as Caltech
    participant S as Security Server
    participant F as External provider
    C->>S: Transaction A: Caltech request
    S->>F: Transaction B: federated request
    F-->>S: Federated return, exchange and validated identity
    S-->>C: Resume A, then issue Caltech tokens
```

> [!note]
> The redirects of each transaction go through the browser. Each flow has its own parameters (`state`, `nonce`, PKCE…).

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#PKCE|PKCE]] · [[reference/glossary#nonce|nonce]] · [[reference/glossary#state|state]]
>
> **See also:** [[03-openid-connect/oidc-flow|OIDC Flow]]

← [[04-federation/why-federation|Why Federation]] · [[04-federation/index|↑ Identity Federation]] · [[04-federation/federation-and-rights|Federation Identifies, Caltech Decides]] →
