---
title: How to Add a Page
tags: [ocid, development, how-to]
---

# How to Add a Page

Example: a `/login` page.

## 1. Create the view

`src/views/LoginView.vue` (start from [[View Template]]):

```vue
<script setup lang="ts"></script>

<template>
  <h1>Login</h1>
</template>
```

## 2. Register the route

`src/router/index.ts`, see [[Routing]]:

```ts
import LoginView from '@/views/LoginView.vue'

routes: [{ path: '/login', name: 'login', component: LoginView }]
```

## 3. Make sure `<RouterView />` is rendered

In `App.vue`, otherwise the route shows nothing.

## 4. Extract reusable pieces

Widgets to `src/components/ui/`, logic to `src/hooks/`, see [[Source Folders]].

## 5. Describe it in Gherkin

Add `cypress/e2e/login.feature` (start from [[Feature Template]]), reuse steps from [[Step Definitions Reference]].

## 6. Check locally

```sh
npm run lint && npm run type-check && npm run test:e2e
```

## 7. Commit

`feat: login page`, see [[Commit Convention]].
