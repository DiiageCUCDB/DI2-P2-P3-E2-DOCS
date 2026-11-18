---
title: "La fédération identifie, Caltech décide"
tags:
  - federation
  - autorisation
---

# La fédération identifie, Caltech décide des droits

Un compte local porte les droits et les règles du projet.

| | |
|---|---|
| **Configurer la confiance** | Déclarer l'émetteur autorisé et le client du Security Server auprès du fournisseur. Contrôler le retour et le jeton externe. |
| **Rattacher l'identité** | Associer le couple **`(iss, sub)`** au compte Caltech. Traiter le premier rattachement comme une action explicite et authentifiée. |
| **Évaluer le MFA** | Interpréter `acr`, `amr` ou `auth_time` selon les garanties convenues avec le fournisseur. Ajouter un facteur local si la preuve est insuffisante. |
| **Émettre les jetons Caltech** | Le Security Server applique les rôles locaux et émet ses propres jetons à destination du client et de l'API. |

Voir [[05-mfa/index]] pour le cas fédéré.
