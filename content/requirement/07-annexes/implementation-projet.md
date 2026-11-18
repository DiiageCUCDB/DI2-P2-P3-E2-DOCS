---
title: "Implémentation du projet"
tags:
  - annexes
  - projet
---

# Ce que vous devez coder dans le projet

Répartition de l'implémentation **sans bibliothèque d'authentification**.

| Composant | À implémenter |
|---|---|
| **Security Server** | Transactions, codes, contrôles, émission et renouvellement des jetons, enrôlement, MFA et intégration WebAuthn. |
| **Caltech et son API** | Démarrage du flux, callback, validation de l'identité, session, validation du jeton d'accès et règles métier. |
| **Fédération** | Client OIDC du Security Server, contrôle du jeton amont et rattachement du compte local. |
| **API natives** | HTTP, JSON, TLS, aléatoire, hachage et signature. Le navigateur fournit son API WebAuthn. |
