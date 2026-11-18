---
title: "Why MFA"
description: "Why ask for another proof."
tags:
  - type/concept
  - topic/mfa
---

An administrator account gives access to more sensitive functions.

| | |
|---|---|
| **The need** | Limit the consequences of a compromised first factor. |
| **What it adds to the flow** | The Security Server asks for another factor **before issuing the code**. Example: password, then TOTP. |
| **What Caltech receives** | The response keeps the same shape, code then tokens. The policy requires additional assurance about the authentication. |
| **The federated case** | The Security Server examines the assurance passed on by the IdP and may ask for an additional local proof. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#IdP|IdP]] · [[reference/glossary#TOTP|TOTP]]

← [[05-mfa/index|MFA]] · [[05-mfa/factors|The Factors]] →
