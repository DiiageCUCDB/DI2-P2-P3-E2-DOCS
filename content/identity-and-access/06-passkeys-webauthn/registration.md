---
title: "Passkey Registration"
description: "Registering a passkey with WebAuthn."
tags:
  - type/flow
  - topic/passkeys
  - topic/webauthn
---

The browser and the authenticator create a key pair bound to the service.

```mermaid
sequenceDiagram
    participant S as Security Server
    participant N as Browser
    participant A as Authenticator
    S->>N: Options, challenge, RP ID and account
    N->>A: Key creation after local verification
    A-->>N: Credential and creation data
    N->>S: Creation data bound to the challenge
```

> [!note]
> The server verifies the response and stores **the passkey identifier and its public key**.

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#WebAuthn and passkeys|WebAuthn and passkeys]]
>
> **See also:** [[06-passkeys-webauthn/authentication|Passkey Sign-In]]

← [[06-passkeys-webauthn/why-webauthn|Why WebAuthn]] · [[06-passkeys-webauthn/index|↑ Passkeys and WebAuthn]] · [[06-passkeys-webauthn/authentication|Passkey Sign-In]] →
