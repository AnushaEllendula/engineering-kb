# Engineering Knowledge Base

Central, version-controlled engineering documentation for **Dark Horse Digital Solutions
Pvt Ltd** — architecture decisions, runbooks, coding standards, and onboarding material.

Built with [MkDocs](https://www.mkdocs.org/) and the
[Material theme](https://squidfunk.github.io/mkdocs-material/), published via GitHub
Pages.

**Live site:** `https://<AnushaEllendula>.github.io/engineering-kb/` (update after
enabling GitHub Pages — see below)

## Repo structure

```
docs/
  index.md                 Landing page
  getting-started/         Environment setup
  onboarding/              New joiner checklist
  architecture/            System overview + ADRs
  coding-standards/        Language/review standards
  runbooks/                Operational procedures
  doc-templates/            Templates for new runbooks/ADRs/how-tos
  assets/                   Images and diagrams
mkdocs.yml                 Site config and navigation
requirements.txt           Python deps to build the site
.github/workflows/         CI: build + deploy to GitHub Pages
```

## Local development

```bash
python -m venv .venv && source .venv/bin/activate   # optional but recommended
pip install -r requirements.txt
mkdocs serve
```

Open `http://127.0.0.1:8000`. Pages rebuild live as you edit.

## Deploying

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site and
publishes it to GitHub Pages automatically. No manual `mkdocs gh-deploy` needed.

**One-time setup after creating the repo on GitHub:**

1. Push this scaffold to a new GitHub repository.
2. In the repo, go to **Settings → Pages** and set the source to **GitHub Actions**.
3. Replace every `<AnushaEllendula>` and `engineering-kb` placeholder in this repo
   (`mkdocs.yml`, `README.md`, docs pages) with your actual org/repo name.
4. Push to `main` — the site will build and publish automatically.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License / access

Internal documentation for Dark Horse Digital Solutions Pvt Ltd. Set repository
visibility (private/internal) according to your organization's policy before adding
sensitive content.
