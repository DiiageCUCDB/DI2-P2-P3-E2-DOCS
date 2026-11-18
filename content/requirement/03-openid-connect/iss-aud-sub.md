---
title: "Issuer, audience, subject"
tags:
  - oidc
  - jetons
---

# Issuer, audience et subject en pratique

Deux jetons signés par le Security Server, chacun pour son destinataire.

```json
// ID Token
{"iss":"https://id.caltech.example",
 "aud":"caltech-web",
 "sub":"etu-0042"}

// Access token JWT
{"iss":"https://id.caltech.example",
 "aud":"https://api.caltech.example",
 "sub":"etu-0042", "scope":"dossier.read"}
```

| Claim | Question | Explication |
|---|---|---|
| **`iss`** | Qui émet ? | Doit correspondre à l'émetteur configuré. Ici, les deux jetons proviennent du même Security Server. |
| **`aud`** | Pour qui ? | Caltech vérifie `aud=caltech-web` dans l'ID Token. L'API attend sa propre audience dans l'access token. |
| **`sub`** | De qui parle-t-on ? | `sub=etu-0042` identifie Léa chez cet émetteur. Un autre émetteur possède ses propres identifiants. |
