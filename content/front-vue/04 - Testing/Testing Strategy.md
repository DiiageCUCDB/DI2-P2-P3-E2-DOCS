---
title: Testing Strategy
tags: [ocid, testing]
---

# Testing Strategy

Everything runs on **Cypress**.

| Level | Location | Tool | Command |
| ----- | -------- | ---- | ------- |
| Component | `src/**/__tests__/*.cy.ts` | Cypress Component Testing (Vue + Vite) | `npm run test:unit` |
| End-to-end | `cypress/e2e/*.feature` | Cypress + Gherkin | `npm run test:e2e` |
| End-to-end (classic) | `cypress/e2e/*.cy.ts` | Cypress | `npm run test:e2e` |

- Behaviour visible to users is described in Gherkin so that non-developers can read it.
- Component tests cover a component in isolation.
- Both run in CI on every PR, see [[CI-CD Pipelines]].

Details: [[Component Tests]] · [[E2E Gherkin Tests]] · [[Step Definitions Reference]]
