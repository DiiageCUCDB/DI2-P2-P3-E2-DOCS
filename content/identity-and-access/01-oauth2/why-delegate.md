---
title: "Why Delegate Access?"
description: "Delegation gives Caltech limited access to a protected resource without sharing Léa’s credentials."
tags:
  - type/concept
  - topic/oauth2
---

Caltech needs limited access to a protected resource.

| | |
|---|---|
| **The need** | Read the record on Léa's behalf with a right limited to this task. |
| **The principle** | The Security Server handles the request and issues a token that Caltech presents to the API. |
| **What you receive** | An access token, possibly a refresh token. The code acts as an intermediary in the interactive journey. |
| **What the API decides** | It verifies the token and applies its own rules to the requested record. |

---

%% footer %%

> [!info] Related
> **See also:** [[00-introduction/authn-authz-session|Authentication, Authorization, Session]] · [[03-openid-connect/api-authorization|API-Side Authorization]]

← [[01-oauth2/index|OAuth 2.0]] · [[01-oauth2/components-and-roles|Components and Roles]] →
