---
title: "Messages OIDC"
tags:
  - oidc
  - trace
---

# OpenID Connect : les messages qui changent

La demande OIDC ajoute `openid` et `nonce` à `/authorize`. La réponse ajoute l'ID Token à `/token`.

```text
À /authorize
scope=openid%20dossier.read
nonce=<nonce-A>

Au retour de /token
{"access_token":"<masqué>",
 "id_token":"<JWT signé masqué>"}

Dans les claims de l'ID Token
{"sub":"etu-0042", "nonce":"<nonce-A>"}
```

| Élément | Rôle |
|---|---|
| **`openid`** | Active la demande d'identité. `dossier.read` reste dédié au droit d'accès à l'API. |
| **`nonce`** | Caltech retrouve dans l'ID Token la valeur générée pour cette tentative. |
| **ID Token** | Résultat d'identité. Après validation, Caltech peut ouvrir la session de Léa. |
