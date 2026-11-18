---
title: "Code Quality Services"
description: "SonarCloud and CodeRabbit setup."
tags:
  - type/reference
  - topic/ocid-frontend
  - topic/devops
---

| Service | Config | Behaviour |
| ------- | ------ | --------- |
| SonarCloud | `sonar-project.properties` (project key `DiiageCUCDB_DI2-P2P3-E2-OCID`, org `diiagecucdb`) | Scan via `sonar.yml`, needs `SONAR_TOKEN` |
| CodeRabbit | `.coderabbit.yaml` | Automatic review on PRs whose base is `main` or `dev` |
| Lint and format | see [[03-development/code-style-and-linting\|Code Style and Linting]] | Enforced in `test.yml` |

Workflows: [[05-devops/ci-cd-pipelines|CI/CD Pipelines]].

---

%% footer %%

> [!info] Related
> **See also:** [[03-development/code-style-and-linting|Code Style and Linting]] · [[05-devops/ci-cd-pipelines|CI/CD Pipelines]]

← [[05-devops/environment-variables|Environment Variables]] · [[ocid-frontend/index|↑ Documentation home]]
