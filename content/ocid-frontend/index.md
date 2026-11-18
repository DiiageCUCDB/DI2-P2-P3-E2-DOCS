---
title: "OCID Front-End Documentation"
description: "Documentation for the Vue 3 front-end of the DI2-P2P3-E2-OCID project."
aliases: [Index, Start here, MOC]
created: 2026-11-17
tags:
  - type/index
  - topic/ocid-frontend
---

> [!todo] Project purpose
> The repository does not describe what OCID does functionally yet. Fill this in: see [[ocid-frontend/open-points|Open Points]].

Front-end web application of the **DI2-P2P3-E2-OCID** project (GitHub org `DiiageCUCDB`), built with Vue 3, TypeScript and Vite.

## Quick start

```sh
git clone https://github.com/DiiageCUCDB/DI2-P2P3-E2-OCID.git
cd DI2-P2P3-E2-OCID
npm install      # also downloads the Cypress binary
npm run dev      # http://localhost:5173
```

Requires Node.js `^22.18.0` or `>=24.12.0`.

| Command | Purpose |
| ------- | ------- |
| `npm run dev` | Dev server with hot reload |
| `npm run build` | Type-check and production build |
| `npm run lint` | oxlint + ESLint |
| `npm run test:unit` | Cypress component tests |
| `npm run test:e2e` | Gherkin e2e tests |

All scripts: [[01-getting-started/npm-scripts|npm Scripts]].

## Map of content

### Getting Started

- [[01-getting-started/prerequisites|Prerequisites]] — Tools and versions needed before installing.
- [[01-getting-started/installation-and-first-run|Installation and First Run]] — Clone, install and run the app locally for the first time.
- [[01-getting-started/npm-scripts|npm Scripts]] — Every npm script and what it does.

### Architecture

- [[02-architecture/architecture-overview|Architecture Overview]] — The SPA stack and how the pieces fit together.
- [[02-architecture/repository-layout|Repository Layout]] — Annotated tree of the repository.
- [[02-architecture/source-folders|Source Folders]] — What goes in each `src/` folder, and what does not.
- [[02-architecture/routing|Routing]] — Vue Router setup in HTML5 history mode.
- [[02-architecture/typescript-and-path-alias|TypeScript and Path Alias]] — TypeScript project references and the `@` path alias.

### Development

- [[03-development/code-style-and-linting|Code Style and Linting]] — Formatting and linting tools and their rules.
- [[03-development/git-workflow|Git Workflow]] — Branches and the pull-request flow.
- [[03-development/commit-convention|Commit Convention]] — Conventional Commits format read by semantic-release.
- [[03-development/how-to-add-a-page|How to Add a Page]] — Step-by-step example of adding a view and a route.

### Testing

- [[04-testing/testing-strategy|Testing Strategy]] — Test levels, tools and commands.
- [[04-testing/component-tests|Component Tests]] — Cypress component tests: pattern, setup and example.
- [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]] — Gherkin scenarios run end to end with Cypress.
- [[04-testing/step-definitions-reference|Step Definitions Reference]] — Shared Gherkin steps and their implementations.

### DevOps

- [[05-devops/docker|Docker]] — Production image, nginx configuration and container usage.
- [[05-devops/ci-cd-pipelines|CI/CD Pipelines]] — The three GitHub Actions workflows.
- [[05-devops/release-process|Release Process]] — Automated releases with semantic-release.
- [[05-devops/environment-variables|Environment Variables]] — `VITE_*` variables and where they are set.
- [[05-devops/code-quality-services|Code Quality Services]] — SonarCloud and CodeRabbit setup.

### Status

- [[ocid-frontend/open-points|Open Points]] — Questions the repository does not answer yet.

---

%% footer %%

[[01-getting-started/prerequisites|Prerequisites]] →
