---
title: "OpenID Connect"
description: "Identify the person who signs in."
tags:
  - type/index
  - topic/oidc
---

## Concepts

- [[03-openid-connect/why-oidc|Why OIDC]] — Why add identity on top of OAuth 2.0.

## The flow

- [[03-openid-connect/oidc-flow|OIDC Flow]] — The flow with identity: Caltech receives an ID Token.
- [[03-openid-connect/messages|OIDC Messages]] — The messages that change when OpenID Connect is added.

## Tokens

- [[03-openid-connect/three-tokens|Three Tokens, Three Audiences]] — Decide where each token travels before deciding where to store it.
- [[03-openid-connect/token-contents|Token Contents]] — What the ID token, access token and refresh token contain.
- [[03-openid-connect/iss-aud-sub|Issuer, Audience, Subject]] — Issuer, audience and subject in practice.

## Trust and validation

- [[03-openid-connect/discovery-jwks|Discovery and JWKS]] — How the client discovers the endpoints and the public keys.
- [[03-openid-connect/id-token-validation|ID Token Validation]] — The client validates the ID Token before creating the session.
- [[03-openid-connect/state-nonce-pkce|state, nonce, and PKCE]] — Three values that bind the exchanges together.

## After sign-in

- [[03-openid-connect/api-authorization|API-Side Authorization]] — The API enforces its own authorization.
- [[03-openid-connect/refresh-revocation-logout|Refresh, Revocation, Logout]] — Renewing, revoking and ending a session.

---

%% footer %%

← [[traces/token|/token Trace]] · [[identity-and-access/index|↑ Course home]] · [[03-openid-connect/why-oidc|Why OIDC]] →
