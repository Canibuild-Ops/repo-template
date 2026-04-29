# {{ repo-name }}

> Replace this README with your project-specific content. The Canibuild-Ops governance baseline (notify-on-push, secret-scan, review-notify, CODEOWNERS) is already wired in via this template.

## Created via Canibuild-Ops governance

This repo was scaffolded from `Canibuild-Ops/repo-template` via the `/create-repo` skill. That means it ships with:

- `.github/workflows/notify.yml` — every push to `main` posts a Claude-generated summary to `#ai-os-changes` in Slack (visibility, not gates)
- `.github/workflows/secret-scan.yml` — gitleaks scan blocks any push that contains a credential
- `.github/workflows/review-notify.yml` — pings Mark in Slack when a PR requests his review (only fires on protected repos)
- `.github/CODEOWNERS` — defaults to `@mdeacon-cib` so any future branch-protection rule has owners to enforce against

## Secrets

All production secrets live in Azure Key Vault `kv-canibuild-ops`. **Never commit secrets to this repo.** See https://github.com/Canibuild-Ops/.github/blob/main/SECURITY.md for the full policy and naming convention.

## Working in this repo

Org-wide doctrine (push skills, repo-naming, secret handling) lives in `Canibuild-Ops/claude-config/CLAUDE-canibuild.md` and is loaded into every Claude Code session via `~/.claude/CLAUDE.md`. Read that for the rules.
