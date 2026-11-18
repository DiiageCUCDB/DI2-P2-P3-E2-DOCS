---
title: "Une preuve en deux requêtes"
tags:
  - pkce
---

# PKCE, une même preuve en deux requêtes

La trace utilise des étiquettes fictives. Les vraies valeurs sont aléatoires.

| Moment | Ce qui se passe |
|---|---|
| **Au départ · garder V** | Caltech conserve le `code_verifier` **V** dans l'état de transaction. Le navigateur transporte uniquement le challenge **C** vers `/authorize`. |
| **Au retour · associer le code à C** | Le Security Server associe le code **A** au challenge **C** lors de son émission. Le navigateur ne transporte que le code de retour et `state`. |
| **À `/token` · envoyer A et V** | Caltech envoie **A** et **V**. Le serveur retrouve **C** à partir de **A** et vérifie le résultat de S256 appliqué à **V**. |
| **Résultat observable** | Avec la preuve attendue et les autres contrôles valides, le serveur délivre les jetons. Une preuve absente ou invalide entraîne un refus. |
