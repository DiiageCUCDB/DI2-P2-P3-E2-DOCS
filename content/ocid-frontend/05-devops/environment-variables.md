---
title: "Environment Variables"
description: "`VITE_*` variables and where they are set."
tags:
  - type/reference
  - topic/ocid-frontend
  - topic/devops
---

Vite exposes only variables prefixed with `VITE_` to client code (`import.meta.env.VITE_*`). They are **baked at build time**, not read at runtime.

| Variable | Used for | Where it is set |
| -------- | -------- | --------------- |
| `VITE_API_URL` | Back-end base URL | Docker build arg; in CI from the repository variable `vars.VITE_API_URL` |

Local development: put values in an `.env.local` file (ignored by git via `*.local`).

> [!warning] Never put secrets in `VITE_*`
> They end up in the public JavaScript bundle.

Secrets used only in CI: `SONAR_TOKEN` (see [[05-devops/code-quality-services|Code Quality Services]]), `GITHUB_TOKEN` (provided by Actions).

See [[05-devops/docker|Docker]] and [[05-devops/ci-cd-pipelines|CI/CD Pipelines]].

---

%% footer %%

> [!info] Related
> **See also:** [[05-devops/docker|Docker]] · [[05-devops/ci-cd-pipelines|CI/CD Pipelines]]

← [[05-devops/release-process|Release Process]] · [[ocid-frontend/index|↑ Documentation home]] · [[05-devops/code-quality-services|Code Quality Services]] →
