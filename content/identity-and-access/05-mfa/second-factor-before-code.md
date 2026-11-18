---
title: "Second Factor Before the Code"
description: "The second factor is required before the authorization code is issued."
tags:
  - type/flow
  - topic/mfa
---

The check takes place on the Security Server during authentication.

```mermaid
sequenceDiagram
    participant N as Léa's browser
    participant S as Security Server
    N->>S: OIDC request with PKCE challenge
    N->>S: Password entry
    S-->>N: First factor validated · second factor requested
    N->>S: Second-factor proof sent
    S-->>N: Redirect with code after validation
```

> [!note]
> The browser returns to Caltech. The exchange at `/token` follows the flow already covered ([[02-pkce/pkce-flow|Flow with PKCE]]).

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#PKCE|PKCE]]
>
> **See also:** [[06-passkeys-webauthn/passkeys-and-mfa|Passkeys and MFA]]

← [[05-mfa/factors|The Factors]] · [[05-mfa/index|↑ MFA]] · [[05-mfa/totp|TOTP]] →
