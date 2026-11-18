---
title: "Installation and First Run"
description: "Clone, install and run the app locally for the first time."
tags:
  - type/how-to
  - topic/ocid-frontend
  - topic/getting-started
---

```sh
git clone https://github.com/DiiageCUCDB/DI2-P2P3-E2-OCID.git
cd DI2-P2P3-E2-OCID
npm install
npm run dev
```

The dev server runs on **http://localhost:5173** with hot reload.

> [!note] Cypress download
> `npm install` triggers the `prepare` script (`cypress install`), which downloads the Cypress binary (about 200 MB). The CI caches it, see [[05-devops/ci-cd-pipelines|CI/CD Pipelines]].

## Verify the setup

1. Open http://localhost:5173: the page shows the heading "You did it!" (current placeholder, see [[ocid-frontend/open-points|Open Points]]).
2. Run `npm run lint` and `npm run type-check`: both should pass.
3. Run `npm run test:e2e`: the `@smoke` home scenario should pass, see [[04-testing/e2e-gherkin-tests|E2E Gherkin Tests]].

## Running in a container instead

See [[05-devops/docker|Docker]] for the dev-profile compose file.

Previous: [[01-getting-started/prerequisites|Prerequisites]] · Next: [[01-getting-started/npm-scripts|npm Scripts]]

---

%% footer %%

> [!info] Related
> **See also:** [[01-getting-started/prerequisites|Prerequisites]] · [[01-getting-started/npm-scripts|npm Scripts]]

← [[01-getting-started/prerequisites|Prerequisites]] · [[ocid-frontend/index|↑ Documentation home]] · [[01-getting-started/npm-scripts|npm Scripts]] →
