---
title: "Pourquoi OIDC"
tags:
  - oidc
---

# OpenID Connect : pourquoi ajouter l'identité ?

Caltech sait demander l'accès au dossier. Pour ouvrir une session, il doit aussi savoir **qui** s'est connecté.

| | |
|---|---|
| **La question de Caltech** | Quelle identité le Security Server a-t-il authentifiée pendant cette tentative ? |
| **Ce que Caltech demande en plus** | Il ajoute `openid` à `scope`. Dans le projet, il envoie aussi un `nonce` lié à la transaction. |
| **Ce que Caltech reçoit en plus** | Un **ID Token** signé à `/token`. Caltech le valide avant d'ouvrir la session de Léa. |
| **Les rôles OIDC** | Caltech est le **Relying Party (RP)**. Le Security Server est son **OpenID Provider (OP)**. |
