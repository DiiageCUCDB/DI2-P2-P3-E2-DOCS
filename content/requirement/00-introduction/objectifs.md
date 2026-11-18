---
title: "Objectifs du cours"
tags:
  - introduction
---

# Objectifs du cours

## Ce qu'on va faire en cours

| Axe | Contenu |
|---|---|
| **Suivre la demande** | Repérer qui agit à chaque étape, du navigateur jusqu'à l'API qui protège le dossier. |
| **Enrichir le flux** | Partir d'[[01-oauth2/index\|OAuth 2.0]], ajouter [[02-pkce/index\|PKCE]], puis [[03-openid-connect/index\|OpenID Connect]]. Comparer les messages et ce que Caltech reçoit à chaque étape. |
| **Changer la connexion** | Observer le Security Server quand Léa se connecte via un [[04-federation/index\|fournisseur externe]], un [[05-mfa/index\|second facteur]] ou une [[06-passkeys-webauthn/index\|passkey]]. |

## Ce que vous saurez démontrer sur Caltech

Léa se connecte, revient dans Caltech et voit son dossier. Vous expliquez comment.

| Compétence | Description |
|---|---|
| **Lire une trace** | Attribuer chaque redirection et requête au bon acteur. Distinguer ce qui passe par le navigateur et entre serveurs. |
| **Expliquer les contrôles** | Dire où le code est échangé, où l'identité est vérifiée et à quel moment l'API décide d'autoriser l'accès au dossier. |
| **Suivre les variantes** | Montrer où interviennent le fournisseur externe, le second facteur et la passkey. |
| **Justifier un refus** | Nommer le contrôle, le composant qui arrête l'échange et le résultat observable. Voir [[07-annexes/tests-de-refus]]. |
