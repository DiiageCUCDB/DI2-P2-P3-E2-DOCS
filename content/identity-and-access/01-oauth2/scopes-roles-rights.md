---
title: "Scope, Role, and Record Permission"
description: "How a scope, a role and the permission on a record fit together."
tags:
  - type/concept
  - topic/oauth2
---

First Caltech request: `scope=dossier.read`.

| | |
|---|---|
| **Requested scope** | The client states the access it wants. `dossier.read` is the name of an API permission defined for the Caltech example. |
| **Granted scope** | The Security Server determines what is granted. The API relies on the granted scope, with its own checks. |
| **Role and business rule** | The student role describes a profile. The business rule verifies that Léa has the right to access the requested record. |
| **Denial example** | The token carries `dossier.read`. The API can still deny reading a record reserved for another student. |

See also [[03-openid-connect/api-authorization|API-Side Authorization]].

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Scope|Scope]]
>
> **See also:** [[03-openid-connect/api-authorization|API-Side Authorization]] · [[04-federation/federation-and-rights|Federation Identifies, Caltech Decides]]

← [[01-oauth2/client-registration|Client Registration]] · [[01-oauth2/index|↑ OAuth 2.0]] · [[01-oauth2/authorization-code|The Authorization Code]] →
