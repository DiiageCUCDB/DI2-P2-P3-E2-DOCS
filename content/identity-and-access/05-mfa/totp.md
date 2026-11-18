---
title: "TOTP"
description: "TOTP as a second factor: enrollment, sign-in and recovery."
tags:
  - type/concept
  - topic/mfa
  - topic/totp
---

An example of a second factor that is independent of the password.

1. **Enroll** — after an authorized authentication, generate a secret specific to the account. Pass it to the authenticator app and confirm with a first code.
2. **Verify** — recompute the code from the secret and the time. Allow a short window, limit attempts and reject a code that was already accepted.
3. **Recover** — provide a controlled path for a lost device. Protect the replacement of the factor and log the changes.

> [!warning]
> TOTP uses a **shared secret**. Protect it at rest and keep it out of the logs.

Reference: RFC 6238.

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#TOTP|TOTP]]

← [[05-mfa/second-factor-before-code|Second Factor Before the Code]] · [[05-mfa/index|↑ MFA]] · [[06-passkeys-webauthn/index|Passkeys and WebAuthn]] →
