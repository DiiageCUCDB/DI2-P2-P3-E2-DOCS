---
title: "state, nonce et PKCE"
tags:
  - oidc
  - securite
---

# Trois valeurs qui lient les échanges

Les trois valeurs sont distinctes. Dans le projet, chacune est **générée par transaction**.

| Valeur | Vérifiée où ? | Contrôle |
|---|---|---|
| **`state`** | Retour navigateur (Caltech) | Le client vérifie que l'état reçu correspond à la transaction du navigateur. Il refuse un état absent ou différent. |
| **`nonce`** | ID Token (Caltech) | Valeur à usage unique envoyée à `/authorize` et vérifiée dans l'ID Token. |
| **PKCE** | `/token` (Security Server) | Le serveur vérifie le `code_verifier` avant d'émettre les jetons. |
| **Fin de transaction** | Client | Le client invalide les valeurs temporaires lorsque la transaction est terminée. |
