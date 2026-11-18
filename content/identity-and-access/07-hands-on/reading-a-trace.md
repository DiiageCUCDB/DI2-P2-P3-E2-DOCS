---
title: "Reading a Trace"
description: "Reading a trace without losing the thread."
tags:
  - type/how-to
  - topic/hands-on
---

Four questions to ask for **every line** of the Caltech trace.

| Question | What to do |
|---|---|
| **Who talks to whom?** | Identify the browser, the Caltech client, the Security Server and the API. With federation, add the external provider. |
| **Which object is passing?** | Name the code or token type, its recipient and the data that binds it to the transaction. |
| **Who decides?** | Spot who authenticates, who validates the return, who issues the tokens and who authorizes reading the record. |
| **Which check explains a denial?** | Distinguish a **transaction** error (`state`, `nonce`, verifier), a **token** error (`iss`, `aud`, `exp`) and a **permission** error (scope or business rule). |

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#iss, aud, sub, exp|iss, aud, sub, exp]] · [[reference/glossary#Scope|Scope]] · [[reference/glossary#nonce|nonce]] · [[reference/glossary#state|state]]
>
> **See also:** [[traces/authorize|/authorize Trace]] · [[traces/callback|Browser Callback Trace]] · [[traces/token|/token Trace]] · [[07-hands-on/workshop|Workshop]]

← [[07-hands-on/project-implementation|Project Implementation]] · [[07-hands-on/index|↑ Hands-On]] · [[07-hands-on/workshop|Workshop]] →
