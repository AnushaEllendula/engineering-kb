# ADR-0001: Adopt a Git-based knowledge base

- **Status:** Accepted
- **Date:** 2026-08-10
- **Deciders:** _fill in_

## Context

The organization needs a central place for engineering documentation — architecture
decisions, runbooks, coding standards, and onboarding material — that stays accurate,
is easy to contribute to, and doesn't rot silently the way ad-hoc wiki pages tend to.

## Decision

Documentation is stored as Markdown in a Git repository (`<your-repo-name>`), rendered
into a static, searchable site using MkDocs with the Material theme, and published via
GitHub Pages. Changes go through the same pull-request review process as code.

## Alternatives considered

- **Provider wiki (GitHub/GitLab/Azure DevOps built-in wiki):** simplest to start, but
  weaker review workflow, no local preview, and typically a separate repo/history from
  the code it documents.
- **Third-party wiki tool (Confluence, Notion, etc.):** rich editing and permissions, but
  lives outside version control, harder to enforce review, and adds a licensing
  dependency.

## Consequences

- Documentation changes are reviewable, diffable, and attributable via `git blame`.
- Contributors need basic Git familiarity — mitigated by the
  [Getting Started](../getting-started/index.md) guide and GitHub's web-based Markdown
  editor for small edits.
- The site requires a build step (MkDocs); this is automated via GitHub Actions on
  merge to `main` (see `.github/workflows/deploy.yml`).
