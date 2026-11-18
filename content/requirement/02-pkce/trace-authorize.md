---
title: "Trace /authorize"
tags:
  - pkce
  - trace
---

# PKCE : ce qui change dans `/authorize`

Caltech ouvre une transaction de connexion liée à la session du navigateur.

```http
GET /authorize?response_type=code
  &client_id=caltech-web
  &redirect_uri=https%3A%2F%2Fcaltech.example%2Fcallback
  &scope=dossier.read
  &state=<etat-A>
  &code_challenge=<empreinte-A>
  &code_challenge_method=S256
```

| Acteur | Action |
|---|---|
| **Client** | Génère les valeurs de transaction et conserve le verifier de PKCE **hors de l'URL**. |
| **Security Server** | Contrôle le client, l'URI exacte, le flux, les scopes et le challenge avant de poursuivre. |
| **Ce que voit le navigateur** | Le challenge S256. Le backend conserve le `code_verifier` jusqu'à l'appel direct à `/token`. |
