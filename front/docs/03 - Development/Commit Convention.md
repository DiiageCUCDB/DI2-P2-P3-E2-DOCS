---
title: Commit Convention
aliases: [Conventional Commits]
tags: [ocid, development, git, release]
---

# Commit Convention

Commits follow [Conventional Commits](https://www.conventionalcommits.org/). They are read by semantic-release ([[Release Process]]).

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
