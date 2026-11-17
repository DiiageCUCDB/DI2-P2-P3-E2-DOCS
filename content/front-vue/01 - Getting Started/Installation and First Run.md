---
title: Installation and First Run
tags: [ocid, getting-started]
---

# Installation and First Run

```sh
git clone https://github.com/DiiageCUCDB/DI2-P2P3-E2-OCID.git
cd DI2-P2P3-E2-OCID
npm install
npm run dev
```

The dev server runs on **http://localhost:5173** with hot reload.

> [!note] Cypress download
> `npm install` triggers the `prepare` script (`cypress install`), which downloads the Cypress binary (about 200 MB). The CI caches it, see [[CI-CD Pipelines]].

## Verify the setup

1. Open http://localhost:5173: the page shows the heading "You did it!" (current placeholder, see [[Open Points]]).
2. Run `npm run lint` and `npm run type-check`: both should pass.
3. Run `npm run test:e2e`: the `@smoke` home scenario should pass, see [[E2E Gherkin Tests]].

## Running in a container instead

See [[Docker]] for the dev-profile compose file.

Previous: [[Prerequisites]] · Next: [[npm Scripts]]
