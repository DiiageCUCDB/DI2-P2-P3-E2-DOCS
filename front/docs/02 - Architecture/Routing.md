---
title: Routing
tags: [ocid, architecture, vue-router]
---

# Routing

Defined in `src/router/index.ts` with Vue Router 5 in **HTML5 history mode**:

```ts
const router = createRouter({
  history: createWebHistory(import.meta.env.BASE_URL),
  routes: [],
})
```

The route table is **empty** for now. Pages will live in `src/views/` ([[Source Folders]]) and be registered here ([[How to Add a Page]]).

## History mode and the server

History mode needs the server to return `index.html` for unknown paths. `nginx.conf` does this with `try_files $uri $uri/ /index.html`, see [[Docker]].

> [!note] `<RouterView>`
> `App.vue` does not render a `<RouterView />` yet. It must be added before routes become visible.
