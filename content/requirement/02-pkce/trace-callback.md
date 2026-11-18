---
title: "Trace retour navigateur"
tags:
  - pkce
  - trace
---

# Retour navigateur : le code lié au challenge

Le Security Server termine l'authentification avant de délivrer le code.

```http
HTTP/1.1 302 Found
Location: https://caltech.example/callback
  ?code=<code-A>&state=<etat-A>
```

État associé au code côté serveur :

```text
client_id · redirect_uri · sujet · scopes
challenge · expiration · statut d'utilisation
```

| Acteur | Action |
|---|---|
| **Côté Caltech** | Récupère la transaction locale et compare `state` avant d'échanger le code. |
| **Côté Security Server** | Crée un code court, à durée de vie limitée et à usage unique, lié à cette requête. |
| **En cas de refus** | Le client traite la réponse d'erreur liée à sa transaction. Une URI invalide ne sert pas à rediriger l'erreur. |
