---
title: "Contenu des jetons"
tags:
  - oidc
  - jetons
---

# Ce que contiennent les jetons

Un **claim** est une information déclarée dans un jeton, avec un nom et une valeur.

| | |
|---|---|
| **Jeton · token** | Valeur que le serveur délivre au client. Son usage dépend du type de jeton et du destinataire prévu. |
| **JWT · format** | Un JWT signé regroupe un en-tête, des claims et une signature. La signature permet de vérifier l'intégrité et l'origine de cette représentation. |
| **Claims** | `iss` : émetteur · `aud` : destinataires · `sub` : sujet · `exp` : instant à partir duquel le jeton expire. |
| **Bearer** | Le client présente l'access token dans l'en-tête `Authorization`. La possession du jeton suffit pour le présenter, d'où l'importance de le protéger. |
