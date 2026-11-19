---
title: "Glossary"
description: "Vocabulary used in the course."
tags:
  - type/reference
  - topic/reference
---

Vocabulary used. Each term is linked from the notes that use it.

## Roles and channels

### Resource Owner

Owner of the resource in the OAuth sense (Léa).

### Client

Application asking for an access right (Caltech Web). See [[01-oauth2/components-and-roles|Components and Roles]].

### Authorization Server

The Security Server: processes the request and issues the tokens.

### Resource Server

The Caltech API: protects the records and checks how the token is used.

### Front channel

Exchanges that go through the browser (redirects).

### Back channel

Direct server-to-server call over HTTPS (`/token`).

## OAuth 2.0

### Scope

Permission requested or granted, e.g. `dossier.read`. See [[01-oauth2/scopes-roles-rights|Scope, Role, and Record Permission]].

### Authorization code

Short-lived, single-use value bound to the request.

### state

Value that ties the return to the browser transaction.

## PKCE

### PKCE

Proof Key for Code Exchange. See [[02-pkce/index|PKCE]].

### code_verifier

Random value generated per attempt and kept by the client.

### code_challenge

Hash (S256) of the verifier, sent to `/authorize`.

## OpenID Connect

### OIDC

OpenID Connect: identity layer on top of OAuth 2.0.

### RP and OP

Relying Party (Caltech) and OpenID Provider (Security Server).

### ID Token

Signed JWT describing the authentication, intended for the client.

### nonce

Value sent to `/authorize` and found again in the ID Token.

### JWT

Header, claims and signature.

### Claim

Piece of information asserted in a token (name and value).

### iss, aud, sub, exp

Issuer, audience, subject and expiration.

### Bearer token

Possession of the token is enough to present it.

### Discovery and JWKS

The OIDC discovery document, and the issuer’s set of public keys.

## Federation

### IdP

External identity provider. See [[04-federation/index|Identity Federation]].

### acr, amr, auth_time

Authentication assurances passed on by an IdP.

## MFA and passkeys

### MFA

Multi-factor authentication. See [[05-mfa/index|MFA]].

### TOTP

One-time code based on a shared secret and the current time.

### WebAuthn and passkeys

Signed proof bound to the service’s origin. See [[06-passkeys-webauthn/index|Passkeys and WebAuthn]].

### RP ID

Identifier of the service in WebAuthn.

### User Verification (UV)

Local verification of the user by the authenticator.

---

%% footer %%

[[reference/index|↑ Reference]]
