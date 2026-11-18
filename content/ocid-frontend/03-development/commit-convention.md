---
title: "Commit Convention"
description: "Conventional Commits format read by semantic-release."
aliases: [Conventional Commits]
tags:
  - type/concept
  - topic/ocid-frontend
  - topic/development
  - topic/git
---

Commits follow [Conventional Commits](https://www.conventionalcommits.org/). They are read by semantic-release ([[05-devops/release-process|Release Process]]).

```
<type>: <short description>

[optional body]

[optional footer, e.g. BREAKING CHANGE: ...]
```

| Type | Release effect | Example |
| ---- | -------------- | ------- |
| `fix:` | patch (1.0.0 to 1.0.1) | `fix: added cypress config` |
| `feat:` | minor (1.0.0 to 1.1.0) | `feat: gherkin init` |
| `BREAKING CHANGE:` in footer | major | |
| `chore:`, `docs:`, `ci:`, `refactor:` | none, no Docker image built | `refactor: view folder` |

> [!warning] Documentation-only pushes
> `docker.yml` ignores pushes that only touch `*.md` files, so docs changes never trigger a release.

The release bot commits with `chore(release): x.y.z [skip ci]`.

---

%% footer %%

> [!info] Related
> **See also:** [[05-devops/ci-cd-pipelines|CI/CD Pipelines]] · [[05-devops/release-process|Release Process]] · [[03-development/git-workflow|Git Workflow]]

← [[03-development/git-workflow|Git Workflow]] · [[ocid-frontend/index|↑ Documentation home]] · [[03-development/how-to-add-a-page|How to Add a Page]] →
