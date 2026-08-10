# Getting Started

This section covers what a new contributor needs to start working with the codebase and
this knowledge base itself.

## Prerequisites

- Git, and a GitHub account with access to the organization
- Python 3.10+ (only needed if you're building this documentation site locally)
- Your team's standard toolchain — see your team's own repository README for
  language/runtime specifics

## Working with this knowledge base locally

```bash
git clone https://github.com/<your-github-org>/<your-repo-name>.git
cd <your-repo-name>
pip install -r requirements.txt
mkdocs serve
```

Then open `http://127.0.0.1:8000` to preview the site as you edit. Pages rebuild live as
you save files.

## Proposing a change

1. Create a branch: `git checkout -b docs/short-description`
2. Edit or add Markdown files under `docs/`
3. Preview locally with `mkdocs serve`
4. Open a pull request — see [CONTRIBUTING.md](https://github.com/<your-github-org>/<your-repo-name>/blob/main/CONTRIBUTING.md)

See also: [Local dev setup](local-setup.md) for project-specific environment setup.
