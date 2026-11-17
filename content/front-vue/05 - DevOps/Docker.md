---
title: Docker
tags: [ocid, devops, docker]
---

# Docker

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
- **SPA fallback**: `try_files $uri $uri/ /index.html` (needed by history mode, see [[Routing]]).
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

Images are published by [[CI-CD Pipelines]]. Variables: [[Environment Variables]].
