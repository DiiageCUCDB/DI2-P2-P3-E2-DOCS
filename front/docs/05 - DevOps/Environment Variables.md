---
title: Environment Variables
tags: [ocid, devops, config]
---

# Environment Variables

Vite exposes only variables prefixed with `VITE_` to client code (`import.meta.env.VITE_*`). They are **baked at build time**, not read at runtime.

| Variable | Used for | Where it is set |
| -------- | -------- | --------------- |
| `VITE_API_URL` | Back-end base URL | Docker build arg; in CI from the repository variable `vars.VITE_API_URL` |

Local development: put values in an `.env.local` file (ignored by git via `*.local`).

> [!warning] Never put secrets in `VITE_*`
> They end up in the public JavaScript bundle.

Secrets used only in CI: `SONAR_TOKEN` (see [[Code Quality Services]]), `GITHUB_TOKEN` (provided by Actions).

See [[Docker]] and [[CI-CD Pipelines]].
