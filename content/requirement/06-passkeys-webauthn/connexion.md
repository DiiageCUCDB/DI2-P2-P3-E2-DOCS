---
title: "Connexion par passkey"
tags:
  - passkeys
  - webauthn
  - diagramme
---

# WebAuthn : connexion par signature

Le Security Server vérifie une preuve fraîche liée à son origine.

```mermaid
sequenceDiagram
    participant S as Security Server
    participant N as Navigateur
    participant A as Authentificateur
    S->>N: Options et nouveau challenge
    N->>A: Demande de preuve et vérification locale
    A-->>N: Assertion signée
    N->>S: Assertion et données client
```

> [!important]
> La politique du projet exige la **vérification locale de l'utilisateur (UV)**.
