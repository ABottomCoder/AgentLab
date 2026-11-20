# Reference notes

Optional. Read this when you are stuck or want a starting point. Nothing here is required, and any of it
can be replaced by a better idea of yours. Official documentation is linked by name rather than URL; ask
Claude to find the current page.

## Any project

- Python, SQLite and pytest are a simple start. Any language is fine if your README and CI cover it.
- A decision record (`docs/decisions/000-template.md`) is worth writing whenever you pick between options.
- Keep secrets in `.env` (git-ignored); in CI and on a host, use their secret settings.
- If a key ever reaches git history, revoke and replace it first; cleaning history comes second.
- Tests that need no keys or network: record a few real responses once and replay them as fixtures.

## Evaluation terms worth looking up

Precision and recall, a confusion matrix, inter-annotator (and self-) agreement, a train/holdout split
and why you only look at the holdout once, and run-to-run agreement for non-deterministic models.

## Recruiter Watch

- X API v2: user timeline endpoints, the `since_id` parameter, and the pay-per-use pricing and usage pages
  in the developer console.
- Discord: a bot can post through the REST API without keeping a connection open.
- Scheduling options: your OS's task scheduler or cron, GitHub Actions on a schedule, a small cloud server.

## HN Hiring Digest

- Two official HN APIs: the Firebase API and the Algolia search API.
- Claude API: the Messages API, structured outputs or a JSON schema, and prompt caching. Set a spend limit
  in the console before the first call.

## Workflow Kit

- Claude Code docs: memory (`CLAUDE.md`), custom slash commands, skills, hooks, subagents.
- git hooks (`pre-commit`) and secret scanners such as gitleaks.

## JobRadar

- Kinds of sources to consider: companies' own careers systems (many expose public job feeds),
  job aggregators with developer APIs, community threads, government data, and your own inbox.
- Gmail API with OAuth and a read-only scope, for job-alert emails.
- For the agent: the Claude API tool-use documentation (how `tool_use` and `tool_result` blocks pair up).
- Hosting: static or serverless hosts, small app hosts, and hosted Postgres with a free tier. Keeping
  personal data private can be simple: a host's built-in password protection, one login for you, or a
  public page that shows aggregates only.
- Public data that can feed insights: state WARN layoff notices, and the US Department of Labor's H-1B
  disclosure data.
