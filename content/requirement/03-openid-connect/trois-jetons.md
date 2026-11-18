---
title: "Trois jetons, trois destinataires"
tags:
  - oidc
  - jetons
---

# Trois jetons, trois destinataires

Décider où chaque jeton **circule** avant de décider où le **conserver**.

| Objet | Destinataire | Rôle |
|---|---|---|
| **ID Token** | Client Caltech | Décrit l'authentification de Léa. Sert à ouvrir la session. |
| **Access token** | API Caltech | Le client le présente à l'API pour demander l'accès dans le périmètre accordé. |
| **Refresh token** | `/token` | Permet de demander un nouvel access token, selon la politique et la durée de vie applicables. |
| **Session Caltech** | Navigateur | Avec un backend, le navigateur reçoit un **cookie de session**. Les jetons restent côté serveur. |
