---
title: "Passkeys et MFA"
tags:
  - passkeys
  - mfa
---

# Passkeys et MFA dans le flux Caltech

Le flux OIDC reprend après que le Security Server a atteint le niveau requis.

| Cas | Garanties |
|---|---|
| **Mot de passe + TOTP** | Le mot de passe apporte le facteur de connaissance. Le TOTP apporte une preuve de possession du secret enrôlé. |
| **Passkey avec UV** | Le serveur vérifie la preuve de possession de la clé et l'indicateur UV. La politique décide si ces garanties satisfont le MFA requis. |
| **Connexion fédérée** | Le serveur interprète les garanties du fournisseur selon la confiance configurée. Il peut exiger un facteur local supplémentaire. |
| **Refus attendu** | Si le niveau exigé manque, **ne pas émettre le code d'autorisation** pour Caltech. |

Voir [[05-mfa/facteurs]] et [[04-federation/federation-droits]].
