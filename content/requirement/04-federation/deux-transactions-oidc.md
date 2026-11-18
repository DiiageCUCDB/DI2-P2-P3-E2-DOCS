---
title: "Deux transactions OIDC"
tags:
  - federation
  - diagramme
---

# Fédération : deux transactions OIDC

Transaction **A** pour Caltech. Transaction **B** avec le fournisseur d'identité externe.

```mermaid
sequenceDiagram
    participant C as Caltech
    participant S as Security Server
    participant F as Fournisseur externe
    C->>S: Transaction A : demande Caltech
    S->>F: Transaction B : demande fédérée
    F-->>S: Retour fédéré, échange et identité validée
    S-->>C: Reprise de A, puis émission des jetons Caltech
```

> [!note]
> Les redirections de chaque transaction passent par le navigateur. Chaque flux a ses propres paramètres (`state`, `nonce`, PKCE…).
