# GitHub Workflows

- `claude.yml` – Responds to `@claude` mentions on issues, PRs, and review comments using `anthropics/claude-code-action`, limited to repo members/collaborators.
- `claude-code-review.yml` – Runs automated Claude code reviews on PR open/sync for trusted authors with a project-specific checklist prompt.
- `claude-issue-triage.yml` – Triage new issues with Claude, adding labels and comments based on the provided triage prompt.
- `dev-release.yml` – On pushes to `main` (or manual trigger), builds the package with `uv` and publishes a PyPI dev release when the version string includes `dev`.
- `docker.yml` – Builds and pushes a multi-arch Docker image to your GHCR namespace (based on the repo owner) on version tags or manual dispatch using Docker metadata for tags/labels.
- `pr-title.yml` – Enforces semantic PR titles on open/edit/sync via `amannn/action-semantic-pull-request`.
- `release.yml` – On version tags, builds distributions, creates a GitHub release with artifacts, publishes to PyPI, then bumps the Homebrew tap for non-pre-release tags.
- `test.yml` – Runs lint, type checks, and SQLite/Postgres test matrices on pushes/PRs to `main` (including `pull_request_target`) across Python 3.12/3.13 on Ubuntu and Windows.
