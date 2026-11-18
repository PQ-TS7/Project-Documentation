# PQ-CA — Project Documentation

Documentation repository for **PQ-CA**, a post-quantum TLS Certificate Authority built as microservices
(ML-DSA signing via OpenSSL 3.x + oqs-provider, a separate RA, an AI-assisted Organization Validation agent,
and two local-LLM assistants). Graduation project — Gigabyte Bridge program.

> This repo holds **documentation only**. Source code lives in the main project repository.

## Repository layout

| Folder | What goes there | Lead |
|---|---|---|
| [`docs/00-project-management`](docs/00-project-management/) | Proposal, roles & task assignment, schedule, meeting notes, progress / Q&A reports | Saif Wael |
| [`docs/01-requirements`](docs/01-requirements/) | SRS, functional / non-functional requirements, traceability | Team |
| [`docs/02-research`](docs/02-research/) | PQC algorithm studies, comparative analyses, libraries & frameworks | Marawan Ahmed |
| [`docs/03-architecture`](docs/03-architecture/) | C4 diagrams, PKI hierarchy, data flows, **ADRs** | Team |
| [`docs/04-security`](docs/04-security/) | Threat model, key management, Root CA ceremony, hardening | Marawan Ahmed / Saif Wael |
| [`docs/05-components`](docs/05-components/) | One folder per microservice (design, API, config) | Component owner |
| [`docs/06-database`](docs/06-database/) | Schema, ER diagrams, roles & grants, audit chain | Andrew Rami |
| [`docs/07-infrastructure`](docs/07-infrastructure/) | Kubernetes, containers, CI/CD, network, SoftHSM2 | Andrew Rami / Saif Wael |
| [`docs/08-operations`](docs/08-operations/) | Runbooks, incident procedures, monitoring | Team |
| [`docs/09-testing`](docs/09-testing/) | Test strategy, test plans, AI evaluation, load-test results | Mariam Hazem Gamgoum |
| [`docs/10-user-guides`](docs/10-user-guides/) | Admin portal, customer portal, RA officer guides | Seif Aly |
| [`docs/11-deliverables`](docs/11-deliverables/) | Submitted reports, presentations, posters (final versions only) | Saif Wael |
| [`templates`](templates/) | Templates for documents, ADRs, meeting notes, runbooks, components | — |
| [`assets`](assets/) | Shared images and logos used across documents | — |

See also: [Glossary](docs/glossary.md) · [Contributing](CONTRIBUTING.md) · [Changelog](CHANGELOG.md)

## Quick rules

1. **`main` is protected.** Work on a branch, open a pull request, get one review.
2. **Markdown first.** Write living documents in Markdown. Binary files (PDF/DOCX/PPTX) are for
   external papers and submitted deliverables; they are stored with **Git LFS**.
3. **Name files** in `kebab-case`, with a version for formal documents: `pq-ca-srs-v0.6.pdf`.
4. **Never commit secrets** — no passwords, private keys, tokens or real customer data, even in examples.

## Getting started

```bash
git lfs install
git clone https://github.com/PQ-TS7/Project-Documentation.git
```
