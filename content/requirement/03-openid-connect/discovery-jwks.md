---
title: "Discovery et JWKS"
tags:
  - oidc
  - jetons
---

# Découvrir les endpoints et les clés publiques

Discovery fournit les adresses. Le **JWKS** est le jeu de clés publiques de l'émetteur.

1. **Configuration** — fixer l'issuer de confiance. Lire le document de découverte OIDC sur cet émetteur via HTTPS.
2. **Métadonnées** — vérifier que le champ `issuer` correspond. Utiliser `authorization_endpoint`, `token_endpoint` et `jwks_uri`.
3. **Clés publiques** — lire le JWKS annoncé, sélectionner une clé compatible via `kid` et vérifier la signature. Planifier le rafraîchissement du cache.

> [!note]
> `/userinfo` est optionnel dans le parcours. Si utilisé, comparer son `sub` à celui de l'ID Token.
