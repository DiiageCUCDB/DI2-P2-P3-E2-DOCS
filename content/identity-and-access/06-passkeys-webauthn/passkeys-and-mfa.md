---
title: "Passkeys and MFA"
description: "How passkeys and MFA combine in the Caltech flow."
tags:
  - type/concept
  - topic/passkeys
  - topic/webauthn
---

The OIDC flow resumes after the Security Server has reached the required level.

| Case | Assurance |
|---|---|
| **Password + TOTP** | The password provides the knowledge factor. TOTP provides proof of possession of the enrolled secret. |
| **Passkey with UV** | The server verifies the proof of possession of the key and the UV flag. The policy decides whether this assurance satisfies the required MFA. |
| **Federated sign-in** | The server interprets the provider's assurance according to the configured trust. It may require an additional local factor. |
| **Expected denial** | If the required level is missing, **do not issue the authorization code** to Caltech. |

See [[05-mfa/factors|The Factors]] and [[04-federation/federation-and-rights|Federation Identifies, Caltech Decides]].

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#TOTP|TOTP]] · [[reference/glossary#User Verification (UV)|User Verification (UV)]] · [[reference/glossary#Authorization code|Authorization code]] · [[reference/glossary#MFA|MFA]] · [[reference/glossary#OIDC|OIDC]] · [[reference/glossary#WebAuthn and passkeys|WebAuthn and passkeys]]
>
> **See also:** [[05-mfa/second-factor-before-code|Second Factor Before the Code]]

← [[06-passkeys-webauthn/authentication|Passkey Sign-In]] · [[06-passkeys-webauthn/index|↑ Passkeys and WebAuthn]] · [[07-hands-on/index|Hands-On]] →
