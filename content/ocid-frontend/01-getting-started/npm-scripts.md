---
title: "npm Scripts"
description: "Every npm script and what it does."
tags:
  - type/reference
  - topic/ocid-frontend
  - topic/getting-started
---

| Command | What it does |
| ------- | ------------ |
| `npm run dev` | Vite dev server with hot reload (port 5173) |
| `npm run build` | Runs `type-check` and `build-only` in parallel (`run-p`) |
| `npm run build-only` | `vite build`, output in `dist/` |
| `npm run type-check` | `vue-tsc --build`, see [[02-architecture/typescript-and-path-alias\|TypeScript and Path Alias]] |
| `npm run preview` | Serves the production build locally (port 4173) |
| `npm run lint` | `run-s "lint:*"`: oxlint then ESLint, both with `--fix` |
| `npm run lint:oxlint` | `oxlint . --fix` |
| `npm run lint:eslint` | `eslint . --fix --cache` |
| `npm run format` | Prettier on `src/` |
| `npm run test:unit` | Cypress component tests, headless, see [[04-testing/component-tests\|Component Tests]] |
| `npm run test:unit:dev` | Cypress component tests, interactive |
| `npm run test:e2e` | Starts `preview` on 4173 then `cypress run --e2e`, see [[04-testing/e2e-gherkin-tests\|E2E Gherkin Tests]] |
| `npm run test:e2e:dev` | Starts `vite dev --port 4173` then `cypress open --e2e` |
| `npm run prepare` | `cypress install`, runs automatically after `npm install` |

> [!warning] Lint modifies files
> Both lint scripts use `--fix`. Commit or stash your work first if you want to review the changes separately.

---

%% footer %%

> [!info] Related
> **See also:** [[01-getting-started/installation-and-first-run|Installation and First Run]] · [[01-getting-started/prerequisites|Prerequisites]]

← [[01-getting-started/installation-and-first-run|Installation and First Run]] · [[ocid-frontend/index|↑ Documentation home]] · [[02-architecture/architecture-overview|Architecture Overview]] →
