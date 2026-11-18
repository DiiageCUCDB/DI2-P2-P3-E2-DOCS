---
title: "Federation Identifies, Caltech Decides"
description: "Federation identifies; Caltech decides the permissions."
tags:
  - type/concept
  - topic/federation
---

A local account carries the project's permissions and rules.

| | |
|---|---|
| **Configure trust** | Declare the authorized issuer and the Security Server's client with the provider. Validate the callback and the external token. |
| **Link the identity** | Associate the **`(iss, sub)`** pair with the Caltech account. Treat the first link as an explicit, authenticated action. |
| **Assess MFA** | Interpret `acr`, `amr` or `auth_time` according to the assurances agreed with the provider. Add a local factor if the proof is insufficient. |
| **Issue Caltech tokens** | The Security Server applies local roles and issues its own tokens for the client and the API. |

See [[05-mfa/index|MFA]] for the federated case.

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#acr, amr, auth_time|acr, amr, auth_time]] · [[reference/glossary#MFA|MFA]]
>
> **See also:** [[03-openid-connect/api-authorization|API-Side Authorization]] · [[01-oauth2/scopes-roles-rights|Scope, Role, and Record Permission]]

← [[04-federation/two-oidc-transactions|Two OIDC Transactions]] · [[04-federation/index|↑ Identity Federation]] · [[05-mfa/index|MFA]] →
