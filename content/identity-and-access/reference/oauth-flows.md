---
title: "OAuth Flows and Uses"
description: "The OAuth flows and what each is used for."
tags:
  - type/reference
  - topic/reference
---

The project uses **Authorization Code with PKCE**.

| Flow                          | Use                                                                                                           |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **Authorization Code + PKCE** | The flow chosen for the Caltech journeys. OIDC extends it to authenticate Léa to Caltech.                     |
| **Client Credentials**        | Useful in some service-to-service exchanges. The subject represented is the client, with no interactive user. |
| **Implicit**                  | Legacy flow. Current practice favors exchanging a code at the `/token` endpoint.                              |
| **Password Grant**            | Absent from the project. Current recommendations forbid using it.                                             |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Authorization code|Authorization code]] · [[reference/glossary#PKCE|PKCE]] · [[reference/glossary#OIDC|OIDC]]
>
> **See also:** [[01-oauth2/authorization-code-flow|Authorization Code Flow]] · [[02-pkce/pkce-flow|Flow with PKCE]] · [[03-openid-connect/oidc-flow|OIDC Flow]]

[[reference/index|↑ Reference]]
