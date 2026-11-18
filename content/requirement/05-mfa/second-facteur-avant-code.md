---
title: "Second facteur avant le code"
tags:
  - mfa
  - diagramme
---

# MFA : le second facteur avant le code

Le contrôle se déroule sur le Security Server pendant l'authentification.

```mermaid
sequenceDiagram
    participant N as Navigateur de Léa
    participant S as Security Server
    N->>S: Demande OIDC avec challenge PKCE
    N->>S: Saisie du mot de passe
    S-->>N: Premier facteur validé · demande du second
    N->>S: Envoi de la preuve du second facteur
    S-->>N: Redirection avec code après validation
```

> [!note]
> Le navigateur revient à Caltech. L'échange à `/token` suit le flux déjà vu ([[02-pkce/flux-pkce]]).
