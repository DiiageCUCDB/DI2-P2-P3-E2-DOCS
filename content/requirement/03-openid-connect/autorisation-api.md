---
title: "Autorisation côté API"
tags:
  - oidc
  - api
  - autorisation
---

# L'API applique sa propre autorisation

Exemple : lecture d'un dossier étudiant avec un access token JWT.

```http
GET /api/dossiers/42
Authorization: Bearer <access-token-masqué>
```

Contrôles de l'API :

1. signature · `iss` · `aud` · expiration
2. scope `dossier.read`
3. règle métier sur le dossier demandé

| Code | Signification |
|---|---|
| **401** | Le jeton est absent, expiré ou invalide, par exemple pour une autre audience. |
| **403** | Le jeton est valide. Le scope manque ou la règle métier interdit l'accès au dossier. |
| **200** | Le jeton et les droits métier permettent la lecture de cette ressource. |
