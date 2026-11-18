---
title: "Passkey Sign-In"
description: "Signing in with a passkey by signature."
tags:
  - type/flow
  - topic/passkeys
  - topic/webauthn
---

The Security Server verifies a fresh proof bound to its origin.

```mermaid
sequenceDiagram
    participant S as Security Server
    participant N as Browser
    participant A as Authenticator
    S->>N: Options and new challenge
    N->>A: Proof request and local verification
    A-->>N: Signed assertion
    N->>S: Assertion and client data
```

> [!important]
> The project policy requires **local user verification (UV)**.

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#User Verification (UV)|User Verification (UV)]]
>
> **See also:** [[06-passkeys-webauthn/registration|Passkey Registration]]

← [[06-passkeys-webauthn/registration|Passkey Registration]] · [[06-passkeys-webauthn/index|↑ Passkeys and WebAuthn]] · [[06-passkeys-webauthn/passkeys-and-mfa|Passkeys and MFA]] →
