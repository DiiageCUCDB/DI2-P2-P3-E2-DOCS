---
title: Release Process
tags: [ocid, devops, release]
---

# Release Process

Fully automated with **semantic-release** (config: `.releaserc`, branch `main` only).

## Pipeline of plugins

1. `commit-analyzer`: decides the bump from [[Commit Convention]].
2. `release-notes-generator`
3. `changelog`: writes `CHANGELOG.md`
4. `npm` with `npmPublish: false`: updates the version in `package.json`
5. `git`: commits `CHANGELOG.md`, `package.json`, `package-lock.json` as `chore(release): ${version} [skip ci]`
6. `github`: creates the GitHub release and tag

## Outcome

- Release published: Docker image pushed, see [[CI-CD Pipelines]].
- Only `chore:`/`docs:`/`ci:` commits: nothing happens.

History so far: `1.0.0-init.1` then `1.0.0` (2026-11-17).

> [!warning]
> Never edit `CHANGELOG.md` or the `version` field manually.
