---
title: "Composants et rôles"
tags:
  - oauth2
---

# Les composants du parcours et les quatre rôles OAuth 2.0

Dans le fil rouge, le **client OAuth est le backend** de l'application web Caltech.

## Composants

| Composant | Rôle dans le parcours |
|---|---|
| **Navigateur** | Suit les redirections et affiche les écrans. Léa y effectue sa connexion. |
| **Client Caltech** | Demande des jetons au Security Server et présente le jeton d'accès à l'API. |
| **Security Server** | Authentifie Léa, applique la politique et délivre les jetons. |
| **API Caltech** | Vérifie le jeton d'accès et décide si Léa peut lire ce dossier. |

> [!note]
> Le navigateur suit les redirections. Le backend Caltech échange le code et appelle l'API.

## Les quatre rôles OAuth 2.0

Une personne et trois rôles techniques.

| Acteur | Rôle OAuth | Description |
|---|---|---|
| **Léa** | Resource Owner | Propriétaire de la ressource. Elle peut autoriser l'accès à son dossier. |
| **Caltech Web** | Client | Application qui demande un droit d'accès à l'API. |
| **Security Server** | Authorization Server | Traite la demande et délivre les jetons d'accès. |
| **API Caltech** | Resource Server | Protège les dossiers et contrôle l'usage du jeton d'accès. |
