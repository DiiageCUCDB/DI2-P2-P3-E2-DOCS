---
title: "Principe de PKCE"
tags:
  - pkce
---

# PKCE lie le code à la transaction du client

Le client envoie d'abord l'empreinte, puis la valeur d'origine.

1. **Client** — génère un `code_verifier` aléatoire par transaction. La RFC fixe 43 à 128 caractères autorisés.
2. **`/authorize`** — envoie le `code_challenge` calculé avec S256. Le serveur l'associe ensuite au code d'autorisation.
3. **`/token`** — envoie le verifier. Le serveur recalcule le challenge, compare et **refuse en cas d'écart**.

> [!abstract] Formule
> `S256 = BASE64URL(SHA-256(ASCII(code_verifier)))` sans padding
