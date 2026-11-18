---
title: "Authentication, Authorization, Session"
description: "Authentication, authorization and session answer three different questions about the same request."
tags:
  - type/concept
  - topic/introduction
---

Three different questions about the same request from Léa.

| Concept | Question | Who / how |
|---|---|---|
| **Authentication** | Who? | The Security Server verifies that Léa controls the authentication methods tied to her account. |
| **Authorization** | What? | To read record 42, the API checks the read permission and that Léa may access that specific record. |
| **Session** | Which link? | Once the identity is validated, the Caltech client ties the browser's subsequent requests to her session. |

> [!important]
> Léa is authenticated. The API can still deny her access to a record reserved for another student.

---

%% footer %%

> [!info] Related
> **See also:** [[03-openid-connect/api-authorization|API-Side Authorization]] · [[01-oauth2/why-delegate|Why Delegate Access?]]

← [[00-introduction/lea-journey|Léa's Journey]] · [[00-introduction/index|↑ Introduction]] · [[01-oauth2/index|OAuth 2.0]] →
