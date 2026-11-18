---
title: "TOTP"
tags:
  - mfa
  - totp
---

# TOTP : enrôlement, connexion et récupération

Exemple de second facteur indépendant du mot de passe.

1. **Enrôler** — après une authentification autorisée, générer un secret propre au compte. Le transmettre à l'application d'authentification et confirmer avec un premier code.
2. **Vérifier** — recalculer le code à partir du secret et du temps. Prévoir une fenêtre courte, limiter les tentatives et refuser un code déjà accepté.
3. **Récupérer** — prévoir un parcours contrôlé pour la perte de l'appareil. Protéger le remplacement du facteur et tracer les changements.

> [!warning]
> Le TOTP utilise un **secret partagé**. Le protéger au repos et le garder hors des journaux.

Référence : RFC 6238.
