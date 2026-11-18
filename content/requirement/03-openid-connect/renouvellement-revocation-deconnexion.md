---
title: "Renouvellement, révocation, déconnexion"
tags:
  - oidc
  - jetons
---

# Renouvellement, révocation et déconnexion

Le navigateur, l'application et le Security Server ont des **états distincts**.

| | |
|---|---|
| **Renouveler** | Le client envoie le refresh token à `/token`. Le serveur vérifie sa validité et le lien au client. |
| **Rotation** | À chaque utilisation acceptée, le serveur peut remplacer le refresh token. Un ancien jeton réutilisé peut signaler une compromission. |
| **Déconnecter** | Fermer la session Caltech. Décider aussi quoi faire de la session du Security Server et des jetons distants. |
| **Révoquer** | L'effet sur un access token déjà émis dépend de la stratégie de validation et de sa durée de vie. |

Référence : RFC 7009 (voir [[07-annexes/references]]).
