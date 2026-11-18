---
title: "E2E Gherkin Tests"
description: "Gherkin scenarios run end to end with Cypress."
tags:
  - type/concept
  - topic/ocid-frontend
  - topic/testing
  - topic/cypress
  - topic/gherkin
---

Scenarios are `.feature` files run by Cypress through `@badeball/cypress-cucumber-preprocessor`, bundled with esbuild.

## Layout

```
cypress/
├── e2e/*.feature                    scenarios (Given / When / Then)
└── support/step_definitions/*.ts    step implementations, shared by all features
```

## Configuration

| Setting | Value | File |
| ------- | ----- | ---- |
| Spec pattern | `cypress/e2e/**/*.feature` and `cypress/e2e/**/*.{cy,spec}.*` | `cypress.config.ts` |
| Base URL | `http://localhost:4173` (the `preview` server) | `cypress.config.ts` |
| Step definitions | `cypress/support/step_definitions/**/*.{js,ts}` | `.cypress-cucumber-preprocessorrc.json` |
| Reports | `cypress/reports/cucumber-report.html` and `.json` | `.cypress-cucumber-preprocessorrc.json` |

## Running

```sh
npm run test:e2e        # builds/serves preview, runs all features headless
npm run test:e2e:dev    # interactive runner on the dev server
npx cypress run --e2e --env tags=@smoke   # only tagged scenarios
```

## Current feature

```gherkin
@smoke
Feature: Home page
  As a visitor
  I want to open the application
  So that I know it is up and running

  Scenario: Visiting the app root url
    Given I visit "/"
    Then I should see the heading "You did it!"
```

## Writing a new feature

1. Copy `_templates/feature-template.md` to `cypress/e2e/<name>.feature`.
2. Reuse existing steps ([[04-testing/step-definitions-reference|Step Definitions Reference]]).
3. If a step is specific to this feature, add `cypress/support/step_definitions/<name>.steps.ts`.
4. Tag scenarios (`@smoke`, ...) to run subsets.

> [!tip] Selectors
> The "type in field" step matches `[name="..."]` or `[data-testid="..."]`. Add a `data-testid` to inputs in views.

---

%% footer %%

> [!info] Related
> **See also:** [[04-testing/testing-strategy|Testing Strategy]] · [[04-testing/component-tests|Component Tests]] · [[04-testing/step-definitions-reference|Step Definitions Reference]]

← [[04-testing/component-tests|Component Tests]] · [[ocid-frontend/index|↑ Documentation home]] · [[04-testing/step-definitions-reference|Step Definitions Reference]] →
