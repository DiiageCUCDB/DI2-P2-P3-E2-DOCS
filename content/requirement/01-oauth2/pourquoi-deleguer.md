---
title: "Pourquoi déléguer l'accès ?"
tags:
  - oauth2
---

# OAuth 2.0 : pourquoi déléguer l'accès ?

Caltech a besoin d'un accès limité à une ressource protégée.

| | |
|---|---|
| **Le besoin** | Lire le dossier au nom de Léa avec un droit limité à cette tâche. |
| **Le principe** | Le Security Server traite la demande et délivre un jeton que Caltech présente à l'API. |
| **Ce que l'on reçoit** | Un access token, éventuellement un refresh token. Le code sert d'intermédiaire dans le parcours interactif. |
| **Ce que l'API décide** | Elle vérifie le jeton et applique ses propres règles sur le dossier demandé. |
