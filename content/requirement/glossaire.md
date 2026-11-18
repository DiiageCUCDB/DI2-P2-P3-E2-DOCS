---
title: "Glossaire"
tags:
  - glossaire
---

# Glossaire

| Terme | Définition (dans le cours) |
|---|---|
| **Resource Owner** | Propriétaire de la ressource au sens OAuth (Léa). |
| **Client** | Application qui demande un droit d'accès (Caltech Web). Voir [[01-oauth2/composants-et-roles]]. |
| **Authorization Server** | Security Server : traite la demande et délivre les jetons. |
| **Resource Server** | API Caltech : protège les dossiers et contrôle l'usage du jeton. |
| **Front channel** | Échanges qui passent par le navigateur (redirections). |
| **Back channel** | Appel direct serveur à serveur par HTTPS (`/token`). |
| **Scope** | Permission demandée / accordée, ex. `dossier.read`. Voir [[01-oauth2/scopes-roles-droits]]. |
| **Code d'autorisation** | Valeur temporaire à usage unique, liée à la demande. |
| **state** | Valeur qui rattache le retour à la transaction du navigateur. |
| **PKCE** | Proof Key for Code Exchange. Voir [[02-pkce/index]]. |
| **code_verifier** | Valeur aléatoire par tentative, gardée par le client. |
| **code_challenge** | Empreinte (S256) du verifier envoyée à `/authorize`. |
| **OIDC** | OpenID Connect : couche d'identité au-dessus d'OAuth 2.0. |
| **RP / OP** | Relying Party (Caltech) / OpenID Provider (Security Server). |
| **ID Token** | JWT signé décrivant l'authentification, destiné au client. |
| **nonce** | Valeur envoyée à `/authorize` et retrouvée dans l'ID Token. |
| **JWT** | En-tête + claims + signature. |
| **Claim** | Information déclarée dans un jeton (nom + valeur). |
| **iss / aud / sub / exp** | Émetteur / destinataires / sujet / expiration. |
| **Bearer** | La possession du jeton suffit pour le présenter. |
| **Discovery / JWKS** | Document de découverte OIDC / jeu de clés publiques de l'émetteur. |
| **IdP** | Fournisseur d'identité externe. Voir [[04-federation/index]]. |
| **acr / amr / auth_time** | Garanties d'authentification transmises par un IdP. |
| **MFA** | Authentification multifacteur. Voir [[05-mfa/index]]. |
| **TOTP** | Code à usage unique basé sur un secret partagé et le temps. |
| **WebAuthn / Passkey** | Preuve signée liée à l'origine du service. Voir [[06-passkeys-webauthn/index]]. |
| **RP ID** | Identifiant du service dans WebAuthn. |
| **UV** | User Verification : vérification locale de l'utilisateur. |
