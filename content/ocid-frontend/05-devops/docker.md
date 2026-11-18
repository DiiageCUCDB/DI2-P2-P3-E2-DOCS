---
title: "Docker"
description: "Production image, nginx configuration and container usage."
tags:
  - type/concept
  - topic/ocid-frontend
  - topic/devops
  - topic/docker
---

## Image (`Dockerfile`)

Two stages:

1. **build** (`node:22-alpine`): `npm ci`, optional `VITE_API_URL` build arg, `npm run build`.
2. **production** (`nginx:1.27-alpine`): copies `nginx.conf` and `dist/`, exposes port 80, healthcheck with `wget` every 30 s.

```sh
docker build --target production \
  --build-arg VITE_API_URL=https://api.example.com \
  -t ocid .
```

## nginx (`nginx.conf`)

- Gzip for text, JSON, JS, XML and SVG.
- **SPA fallback**: `try_files $uri $uri/ /index.html` (needed by history mode, see [[02-architecture/routing|Routing]]).
- `/assets/`: cache for 1 year, `public, immutable` (Vite hashes file names).

## Compose

| File | Use | Port |
| ---- | --- | ---- |
| `compose.yml` | Runs `ghcr.io/diiagecucdb/di2-p2p3-e2-ocid:latest` | 8080 to 80 |
| `compose.dev.yml` | Dev server in `node:22-alpine`, profile `dev`, mounts the repo | 5173 |

```sh
docker compose up -d                                          # http://localhost:8080
docker compose -f compose.dev.yml --profile dev up dev        # http://localhost:5173
```

`.dockerignore` excludes `node_modules`, `dist`, `.git`, `.github`, `.env*`, editor folders, compose files and the README.

Images are published by [[05-devops/ci-cd-pipelines|CI/CD Pipelines]]. Variables: [[05-devops/environment-variables|Environment Variables]].

---

%% footer %%

> [!info] Related
> **See also:** [[05-devops/environment-variables|Environment Variables]] · [[05-devops/ci-cd-pipelines|CI/CD Pipelines]]

← [[04-testing/step-definitions-reference|Step Definitions Reference]] · [[ocid-frontend/index|↑ Documentation home]] · [[05-devops/ci-cd-pipelines|CI/CD Pipelines]] →
