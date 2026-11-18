---
title: "Components and Roles"
description: "The components of the journey and the four OAuth 2.0 roles they play."
tags:
  - type/concept
  - topic/oauth2
---

In the running example, the **OAuth client is the backend** of the Caltech web application.

## Components

| Component | Role in the journey |
|---|---|
| **Browser** | Follows redirects and displays screens. Léa signs in there. |
| **Caltech client** | Requests tokens from the Security Server and presents the access token to the API. |
| **Security Server** | Authenticates Léa, applies the policy and issues the tokens. |
| **API Caltech** | Verifies the access token and decides whether Léa can read this record. |

> [!note]
> The browser follows redirects. The Caltech backend exchanges the code and calls the API.

## The four OAuth 2.0 roles

One person and three technical roles.

| Actor | OAuth role | Description |
|---|---|---|
| **Léa** | Resource Owner | Owner of the resource. She can authorize access to her record. |
| **Caltech Web** | Client | Application that requests access rights to the API. |
| **Security Server** | Authorization Server | Handles the request and issues the access tokens. |
| **API Caltech** | Resource Server | Protects the records and controls the use of the access token. |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Authorization Server|Authorization Server]] · [[reference/glossary#Resource Owner|Resource Owner]] · [[reference/glossary#Resource Server|Resource Server]]
>
> **See also:** [[00-introduction/lea-journey|Léa's Journey]]

← [[01-oauth2/why-delegate|Why Delegate Access?]] · [[01-oauth2/index|↑ OAuth 2.0]] · [[01-oauth2/client-registration|Client Registration]] →
