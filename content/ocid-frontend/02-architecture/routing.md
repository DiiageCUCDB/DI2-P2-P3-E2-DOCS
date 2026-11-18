---
title: "Routing"
description: "Vue Router setup in HTML5 history mode."
tags:
  - type/concept
  - topic/ocid-frontend
  - topic/architecture
  - topic/vue-router
---

Defined in `src/router/index.ts` with Vue Router 5 in **HTML5 history mode**:

```ts
const router = createRouter({
  history: createWebHistory(import.meta.env.BASE_URL),
  routes: [],
})
```

The route table is **empty** for now. Pages will live in `src/views/` ([[02-architecture/source-folders|Source Folders]]) and be registered here ([[03-development/how-to-add-a-page|How to Add a Page]]).

## History mode and the server

History mode needs the server to return `index.html` for unknown paths. `nginx.conf` does this with `try_files $uri $uri/ /index.html`, see [[05-devops/docker|Docker]].

> [!note] `<RouterView>`
> `App.vue` does not render a `<RouterView />` yet. It must be added before routes become visible.

---

%% footer %%

> [!info] Related
> **See also:** [[02-architecture/source-folders|Source Folders]] · [[02-architecture/repository-layout|Repository Layout]] · [[03-development/how-to-add-a-page|How to Add a Page]]

← [[02-architecture/source-folders|Source Folders]] · [[ocid-frontend/index|↑ Documentation home]] · [[02-architecture/typescript-and-path-alias|TypeScript and Path Alias]] →
