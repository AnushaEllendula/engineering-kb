# Runbooks

Runbooks are step-by-step procedures for operational tasks — especially ones performed
under time pressure, like incident response. A good runbook assumes the reader is
stressed and in a hurry: be explicit, avoid unnecessary context, and put the commands to
run front and center.

## Index

> Add a row per runbook as they're written.

| Runbook | When to use it |
|---|---|
| _example: Restart the ingestion service_ | _example: ingestion lag alert fires_ |

## Writing a new runbook

Copy [doc-templates/runbook-template.md](../doc-templates/runbook-template.md), fill it in, and
open a pull request. Add it to the table above and to `nav:` in `mkdocs.yml`.

## Keeping runbooks trustworthy

A runbook that's wrong is worse than no runbook — it costs time during an incident and
erodes trust in the whole KB. Whoever follows a runbook during a real incident should
fix it immediately afterward if any step was inaccurate or missing.
