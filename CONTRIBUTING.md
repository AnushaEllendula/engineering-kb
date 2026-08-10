# Contributing to the Knowledge Base

This knowledge base is maintained the same way we maintain code: propose changes via
pull request, get a review, merge.

## Making a change

1. **Clone and branch**

   ```bash
   git clone https://github.com/AnushaEllendula/engineering-kb.git
   cd engineering-kb
   git checkout -b docs/short-description
   ```

2. **Install and preview locally**

   ```bash
   pip install -r requirements.txt
   mkdocs serve
   ```

   Open `http://127.0.0.1:8000` and confirm your change renders and navigates correctly.

3. **Follow the existing structure**

   - New runbook → copy `docs/doc-templates/runbook-template.md`
   - New architecture decision → copy `docs/doc-templates/adr-template.md`, number it
     sequentially, and add it to `docs/adr/index.md`
   - New task-oriented guide → copy `docs/doc-templates/how-to-template.md`
   - New page → add it to the `nav:` section of `mkdocs.yml`, or it won't appear in the
     site navigation (it will still build, just be unreachable via menus)

4. **Open a pull request**

   Small, focused PRs are easier to review. Explain *why* the change is needed, not just
   what changed — that context is often more valuable than the edit itself.

5. **Review**

   At least one approval is required to merge (configure this as a branch protection
   rule on `main`). Reviewers should check accuracy, not just formatting — a
   confidently-wrong runbook is worse than no runbook.

## Writing guidelines

- Prefer plain language over jargon; assume the reader is new.
- Keep pages focused — split a page if it's trying to cover two topics.
- Use relative links between pages (e.g. `[link](../architecture/index.md)`) so links
  keep working locally, in PR previews, and on the published site.
- Store images under `docs/assets/` and reference them with relative paths.
- Runbook and ADR content should be reviewed for accuracy periodically — stale
  operational docs are actively dangerous during an incident.

## Reporting a problem without fixing it yourself

Open an issue using the "Documentation issue" template if you spot something wrong but
don't have time to fix it — that's still a valuable contribution.
