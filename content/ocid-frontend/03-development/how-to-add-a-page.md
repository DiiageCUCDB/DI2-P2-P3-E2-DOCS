---
title: "How to Add a Page"
description: "Step-by-step example of adding a view and a route."
tags:
  - type/how-to
  - topic/ocid-frontend
  - topic/development
---

Example: a `/login` page.

## 1. Create the view

`src/views/LoginView.vue` (start from `_templates/view-template.md`):

```vue
<script setup lang="ts"></script>

<template>
  <h1>Login</h1>
</template>
```

## 2. Register the route

`src/router/index.ts`, see [[02-architecture/routing|Routing]]:

```ts
import LoginView from '@/views/LoginView.vue'

routes: [{ path: '/login', name: 'login', component: LoginView }]
```

## 3. Make sure `<RouterView />` is rendered

In `App.vue`, otherwise the route shows nothing.

## 4. Extract reusable pieces

Widgets to `src/components/ui/`, logic to `src/composables/`, see [[02-architecture/source-folders|Source Folders]].

## 5. Describe it in Gherkin

Add `cypress/e2e/login.feature` (start from `_templates/feature-template.md`), reuse steps from [[04-testing/step-definitions-reference|Step Definitions Reference]].

## 6. Check locally

```sh
npm run lint && npm run type-check && npm run test:e2e
```

## 7. Commit

`feat: login page`, see [[03-development/commit-convention|Commit Convention]].

---

%% footer %%

> [!info] Related
> **See also:** [[02-architecture/source-folders|Source Folders]] · [[02-architecture/repository-layout|Repository Layout]] · [[02-architecture/routing|Routing]]

← [[03-development/commit-convention|Commit Convention]] · [[ocid-frontend/index|↑ Documentation home]] · [[04-testing/testing-strategy|Testing Strategy]] →
