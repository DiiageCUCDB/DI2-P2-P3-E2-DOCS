---
title: "Component Tests"
description: "Cypress component tests: pattern, setup and example."
tags:
  - type/concept
  - topic/ocid-frontend
  - topic/testing
  - topic/cypress
---

- **Pattern:** `src/**/__tests__/*.{cy,spec}.{js,ts,jsx,tsx}` (from `cypress.config.ts`).
- **Dev server:** framework `vue`, bundler `vite`.
- **Setup:** `cypress/support/component.ts` registers `cy.mount`.
- **Types:** `tsconfig.cypress-ct.json`, see [[02-architecture/typescript-and-path-alias|TypeScript and Path Alias]].

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
> Update this test when the placeholder in `App.vue` is replaced, see [[ocid-frontend/open-points|Open Points]].

---

%% footer %%

> [!info] Related
> **See also:** [[04-testing/testing-strategy|Testing Strategy]] · [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]] · [[04-testing/step-definitions-reference|Step Definitions Reference]]

← [[04-testing/testing-strategy|Testing Strategy]] · [[ocid-frontend/index|↑ Documentation home]] · [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]] →
