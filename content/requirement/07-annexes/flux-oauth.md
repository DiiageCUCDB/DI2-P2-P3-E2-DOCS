---
title: "Flux OAuth et usages"
tags:
  - annexes
  - oauth2
---

# Les flux OAuth et leurs usages

Le projet utilise **Authorization Code avec PKCE**.

| Flux | Usage |
|---|---|
| **Authorization Code + PKCE** | Flux retenu pour les parcours Caltech. OIDC l'enrichit pour authentifier Léa auprès de Caltech. |
| **Client Credentials** | Utile dans certains échanges entre services. Le sujet représenté est le client, sans utilisateur interactif. |
| **Implicit** | Flux historique. Les pratiques actuelles privilégient l'échange d'un code au point d'entrée `/token`. |
| **Password Grant** | Absent du projet. La recommandation actuelle interdit de l'utiliser. |
