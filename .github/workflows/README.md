# GitHub Workflows (Fork)

This is a fork of [basicmachines-co/basic-memory](https://github.com/basicmachines-co/basic-memory) specifically for building Docker containers with custom UID/GID settings (99/100) for unRAID compatibility.

## Active Workflows

- **`docker.yml`** – Builds and pushes a multi-arch Docker image to GHCR on:
  - Pushes to `main` branch
  - Version tags (`v*`)
  - Manual workflow dispatch
  
  The image is built with `UID=99` and `GID=100` for unRAID's `nobody` user compatibility.

- **`test.yml`** – Runs lint, type checks, and SQLite/Postgres test matrices on pushes/PRs to `main`.

## Removed Workflows (from upstream)

The following upstream workflows have been removed as they're not needed for this fork:

- `dev-release.yml` – PyPI dev releases
- `release.yml` – PyPI/Homebrew publishing
- `claude*.yml` – Claude AI integrations
- `pr-title.yml` – Semantic PR title enforcement

## Docker Image Usage

```bash
docker pull ghcr.io/ryangates/basic-memory:latest
```

The image runs as UID 99 / GID 100 which matches unRAID's `nobody` user.
