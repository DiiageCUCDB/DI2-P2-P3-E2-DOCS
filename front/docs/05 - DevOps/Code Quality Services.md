---
title: Code Quality Services
tags: [ocid, devops, quality]
---

# Code Quality Services

| Service | Config | Behaviour |
| ------- | ------ | --------- |
| SonarCloud | `sonar-project.properties` (project key `DiiageCUCDB_DI2-P2P3-E2-OCID`, org `diiagecucdb`) | Scan via `sonar.yml`, needs `SONAR_TOKEN` |
| CodeRabbit | `.coderabbit.yaml` | Automatic review on PRs whose base is `main` or `dev` |
| Lint and format | see [[Code Style and Linting]] | Enforced in `test.yml` |

Workflows: [[CI-CD Pipelines]].
