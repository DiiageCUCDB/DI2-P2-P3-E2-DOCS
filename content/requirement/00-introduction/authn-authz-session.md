---
title: "Authentifier, autoriser, ouvrir une session"
tags:
  - introduction
  - concepts
---

# Authentifier, autoriser, ouvrir une session

Trois questions différentes sur la même demande de Léa.

| Notion | Question | Qui / comment |
|---|---|---|
| **Authentification** | Qui ? | Le Security Server vérifie que Léa contrôle les moyens d'authentification associés à son compte. |
| **Autorisation** | Quoi ? | Pour lire le dossier 42, l'API vérifie le droit de lecture et que Léa peut accéder à ce dossier précis. |
| **Session** | Quel lien ? | Après validation de l'identité, le client Caltech associe les requêtes suivantes du navigateur à sa session. |

> [!important]
> Léa est authentifiée. L'API peut lui refuser l'accès à un dossier réservé à un autre étudiant.
