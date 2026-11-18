---
title: "Identité et accès : d'OAuth 2.0 aux passkeys"
tags:
  - index
  - caltech
---

# Identité et accès — projet Caltech

> [!info] DIIAGE / M1 / DI2 P2–P3
> On suit la demande de **Léa**, qui ouvre **Caltech** pour consulter son dossier étudiant, et on enrichit le flux à chaque nouveau besoin.

## Les acteurs du fil rouge

| Acteur | Rôle |
|---|---|
| **Caltech** | Application cliente (backend de l'application web) |
| **Security Server** | Identité et jetons |
| **API Caltech** | Ressource protégée |

## Plan du cours

| # | Partie | Question à laquelle elle répond |
|---|---|---|
| 00 | [[00-introduction/index\|Introduction]] | Que va-t-on démontrer ? |
| 01 | [[01-oauth2/index\|OAuth 2.0]] | Obtenir le droit d'appeler l'API |
| 02 | [[02-pkce/index\|PKCE]] | Lier l'échange du code à sa demande |
| 03 | [[03-openid-connect/index\|OpenID Connect]] | Identifier la personne qui se connecte |
| 04 | [[04-federation/index\|Fédération d'identité]] | S'appuyer sur un fournisseur externe |
| 05 | [[05-mfa/index\|MFA]] | Exiger un facteur supplémentaire selon la politique |
| 06 | [[06-passkeys-webauthn/index\|Passkeys et WebAuthn]] | Inscrire une passkey puis se connecter avec |
| 07 | [[07-annexes/index\|Annexes]] | Projet, atelier, tests de refus, références |
| — | [[glossaire\|Glossaire]] | Vocabulaire du cours |

> [!tip] Méthode
> À chaque étape : on part du **besoin**, on suit les **échanges**, puis on regarde le **résultat**.
