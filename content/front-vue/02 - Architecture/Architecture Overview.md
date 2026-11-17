---
title: Architecture Overview
tags: [ocid, architecture]
---

# Architecture Overview

OCID is a **single-page application** (SPA). There is no back end in this repository: the app is built to static files and served by nginx. A back-end base URL can be injected at build time, see [[Environment Variables]].

## Stack

| Domain | Tools |
| ------ | ----- |
| Framework | Vue 3 (`<script setup>`), Vue Router 5 |
| Language | TypeScript, SCSS (`sass-embedded`) |
| Build / dev | Vite 8 with `@vitejs/plugin-vue` and `vite-plugin-vue-devtools` |
| Tests | Cypress (component + e2e), Gherkin via `@badeball/cypress-cucumber-preprocessor` |
| Lint / format | oxlint, ESLint, Prettier, EditorConfig |
| Quality | SonarCloud, CodeRabbit |
| Delivery | Docker (Node build, nginx runtime), GHCR, semantic-release |

## Runtime flow

```mermaid
flowchart LR
  index[index.html] --> main[src/main.ts]
  main --> app[App.vue]
  main --> router[src/router]
  router --> views[src/views]
  views --> ui[src/components/ui]
  views --> hooks[src/hooks]
  hooks --> lib[src/lib]
  views --> ctx[src/contexts]
  hooks --> types[src/types]
```

`main.ts` imports `main.scss`, creates the Vue app, installs the router and mounts on `#app`.

## Delivery flow

```mermaid
flowchart LR
  dev[Developer] -->|PR| ci[Test + Sonar workflows]
  ci -->|merge to main| rel[semantic-release]
  rel --> img[Docker image on GHCR]
  img --> nginx[nginx serves dist/]
```

See [[CI-CD Pipelines]] and [[Release Process]].

Related: [[Repository Layout]] · [[Source Folders]]
