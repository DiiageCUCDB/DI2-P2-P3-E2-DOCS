---
title: "Course Objectives"
description: "What the course covers and what you will be able to demonstrate on Caltech."
tags:
  - type/concept
  - topic/introduction
---

## What we will do in class

| Focus | Content |
|---|---|
| **Follow the request** | Identify who acts at each step, from the browser to the API that protects the record. |
| **Enrich the flow** | Start from [[01-oauth2/index\|OAuth 2.0]], add [[02-pkce/index\|PKCE]], then [[03-openid-connect/index\|OpenID Connect]]. Compare the messages and what Caltech receives at each step. |
| **Change the login** | Observe the Security Server when Léa signs in through an [[04-federation/index\|external provider]], a [[05-mfa/index\|second factor]] or a [[06-passkeys-webauthn/index\|passkey]]. |

## What you will be able to demonstrate on Caltech

Léa signs in, returns to Caltech and sees her record. You explain how.

| Skill | Description |
|---|---|
| **Read a trace** | Attribute each redirect and request to the right actor. Distinguish what goes through the browser from what goes between servers. |
| **Explain the controls** | Say where the code is exchanged, where the identity is verified and when the API decides to allow access to the record. |
| **Follow the variants** | Show where the external provider, the second factor and the passkey come into play. |
| **Justify a denial** | Name the control, the component that stops the exchange and the observable result. See [[07-hands-on/refusal-tests\|Refusal Tests]]. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#WebAuthn and passkeys|WebAuthn and passkeys]] · [[reference/glossary#OIDC|OIDC]] · [[reference/glossary#PKCE|PKCE]]

← [[00-introduction/index|Introduction]] · [[00-introduction/lea-journey|Léa's Journey]] →
