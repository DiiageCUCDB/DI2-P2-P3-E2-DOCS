---
title: "TypeScript and Path Alias"
description: "TypeScript project references and the `@` path alias."
tags:
  - type/concept
  - topic/ocid-frontend
  - topic/architecture
  - topic/typescript
---

## Project references

`tsconfig.json` has no files of its own, only references:

| Config | Scope |
| ------ | ----- |
| `tsconfig.app.json` | `src/**` and `env.d.ts`, excludes `src/**/__tests__/*`. Strict extras: `noUncheckedIndexedAccess`. |
| `tsconfig.node.json` | Node-side config files (Vite, Cypress config, ...) |
| `tsconfig.cypress-ct.json` | Extends the app config and includes `src/**` plus Cypress component support, so tests are type-checked |
| `cypress/tsconfig.json` | Cypress e2e files |

`npm run type-check` runs `vue-tsc --build`. Plain `tsc` cannot read `.vue` files, hence `vue-tsc`.

## Path alias

`@` maps to `src/`, declared twice and kept in sync:

- `vite.config.ts`: `resolve.alias` (runtime and bundling)
- `tsconfig.app.json`: `paths` (type checking and editor)

If you change it, change both.

---

%% footer %%

> [!info] Related
> **Key terms:** [[reference/glossary#Scope|Scope]]
>
> **See also:** [[02-architecture/source-folders|Source Folders]]

← [[02-architecture/routing|Routing]] · [[ocid-frontend/index|↑ Documentation home]] · [[03-development/code-style-and-linting|Code Style and Linting]] →
