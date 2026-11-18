---
title: "state, nonce, and PKCE"
description: "Three values that bind the exchanges together."
tags:
  - type/concept
  - topic/oidc
---

The three values are distinct. In the project, each one is **generated per transaction**.

| Value | Verified where? | Check |
|---|---|---|
| **`state`** | Browser return (Caltech) | The client checks that the received state matches the browser's transaction. It rejects a missing or different state. |
| **`nonce`** | ID Token (Caltech) | Single-use value sent to `/authorize` and verified in the ID Token. |
| **PKCE** | `/token` (Security Server) | The server verifies the `code_verifier` before issuing the tokens. |
| **End of transaction** | Client | The client invalidates the temporary values once the transaction is complete. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#ID Token|ID Token]] · [[reference/glossary#PKCE|PKCE]] · [[reference/glossary#code_verifier|code_verifier]] · [[reference/glossary#nonce|nonce]] · [[reference/glossary#state|state]]
>
> **See also:** [[02-pkce/principle|PKCE Principle]] · [[07-hands-on/refusal-tests|Refusal Tests]] · [[03-openid-connect/id-token-validation|ID Token Validation]] · [[01-oauth2/client-registration|Client Registration]]

← [[03-openid-connect/id-token-validation|ID Token Validation]] · [[03-openid-connect/index|↑ OpenID Connect]] · [[03-openid-connect/api-authorization|API-Side Authorization]] →
