# Reference notes

Optional. Read this when you are stuck or want a starting point. Nothing here is required, and any of it
can be replaced by a better idea of yours. Official documentation is linked by name rather than URL; ask
Claude to find the current page.

## Any project

- Python, SQLite and pytest are a simple start. Any language is fine if your README and CI cover it.
- A decision record (`docs/decisions/000-template.md`) is worth writing whenever you pick between options.
- Keep secrets in `.env` (git-ignored); in CI and on a host, use their secret settings.

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
- Hosting: static or serverless hosts, small app hosts, and hosted Postgres with a free tier.
- Public data that can feed insights: state WARN layoff notices, and the US Department of Labor's H-1B
  disclosure data.
