---
title: "Refusal Tests"
description: "Which component must stop the flow, and how it shows."
tags:
  - type/exercise
  - topic/hands-on
---

State the **component**, its **check** and the **observable result**.

| Component | Denial case | Result |
|---|---|---|
| **Caltech** | The returned `state` does not match or the ID Token `nonce` differs. | Caltech refuses to create the session. |
| **Security Server** | The verifier does not match the challenge or the code has already been used. | `/token` refuses to issue the tokens. |
| **API Caltech** | Token valid for another audience. | **401** |
| **API Caltech** | Token accepted but lacking the business permission. | **403** |
| **Authentication** | Revoked passkey, invalid second factor or invalid external ID Token. | The server refuses the sign-in concerned. |

See also [[03-openid-connect/state-nonce-pkce|state, nonce, and PKCE]] and [[03-openid-connect/api-authorization|API-Side Authorization]].

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#nonce|nonce]] · [[reference/glossary#ID Token|ID Token]] · [[reference/glossary#PKCE|PKCE]] · [[reference/glossary#WebAuthn and passkeys|WebAuthn and passkeys]] · [[reference/glossary#state|state]]
>
> **See also:** [[03-openid-connect/id-token-validation|ID Token Validation]] · [[03-openid-connect/state-nonce-pkce|state, nonce, and PKCE]] · [[01-oauth2/client-registration|Client Registration]] · [[07-hands-on/project-implementation|Project Implementation]]

← [[07-hands-on/workshop|Workshop]] · [[07-hands-on/index|↑ Hands-On]]
