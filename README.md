# skill-github-daily-ops

Daily GitHub repo health check + safe Dependabot auto-merge. Scans all org repos, reports open PRs/issues/alerts, and auto-merges low/medium severity Dependabot PRs.

## Usage

```bash
# Health report for all org repos
node scripts/daily-ops.js --org Zero2Ai-hub --report

# Auto-merge safe Dependabot PRs
node scripts/daily-ops.js --org Zero2Ai-hub --merge-dependabot

# Both, scoped to specific repos
node scripts/daily-ops.js --org Zero2Ai-hub --repos "repo1,repo2" --report --merge-dependabot
```

## Arguments

| Arg | Default | Description |
|---|---|---|
| `--org` | required | GitHub org name |
| `--report` | false | Output markdown health report |
| `--merge-dependabot` | false | Auto-merge low/medium CVE Dependabot PRs |
| `--repos` | all | Comma-separated repo list to scope |

## Requirements

- Node.js
- `GH_TOKEN` env var or `~/.github_token` with `repo` + `security_events` scopes

## Part of the [Zero2Ai-hub](https://github.com/Zero2Ai-hub) skills ecosystem.
