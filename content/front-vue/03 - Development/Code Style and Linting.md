---
title: Code Style and Linting
tags: [ocid, development, lint]
---

# Code Style and Linting

## Formatting

| Tool | Rules |
| ---- | ----- |
| Prettier | no semicolons, single quotes, print width 100 (`.prettierrc.json`) |
| EditorConfig | UTF-8, 2 spaces, LF, final newline, trim trailing whitespace, max line 100 |

Run `npm run format` (Prettier on `src/`).

## Linting

Two linters run in sequence via `npm run lint`:

1. **oxlint** (`.oxlintrc.json`): plugins `eslint`, `typescript`, `unicorn`, `oxc`, `vue`; category `correctness` set to `error`.
2. **ESLint** (`eslint.config.ts`): `eslint-plugin-vue` essential rules, `@vue/eslint-config-typescript` recommended, `eslint-plugin-oxlint` to turn off rules already covered by oxlint, and `eslint-config-prettier` so formatting is left to Prettier.

Ignored: `dist/`, `dist-ssr/`, `coverage/`.

> [!tip]
> Install the editor extensions listed in [[Prerequisites]] to get these on save.

The CI runs lint on every PR, see [[CI-CD Pipelines]].
