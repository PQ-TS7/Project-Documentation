# Contributing

## Branching model

`main` always holds reviewed documentation. All changes go through pull requests.

| Branch | Purpose |
|---|---|
| `main` | Reviewed, published documentation. Protected — no direct pushes. |
| `docs/<section>` | Long-lived working branch per section (e.g. `docs/architecture`). Merged to `main` via PR. |
| `docs/<section>-<topic>` | Short-lived branch for one document or change (e.g. `docs/architecture-c4-container`). |
| `fix/<topic>` | Typos, broken links, small corrections. |
| `chore/<topic>` | Repo tooling, templates, CI. |

> Git cannot have both `docs/architecture` and `docs/architecture/<topic>` as branches, so short-lived
> branches use a hyphen: `docs/architecture-c4-container`.

Section branches that exist today:

```text
docs/project-management   docs/requirements    docs/research
docs/architecture         docs/security        docs/components
docs/database             docs/infrastructure  docs/operations
docs/testing              docs/user-guides     docs/deliverables
```

Keep a section branch in sync with `main` before opening a PR:

```bash
git switch docs/architecture
git pull origin main
```

## Commit messages

Use [Conventional Commits](https://www.conventionalcommits.org/) with the section as scope:

```text
docs(architecture): add C2 container diagram
docs(database): document ov_assessments grants
fix(research): correct ML-DSA-65 signature size
chore(repo): add markdownlint config
```

## Pull requests

1. Branch from `main` (or your section branch).
2. Fill in the PR template: what changed, which section, source documents.
3. At least **one reviewer** — preferably the section lead (see [CODEOWNERS](.github/CODEOWNERS)).
4. CI must pass (Markdown lint + relative-link check).
5. Squash-merge, then delete the short-lived branch.

## File conventions

- **Names:** lowercase `kebab-case`, no spaces: `root-ca-key-ceremony.md`, `pq-ca-srs-v0.6.pdf`.
- **Versions:** formal documents carry `vMAJOR.MINOR` in the file name and in their header.
  Replace the old version in the same PR; Git history keeps the previous one.
- **Every folder has a `README.md`** that indexes its contents. Update it when you add a file.
- **Diagrams:** commit the editable source (`.drawio`, `.drawio.svg`, `.puml`, `.mmd`) next to any exported image.
  Prefer Mermaid inside Markdown for simple diagrams.
- **Images:** put them in an `images/` folder beside the document, or in [`/assets`](assets/) if shared.
- **Binary files** (`.pdf`, `.docx`, `.pptx`, `.xlsx`, `.png`, `.jpg`, `.zip`) are tracked by Git LFS
  (see `.gitattributes`). Run `git lfs install` once per machine.

## Document header

Every Markdown document starts with the header from [`templates/document-template.md`](templates/document-template.md):
title, status (`Draft` / `In review` / `Approved` / `Superseded`), version, owner, last updated.

## Architecture decisions

Significant design decisions are recorded as ADRs in [`docs/03-architecture/adr`](docs/03-architecture/adr/)
using [`templates/adr-template.md`](templates/adr-template.md). An accepted ADR is not edited —
supersede it with a new ADR.

## Never commit

- Passwords, API keys, tokens, DB credentials, private keys (`*.key`, `*.p12`, `*.pfx`), SoftHSM token files.
- Real applicant / customer documents or personal data — use redacted or synthetic samples.
- Third-party copyrighted material beyond what citation needs.
