---
title: "Project Implementation"
description: "What you must code in the project."
tags:
  - type/exercise
  - topic/hands-on
---

How the implementation is split **without an authentication library**.

| Component | To implement |
|---|---|
| **Security Server** | Transactions, codes, checks, token issuance and renewal, enrollment, MFA and WebAuthn integration. |
| **Caltech and its API** | Flow start, callback, identity validation, session, access token validation and business rules. |
| **Federation** | The Security Server's OIDC client, upstream token checks and linking to the local account. |
| **Native APIs** | HTTP, JSON, TLS, randomness, hashing and signing. The browser provides its own WebAuthn API. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#WebAuthn and passkeys|WebAuthn and passkeys]] · [[reference/glossary#MFA|MFA]] · [[reference/glossary#OIDC|OIDC]]
>
> **See also:** [[07-hands-on/refusal-tests|Refusal Tests]]

← [[07-hands-on/index|Hands-On]] · [[07-hands-on/reading-a-trace|Reading a Trace]] →
