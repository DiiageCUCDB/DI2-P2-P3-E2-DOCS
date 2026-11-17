---
title: TypeScript and Path Alias
tags: [ocid, architecture, typescript]
---

# TypeScript and Path Alias

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
