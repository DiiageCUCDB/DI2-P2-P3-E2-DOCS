---
title: "Validation de l'ID Token"
tags:
  - oidc
  - jetons
  - securite
---

# Le client valide l'ID Token avant la session

Le parcours du cours vérifie **systématiquement la signature**.

```text
En-tête : alg=<algorithme>, kid=<clé>
Claims utiles au client :
iss   <émetteur configuré>
sub   <identifiant du sujet>
aud   caltech-web
exp   <expiration>
iat   <émission>
nonce <nonce-A>
```

| Contrôle | Détail |
|---|---|
| **Origine et intégrité** | Vérifier la signature avec une clé de l'émetteur approuvé et un algorithme autorisé. |
| **Émetteur et destinataire** | Comparer `iss`, vérifier `aud` et contrôler `azp` selon le cas. Vérifier la présence de `sub`. |
| **Fraîcheur et lien au flux** | Contrôler `exp`, `iat` et le `nonce` attendu. **Créer la session après ces contrôles.** |
