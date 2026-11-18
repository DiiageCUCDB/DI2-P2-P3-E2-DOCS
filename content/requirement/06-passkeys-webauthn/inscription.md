---
title: "Inscription d'une passkey"
tags:
  - passkeys
  - webauthn
  - diagramme
---

# WebAuthn : inscription d'une passkey

Le navigateur et l'authentificateur créent une paire de clés liée au service.

```mermaid
sequenceDiagram
    participant S as Security Server
    participant N as Navigateur
    participant A as Authentificateur
    S->>N: Options, challenge, RP ID et compte
    N->>A: Création de la clé après vérification locale
    A-->>N: Credential et données de création
    N->>S: Données de création liées au challenge
```

> [!note]
> Le serveur vérifie la réponse et conserve **l'identifiant de la passkey et sa clé publique**.
