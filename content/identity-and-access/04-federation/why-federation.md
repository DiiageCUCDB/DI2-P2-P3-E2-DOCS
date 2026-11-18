---
title: "Why Federation"
description: "Why Caltech can trust an external identity provider."
tags:
  - type/concept
  - topic/federation
---

Léa already has an account with a trusted external identity provider.

| | |
|---|---|
| **The need** | Allow that account to be used and apply the permissions defined locally in Caltech. |
| **What it adds to the flow** | The Security Server opens a **second OIDC transaction** with the provider and validates the response. |
| **The result** | It links the external identity to the local account, then resumes the Caltech transaction. |
| **Two trust relationships** | The Security Server is the **provider** for Caltech and a **client** of the external identity provider (IdP). |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#IdP|IdP]] · [[reference/glossary#OIDC|OIDC]]

← [[04-federation/index|Identity Federation]] · [[04-federation/two-oidc-transactions|Two OIDC Transactions]] →
