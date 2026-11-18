---
title: "Step Definitions Reference"
description: "Shared Gherkin steps and their implementations."
tags:
  - type/reference
  - topic/ocid-frontend
  - topic/testing
  - topic/cypress
  - topic/gherkin
---

Shared steps in `cypress/support/step_definitions/common.steps.ts`.

| Keyword | Step | Implementation |
| ------- | ---- | -------------- |
| Given | `I visit "{path}"` | `cy.visit(path)` |
| When | `I click on "{text}"` | `cy.contains(text).click()` |
| When | `I type "{value}" in the "{field}" field` | types into `[name="field"]` or `[data-testid="field"]` |
| Then | `I should see the heading "{text}"` | `cy.contains('h1', text)` is visible |
| Then | `I should see "{text}"` | `cy.contains(text)` is visible |
| Then | `I should be on "{path}"` | `cy.location('pathname')` equals path |

Add new shared steps to `common.steps.ts`, feature-specific ones to their own `*.steps.ts`. See [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]].

---

%% footer %%

> [!info] Related
> **See also:** [[04-testing/testing-strategy|Testing Strategy]] · [[04-testing/component-tests|Component Tests]] · [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]]

← [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]] · [[ocid-frontend/index|↑ Documentation home]] · [[05-devops/docker|Docker]] →
