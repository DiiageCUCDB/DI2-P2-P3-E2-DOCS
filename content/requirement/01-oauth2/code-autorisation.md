---
title: "Le code d'autorisation"
tags:
  - oauth2
  - code
---

# Le code d'autorisation sert de relais

Le code circule d'abord via le navigateur. Les jetons arrivent au client via `/token`.

| | |
|---|---|
| **Front channel** | Le navigateur conduit Léa sur `/authorize` et ramène le code à l'URI de retour du client (le *callback*). |
| **Code d'autorisation** | Valeur temporaire à usage unique liée à la demande. Le client la présente au serveur pour obtenir les jetons. |
| **Back channel** | Le backend Caltech appelle `/token` directement par HTTPS. La réponse contient les jetons destinés au client. |
| **Paramètre `state`** | Caltech le génère pour la demande et le vérifie au retour. Il rattache la réponse à la transaction du navigateur. |
