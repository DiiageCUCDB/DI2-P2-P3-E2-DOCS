---
title: "Trace /token"
tags:
  - pkce
  - trace
---

# PKCE : ce qui change dans `/token`

Le point d'entrée `/token` reçoit une requête directe du client.

```http
POST /token
Content-Type: application/x-www-form-urlencoded
Authorization: Basic <identifiants-masqués>

grant_type=authorization_code
&code=<code-A>
&redirect_uri=https%3A%2F%2Fcaltech.example%2Fcallback
&code_verifier=<verifier-A>
```

| | |
|---|---|
| **Identité du client** | L'exemple utilise `client_secret_basic` pour le client confidentiel. Un client public présente son `client_id`. |
| **Consommation du code** | Vérifie le client, l'URI, l'expiration, l'usage unique et PKCE. Consomme le code **de façon atomique**. |
| **Ce que Caltech reçoit** | Un access token et, si le serveur en émet un, un refresh token. |

Suite : [[03-openid-connect/index|OpenID Connect]].
