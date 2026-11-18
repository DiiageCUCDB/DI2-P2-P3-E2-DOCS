---
title: "Why OIDC"
description: "Why add identity on top of OAuth 2.0."
tags:
  - type/concept
  - topic/oidc
---

Caltech knows how to request access to the record. To open a session, it also needs to know **who** signed in.

| | |
|---|---|
| **Caltech's question** | Which identity did the Security Server authenticate during this attempt? |
| **What Caltech additionally requests** | It adds `openid` to `scope`. In the project, it also sends a `nonce` bound to the transaction. |
| **What Caltech additionally receives** | A signed **ID Token** from `/token`. Caltech validates it before opening Léa's session. |
| **The OIDC roles** | Caltech is the **Relying Party (RP)**. The Security Server is its **OpenID Provider (OP)**. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#RP and OP|RP and OP]] · [[reference/glossary#ID Token|ID Token]] · [[reference/glossary#OIDC|OIDC]] · [[reference/glossary#Scope|Scope]] · [[reference/glossary#nonce|nonce]]

← [[03-openid-connect/index|OpenID Connect]] · [[03-openid-connect/oidc-flow|OIDC Flow]] →
