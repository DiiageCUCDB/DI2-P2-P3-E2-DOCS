---
title: "Enregistrement du client"
tags:
  - oauth2
  - configuration
---

# L'enregistrement fixe les règles du client

Caltech Web est enregistré sous le `client_id` **`caltech-web`**. Son backend conserve les jetons.

| | |
|---|---|
| **Identité du client** | `client_id` identifie l'application. Un client confidentiel s'authentifie selon la méthode déclarée. |
| **URI de retour** | Enregistrer **exactement** `https://caltech.example/callback`. Comparer cette valeur à la demande. |
| **Client public** | Une SPA ou une application mobile ne peut pas protéger un secret embarqué. Elle utilise le flux avec [[02-pkce/index\|PKCE]]. |
| **Périmètre de l'accès** | Le serveur connaît les scopes permis et le type de flux autorisé pour ce client. |
