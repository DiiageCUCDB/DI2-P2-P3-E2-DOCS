---
title: "Lire une trace"
tags:
  - annexes
  - atelier
---

# Lire une trace sans perdre le fil

Quatre questions à poser pour **chaque ligne** de la trace Caltech.

| Question | À faire |
|---|---|
| **Qui parle à qui ?** | Identifier le navigateur, le client Caltech, le Security Server et l'API. En fédération, ajouter le fournisseur externe. |
| **Quel objet circule ?** | Nommer le code ou le type de jeton, son destinataire et la donnée qui le lie à la transaction. |
| **Qui décide ?** | Repérer qui authentifie, qui valide le retour, qui délivre les jetons et qui autorise la lecture du dossier. |
| **Quel contrôle explique un refus ?** | Distinguer une erreur de **transaction** (`state`, `nonce`, verifier), de **jeton** (`iss`, `aud`, `exp`) et de **droit** (scope ou règle métier). |
