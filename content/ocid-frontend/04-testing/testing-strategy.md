---
title: "Testing Strategy"
description: "Test levels, tools and commands."
tags:
  - type/concept
  - topic/ocid-frontend
  - topic/testing
  - topic/cypress
---

Everything runs on **Cypress**.

| Level | Location | Tool | Command |
| ----- | -------- | ---- | ------- |
| Component | `src/**/__tests__/*.cy.ts` | Cypress Component Testing (Vue + Vite) | `npm run test:unit` |
| End-to-end | `cypress/e2e/*.feature` | Cypress + Gherkin | `npm run test:e2e` |
| End-to-end (classic) | `cypress/e2e/*.cy.ts` | Cypress | `npm run test:e2e` |

- Behaviour visible to users is described in Gherkin so that non-developers can read it.
- Component tests cover a component in isolation.
- Both run in CI on every PR, see [[05-devops/ci-cd-pipelines|CI/CD Pipelines]].

Details: [[04-testing/component-tests|Component Tests]] · [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]] · [[04-testing/step-definitions-reference|Step Definitions Reference]]

---

%% footer %%

> [!info] Related
> **See also:** [[04-testing/component-tests|Component Tests]] · [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]] · [[04-testing/step-definitions-reference|Step Definitions Reference]]

← [[03-development/how-to-add-a-page|How to Add a Page]] · [[ocid-frontend/index|↑ Documentation home]] · [[04-testing/component-tests|Component Tests]] →
