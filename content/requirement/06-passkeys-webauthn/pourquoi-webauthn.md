---
title: "Pourquoi WebAuthn"
tags:
  - passkeys
  - webauthn
---

# Passkeys : pourquoi passer à WebAuthn ?

Léa peut prouver son identité avec une clé liée au service.

| | |
|---|---|
| **Le besoin** | Réduire la dépendance au mot de passe et utiliser une preuve liée à l'origine du service. |
| **L'ajout au flux** | Le Security Server lance WebAuthn pendant l'authentification. L'authentificateur répond à un **défi frais** avec une preuve signée. |
| **Ce que le serveur vérifie** | Le défi, l'origine, le service concerné, la signature et les indicateurs exigés. |
| **Ce que Caltech reçoit** | Après validation de la politique, le flux OIDC reprend. Caltech obtient les mêmes types de jetons. |
