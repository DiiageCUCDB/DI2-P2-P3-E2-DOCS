---
title: "PKCE Principle"
description: "PKCE binds the code to the client’s transaction with a verifier and its challenge."
tags:
  - type/concept
  - topic/pkce
---

The client sends the hash first, then the original value.

1. **Client** — generates a random `code_verifier` for each transaction. The RFC allows 43 to 128 characters.
2. **`/authorize`** — sends the `code_challenge` computed with S256. The server then associates it with the authorization code.
3. **`/token`** — sends the verifier. The server recomputes the challenge, compares it, and **rejects on mismatch**.

> [!abstract] Formula
> `S256 = BASE64URL(SHA-256(ASCII(code_verifier)))` without padding

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#code_verifier|code_verifier]] · [[reference/glossary#Authorization code|Authorization code]] · [[reference/glossary#code_challenge|code_challenge]]
>
> **See also:** [[03-openid-connect/state-nonce-pkce|state, nonce, and PKCE]]

← [[02-pkce/why-pkce|Why PKCE]] · [[02-pkce/index|↑ PKCE]] · [[02-pkce/pkce-flow|Flow with PKCE]] →
