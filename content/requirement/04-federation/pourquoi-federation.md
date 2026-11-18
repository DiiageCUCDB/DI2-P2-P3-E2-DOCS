---
title: "Pourquoi la fédération"
tags:
  - federation
---

# Fédération : pourquoi faire confiance à un IdP ?

Léa possède déjà un compte chez un fournisseur d'identité externe approuvé.

| | |
|---|---|
| **Le besoin** | Permettre l'usage de ce compte et appliquer les droits définis localement dans Caltech. |
| **L'ajout au flux** | Le Security Server ouvre une **seconde transaction OIDC** avec le fournisseur et valide la réponse. |
| **Le résultat** | Il associe l'identité externe au compte local, puis reprend la transaction Caltech. |
| **Deux relations de confiance** | Le Security Server est **fournisseur** pour Caltech et **client** du fournisseur d'identité externe (IdP). |
