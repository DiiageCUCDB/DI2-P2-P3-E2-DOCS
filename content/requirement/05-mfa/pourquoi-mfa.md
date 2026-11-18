---
title: "Pourquoi le MFA"
tags:
  - mfa
---

# MFA : pourquoi demander une autre preuve ?

Un compte administrateur donne accès à des fonctions plus sensibles.

| | |
|---|---|
| **Le besoin** | Limiter les conséquences de la compromission du premier facteur. |
| **L'ajout au flux** | Le Security Server demande un autre facteur **avant d'émettre le code**. Exemple : mot de passe, puis TOTP. |
| **Ce que Caltech reçoit** | La réponse garde la même forme, code puis jetons. La politique exige des garanties supplémentaires sur l'authentification. |
| **Le cas fédéré** | Le Security Server examine les garanties transmises par l'IdP et peut demander une preuve locale supplémentaire. |
