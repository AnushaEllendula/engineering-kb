# Architecture Decision Records (ADRs)

An ADR captures a significant architectural decision: the context that prompted it, the
options considered, the decision made, and its consequences. ADRs are immutable once
accepted — if a decision is later reversed, write a new ADR that supersedes the old one
rather than editing it.

## Index

| ID | Title | Status |
|---|---|---|
| [0001](0001-adopt-git-based-kb.md) | Adopt a Git-based knowledge base | Accepted |

## Writing a new ADR

1. Copy [doc-templates/adr-template.md](../doc-templates/adr-template.md) to
   `docs/adr/00XX-short-title.md` (next sequential number)
2. Fill it in and open a pull request
3. Add a row to the index table above
4. Add the new file to `nav:` in `mkdocs.yml` under **Architecture → Architecture
   Decision Records**
