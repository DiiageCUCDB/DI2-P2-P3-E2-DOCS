---
title: "Tests de refus"
tags:
  - annexes
  - projet
  - securite
---

# Tests de refus : qui doit arrêter le flux ?

Indiquer le **composant**, son **contrôle** et le **résultat observable**.

| Composant | Cas de refus | Résultat |
|---|---|---|
| **Caltech** | Le `state` retourné ne correspond pas ou le `nonce` de l'ID Token diffère. | Caltech refuse de créer la session. |
| **Security Server** | Le verifier ne correspond pas au challenge ou le code a déjà servi. | `/token` refuse de délivrer les jetons. |
| **API Caltech** | Jeton valide pour une autre audience. | **401** |
| **API Caltech** | Jeton accepté mais dépourvu du droit métier. | **403** |
| **Authentification** | Passkey révoquée, second facteur invalide ou ID Token externe invalide. | Le serveur refuse la connexion concernée. |

Voir aussi [[03-openid-connect/state-nonce-pkce]] et [[03-openid-connect/autorisation-api]].
