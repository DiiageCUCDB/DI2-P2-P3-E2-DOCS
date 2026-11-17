---
title: Component Tests
tags: [ocid, testing, cypress]
---

# Component Tests

- **Pattern:** `src/**/__tests__/*.{cy,spec}.{js,ts,jsx,tsx}` (from `cypress.config.ts`).
- **Dev server:** framework `vue`, bundler `vite`.
- **Setup:** `cypress/support/component.ts` registers `cy.mount`.
- **Types:** `tsconfig.cypress-ct.json`, see [[TypeScript and Path Alias]].

Current example, `src/__tests__/App.cy.ts`:

```ts
import App from '../App.vue'

describe('App', () => {
  it('mounts and renders properly', () => {
    cy.mount(App)
    cy.get('h1').should('contain', 'You did it!')
  })
})
```

```sh
npm run test:unit       # headless
npm run test:unit:dev   # interactive
```

> [!note]
> Update this test when the placeholder in `App.vue` is replaced, see [[Open Points]].
