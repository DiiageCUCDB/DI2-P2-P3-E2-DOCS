---
title: "Why WebAuthn"
description: "Why move from passwords to WebAuthn."
tags:
  - type/concept
  - topic/passkeys
  - topic/webauthn
---

Léa can prove her identity with a key bound to the service.

| | |
|---|---|
| **The need** | Reduce dependence on the password and use a proof bound to the service's origin. |
| **What it adds to the flow** | The Security Server starts WebAuthn during authentication. The authenticator answers a **fresh challenge** with a signed proof. |
| **What the server verifies** | The challenge, the origin, the relevant service, the signature and the required flags. |
| **What Caltech receives** | Once the policy is satisfied, the OIDC flow resumes. Caltech gets the same types of tokens. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#OIDC|OIDC]] · [[reference/glossary#WebAuthn and passkeys|WebAuthn and passkeys]]
>
> **See also:** [[05-mfa/factors|The Factors]]

← [[06-passkeys-webauthn/index|Passkeys and WebAuthn]] · [[06-passkeys-webauthn/registration|Passkey Registration]] →
