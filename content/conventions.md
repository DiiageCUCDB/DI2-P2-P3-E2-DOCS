---
title: "How This Knowledge Base Works"
description: "Structure, naming, frontmatter, tags and linking rules for the notes in this vault."
tags:
  - type/reference
  - topic/meta
---

The `content/` folder is both an **Obsidian vault** (open `content/` as the vault) and the source of the published Quartz site.

## Structure

```
content/
├── index.md                  landing page
├── conventions.md            this note
├── requirement/
├── identity-and-access/      the course
│   ├── index.md              course outline
│   ├── 00-introduction/ … 06-passkeys-webauthn/
│   └── reference/            glossary, flow summary, external references
├── ocid-frontend/            front-end documentation
│   ├── index.md              map of content
│   ├── 01-getting-started/ … 05-devops/
└── _templates/               Obsidian templates, not published
```

## Rules

- **Language:** English everywhere. Code identifiers and sample values in traces (for example `dossier.read`) are left as they appear in the project.
- **Names:** folders and files are lowercase kebab-case. Chapters keep a two-digit prefix (`02-pkce`). Every folder that is a chapter has an `index.md`.
- **Title:** set in the frontmatter `title`. Notes have **no `# H1`** in the body, because the site renders the title itself.
- **Description:** one sentence in `description`. It is shown in link previews and search.
- **One idea per note.** A concept (`why-*`), a flow, a trace or a how-to each get their own note. Group them in the chapter `index.md`.

## Tags

Two namespaces only:

| Tag | Values |
|---|---|
| `type/` | `index`, `concept`, `flow`, `trace`, `exercise`, `how-to`, `reference`, `status` |
| `topic/` | the chapter or area (`oauth2`, `pkce`, `oidc`, `federation`, `mfa`, `passkeys`, `webauthn`, `jwt`, `ocid-frontend`, `architecture`, `testing`, `devops`, …) |

## Links

- Always use `[[folder/note|Alias]]` with an alias, so the link reads well and still resolves when the note name is not unique (`index`).
- Link a term to the glossary with `[[reference/glossary#Term|Term]]`.
- Each note ends, after a `%% footer %%` marker, with an optional **Related** callout (key terms, see also) and a **previous · up · next** line. When you add a note, list it in its chapter `index.md` and update the neighbours’ navigation line.

## Templates

`_templates/` holds the Obsidian templates (`note-template`, `feature-template`, `view-template`). The folder is excluded from the published site.
