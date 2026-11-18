---
title: "Scope, rôle et droit sur un dossier"
tags:
  - oauth2
  - autorisation
---

# Scope, rôle et droit sur un dossier

Première demande Caltech : `scope=dossier.read`.

| | |
|---|---|
| **Scope demandé** | Le client indique les accès qu'il souhaite. `dossier.read` est le nom d'une permission d'API définie pour l'exemple Caltech. |
| **Scope accordé** | Le Security Server détermine ce qui est accordé. L'API s'appuie sur la portée accordée, avec ses propres contrôles. |
| **Rôle et règle métier** | Le rôle étudiant décrit un profil. La règle métier vérifie que Léa a le droit d'accéder au dossier demandé. |
| **Exemple de refus** | Le jeton porte `dossier.read`. L'API peut encore refuser la lecture d'un dossier réservé à un autre étudiant. |

Voir aussi [[03-openid-connect/autorisation-api]].
