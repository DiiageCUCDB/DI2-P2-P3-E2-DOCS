---
title: "Les facteurs"
tags:
  - mfa
---

# MFA : les facteurs et leur preuve

La politique porte sur les facteurs **effectivement vérifiés**.

| Catégorie | Définition |
|---|---|
| **Connaissance** | Quelque chose que l'utilisateur sait : mot de passe, PIN. |
| **Possession** | Quelque chose que l'utilisateur possède : appareil détenant une clé privée ou un secret TOTP. |
| **Inhérence** | Une caractéristique de l'utilisateur : biométrie utilisée localement par un authentificateur. |

> [!important] Application au projet
> Pour un compte administrateur, évaluer la politique MFA **à chaque parcours** avant d'émettre le code d'autorisation.
