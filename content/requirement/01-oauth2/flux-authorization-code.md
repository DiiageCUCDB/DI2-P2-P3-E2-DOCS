---
title: "Flux Authorization Code"
tags:
  - oauth2
  - diagramme
---

# OAuth 2.0 : le flux Authorization Code

Flux historique de référence. Il permet à Caltech d'obtenir un jeton d'accès pour l'API.

```mermaid
sequenceDiagram
    participant N as Navigateur
    participant C as Client Caltech
    participant S as Security Server
    participant A as API Caltech
    N->>C: GET /dossier
    C-->>N: 302 vers /authorize
    N->>S: GET /authorize (client_id, scope, state)
    S-->>N: Authentification de Léa, puis 302 avec code
    N->>C: GET /callback (code, state)
    Note over C,S: Échange direct entre serveurs
    C->>S: POST /token (code)
    S-->>C: Access token (+ refresh token éventuel)
    C->>A: Appel API avec l'access token
```

> [!warning] Limite
> Rien dans l'échange du code ne prouve qu'il est présenté par le client qui l'a demandé → [[02-pkce/pourquoi-pkce]].
