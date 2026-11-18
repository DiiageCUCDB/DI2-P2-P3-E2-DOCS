---
title: "Identity and Access: From OAuth 2.0 to Passkeys"
description: "Course on delegated access, identity and strong authentication, following Léa’s sign-in to Caltech."
tags:
  - type/index
---

> [!info] DIIAGE / M1 / DI2 P2–P3
> Course by Gaultier Large. We follow the request of **Léa**, who opens **Caltech** to view her student record, and enrich the flow with each new need.

## The actors of the running example

| Actor | Role |
|---|---|
| **Caltech** | Client application (backend of the web application) |
| **Security Server** | Identity and tokens |
| **API Caltech** | Protected resource |

## Course outline

| # | Part | Question it answers |
|---|---|---|
| 00 | [[00-introduction/index\|Introduction]] | What are we going to demonstrate? |
| 01 | [[01-oauth2/index\|OAuth 2.0]] | Get the right to call the API |
| 02 | [[02-pkce/index\|PKCE]] | Bind the code exchange to its request |
| 03 | [[03-openid-connect/index\|OpenID Connect]] | Identify the person who signs in |
| 04 | [[04-federation/index\|Identity Federation]] | Rely on an external provider |
| 05 | [[05-mfa/index\|MFA]] | Require an extra factor according to policy |
| 06 | [[06-passkeys-webauthn/index\|Passkeys and WebAuthn]] | Register a passkey, then sign in with it |
| 07 | [[07-hands-on/index\|Hands-On]] | Project brief, workshop, denial tests |
| — | [[reference/index\|Reference]] | Glossary, flow summary, external references |

> [!tip] Method
> At each step: start from the **need**, follow the **exchanges**, then look at the **result**.

---

%% footer %%

[[00-introduction/index|Introduction]] →
