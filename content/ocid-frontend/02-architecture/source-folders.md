---
title: "Source Folders"
description: "What goes in each `src/` folder, and what does not."
aliases: [src structure, where to put things]
tags:
  - type/concept
  - topic/ocid-frontend
  - topic/architecture
---

The folders below currently only contain a `.gitkeep`. This note defines **what goes where** so the team stays consistent.

| Folder | Put here | Do not put here |
| ------ | -------- | --------------- |
| `views/` | One component per page/route (`HomeView.vue`, ...). Assembles components and calls hooks. | Reusable widgets |
| `components/ui/` | Generic, reusable UI pieces (buttons, inputs, modals, cards). Props in, events out. | Business logic, API calls |
| `hooks/` | Vue composables `useXxx.ts` wrapping reusable logic (API calls, forms, state helpers). | Pure helpers with no Vue reactivity |
| `contexts/` | State shared across distant components via `provide`/`inject` (session, theme, ...). | Local component state |
| `lib/` | Pure functions, constants, HTTP client, formatters. No Vue dependency. | Composables |
| `types/` | Shared TypeScript types and interfaces (data models, API responses). Entry: `types/index.ts`. | Runtime code |
| `router/` | Route table and guards. See [[02-architecture/routing\|Routing]]. | Page content |
| `__tests__/` | Component tests `*.cy.ts`. See [[04-testing/component-tests\|Component Tests]]. | e2e tests |

## Existing files

- `main.ts`: app entry point.
- `main.scss`: global styles, imported in `main.ts`.
- `App.vue`: root component, currently the Vite placeholder.

## Naming conventions (proposed)

- Components and views: `PascalCase.vue`; views end with `View` (`LoginView.vue`).
- Composables: `useCamelCase.ts`.
- Types: `PascalCase`, grouped per domain in `types/`.

> [!tip] Import style
> Use the `@` alias: `import BaseButton from '@/components/ui/BaseButton.vue'`. See [[02-architecture/typescript-and-path-alias|TypeScript and Path Alias]].

See also: [[03-development/how-to-add-a-page|How to Add a Page]] · [[02-architecture/architecture-overview|Architecture Overview]]

---

%% footer %%

> [!info] Related
> **See also:** [[02-architecture/repository-layout|Repository Layout]] · [[03-development/how-to-add-a-page|How to Add a Page]] · [[02-architecture/routing|Routing]] · [[02-architecture/typescript-and-path-alias|TypeScript and Path Alias]]

← [[02-architecture/repository-layout|Repository Layout]] · [[ocid-frontend/index|↑ Documentation home]] · [[02-architecture/routing|Routing]] →
