---
title: "Pourquoi PKCE"
tags:
  - pkce
---

# Pourquoi OAuth a ajouté PKCE

*Proof Key for Code Exchange* : preuve liée à l'échange du code.

| | |
|---|---|
| **Le code transite** | Le navigateur ramène le code au client. L'échange du code historique ne comporte aucune preuve propre à cette tentative. |
| **Le problème** | Si le code est intercepté, un client public ne dispose pas d'un secret durable pour s'authentifier auprès du serveur. |
| **La preuve ajoutée** | Le client crée un `code_verifier` aléatoire par tentative. Sa requête initiale transmet l'empreinte, le `code_challenge`. |
| **Le résultat** | Le serveur peut relier l'échange du code à la transaction de départ. Les types de jetons restent les mêmes. |
