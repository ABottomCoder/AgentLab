# AgentLab

Learn to work with AI agents by building tools you will actually use while job hunting.

Four projects, from small to large:

| Project | What you end up with |
|---|---|
| Recruiter Watch | job posts from recruiters on X, pushed to your phone |
| HN Hiring Digest | the monthly "Who is hiring?" thread, turned into structured data |
| Workflow Kit | your own Claude Code setup: lessons, hooks, skills, subagents |
| JobRadar | your job-search tool: many sources, daily picks, application tracking, a deployed dashboard, insights |

Along the way you go from *using* an agent, to *making it reliable*, to *building one yourself*.
JobRadar, finished, is a project you can talk about for 30 minutes in an interview.

## Set up your own copy

This starter repo is public; your work lives in a repo of your own.

1. Clone the starter repo.
2. On GitHub, create an **empty** repo under your account (no README, no license). Public is simplest:
   nothing personal is committed by design, and it doubles as a portfolio.
3. Point your clone at it and push:
   ```bash
   git remote rename origin starter
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
4. Send your repo URL to the people checking your work. If you keep it private, add them as
   collaborators so they can pull it. They only pull and run your code; they never push to your repo.

Updates to the task list may land in the starter repo later. To bring them in, commit your work first,
then `git pull starter main` on your `main` branch. If a file you also edited conflicts (`HANDOFF.md`,
`PROGRESS.md`), keep your version.

## What never goes in the repo

Your resume, your application records, labels with personal notes, and screenshots that show your
inbox or other personal details. Keep them in `data/private/` (git-ignored). Your repo can then be
public without exposing you.

## Getting started

1. Open this folder with Claude Code. It reads `CLAUDE.md`, whose "coach mode" makes it a coach rather
   than someone who does the work for you.
2. Read [TASKS.md](TASKS.md) and start with S1.
3. Before each session, glance at [HANDOFF.md](HANDOFF.md) to see where you left off.

## How to work here

1. One branch per task, named after it (`rw2-incremental-fetch`).
2. Open a PR into `main` and fill in the template.
3. CI must be green (tests and the secret scan).
4. Merge it yourself. Update [PROGRESS.md](PROGRESS.md) in the same PR.
5. When Claude makes a mistake worth remembering, add it to [lessons.md](lessons.md).
6. When you choose between options, write a decision record in `docs/decisions/` (template
   `000-template.md`).

## Why this is not easy even with Claude Code

On purpose. Claude Code can write a lot of the code, but every task has a part it cannot do for you:

- **What only you know**: which roles and companies you want, which jobs are worth applying to, your
  resume.
- **What only you can do**: sign up for accounts, get keys, create bots, deploy.
- **What you must judge**: some requirements are left open on purpose. You set the standard and write
  down why.
- **What you must prove**: acceptance is command output and evaluation numbers, not Claude saying "done".
- **What you do live**: at each gate you explain your work and make a small change without Claude.

[hand-written] and [by hand] steps run on trust. They are where most of the learning happens, and the
gates are where you get to show it.

## What it costs

Rough estimates, not measured; check each provider's current pricing and set a spending cap before the
first call.

- Claude Code: your existing subscription.
- X API: charged per post returned; roughly a few dollars up to about $20 a month, depending on how many
  accounts you watch and how often they post (RW1 makes you work out the real number).
- Claude API (from HN2 on): a few dollars a month at this scale, more if you rerun evaluations often.
- Discord, the HN API, the Gmail API: free.
- Hosting the dashboard (JR12): free tiers are usually enough.

## Checks

- About every two weeks we pull your repo, run your tests (they need no keys), and read the commits,
  PRs, `PROGRESS.md`, evidence and evaluation results. We do not change anything in it; feedback comes
  to you directly.
- Each layer ends with a live gate (C1–C3 in TASKS.md). Tell us when you reach one; the live parts run
  on your machine, with your keys.
- There is no deadline. If something is unclear or you are stuck for days, ask: that is what the checks
  are for.
- The task list may change as you go. Changes land in this starter repo; `git pull starter main`
  brings them in.

## Map

| Path | What it is for |
|---|---|
| `TASKS.md` | every task and how it is checked |
| `PROGRESS.md` | your log, one entry per task |
| `HANDOFF.md` | where you are and what is next, mainly for a fresh Claude session |
| `lessons.md` | mistakes (Claude's and yours) and how to prevent them |
| `CLAUDE.md` | rules for Claude Code, including coach mode |
| `projects/` | the four projects |
| `docs/decisions/` | decision records |
| `docs/evidence/` | screenshots and command output |
| `docs/reference/` | optional notes and starting points, never requirements |
| `.env.example` | which keys you need (real ones go in `.env`, never committed) |
