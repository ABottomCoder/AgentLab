# Tasks

Four projects. Each task says **what** to achieve and **how we will know it is done**. How you build it is
up to you. If you want a starting point, [docs/reference/](docs/reference/README.md) has optional notes.

- Work in ID order, with two exceptions: Workflow Kit (WK) tasks run alongside the others, and JR2
  (collecting) and JR4 (tracking applications) may start any time. Start them early: insights need
  weeks of history, and until JR4 exists, keep your applications in a spreadsheet.
- A task is done when its PR is merged, `PROGRESS.md` has an entry, and the evidence is in
  `docs/evidence/`.
- Every project has tests that run without keys or network, so we can run them on our side.
- Gates (C1–C3) are live sessions with us; tell us when you reach one. You can keep going before a gate;
  fix what it finds.
- **[by hand]**: no Claude for this step. **[hand-written]**: you write this code; Claude may only
  explain and review.
- Rough size: ★ an evening, ★★ a few evenings, ★★★ about a week, ★★★★ more than a week. The whole list
  is about 3–4 months part-time (an estimate), plus waiting time for data to build up.
- Three layers: Recruiter Watch is about *using* an agent (gate C1); HN, Workflow Kit and JR1–JR6 are
  about *making it reliable* (gate C2); JR7 onward is about *building one* (gate C3).

---

## 0. Setup

**S1 Make the repo yours** ★
Anyone can clone it and run your projects from the README. Your tests run automatically on every PR.
One project with one passing test is enough to start. Subscribe to job alerts on the job boards you
use, today, delivered to an inbox your tools will be able to read later: that history starts the day
you subscribe.
*Done when*: we follow your README on our machine without getting stuck, CI runs your tests, and your
alerts are arriving.

---

## 1. Recruiter Watch

Recruiters and hiring managers post openings on X, often before job boards do. Watch the people who
matter to you and get their real job posts on your phone every day, without paying twice for the same
post.

**RW1 Who to watch** ★★
*Done when*: a list of at least 15 accounts with a reason for each, a monthly cost estimate built from
real numbers, and a spending cap set.

**RW2 Only what is new** ★★
*Done when*: a second run right after the first costs nothing.

**RW3 Job post or not** ★★★
*Done when*: you can state how accurate your filter is, measured on at least 50 posts you labeled
[by hand].

**RW4 To your phone** ★★
*Done when*: job posts arrive in your Discord, the first run behaves sensibly (you define sensibly), and
no secret is in the git history.

**RW5 Every day, on its own** ★★★
*Done when*: three consecutive days of real unattended runs, and a failure reaches you.

**C1 Gate**: explain how one post travels to your phone; make a small change live without Claude.

---

## 2. HN Hiring Digest

Every month, Hacker News runs "Ask HN: Who is hiring?" with a few hundred free-text posts. Turn them
into data you can filter, and into a digest you would actually read.

**HN1 The thread** ★
*Done when*: you have every post of the latest thread, as clean text.

**HN2 Structure with an LLM** ★★★
*Done when*: each post becomes the fields you chose, with accuracy per field measured against answers
you wrote [by hand] for 20 posts, a known cost per month, and a measured run-to-run agreement.

**HN3 The digest** ★★
*Done when*: the digest reaches your phone, and you have a list of the companies it surfaced (JobRadar
will use it).

---

## 3. Workflow Kit

Make your work with Claude Code reliable and fast. Each task changes how you work, not what the code does.

**WK1 Lessons that change behaviour** ★★ (ongoing from S1)
*Done when* (by gate C2): at least 8 lessons from real incidents, at least 3 turned into rules, one rule
shown to have prevented a repeat, and one of your own rules removed because it was useless (coach mode
stays).

**WK2 Automate the repetitive** ★★
*Done when*: at least three things automated, one of which stops secrets before they are committed, with
the time saved measured.

**WK3 Subagents: worth it?** ★★★
*Done when*: one wide task done with and without subagents, compared with numbers, and your rule for when
to use them.

**WK4 Handoff** ★★
*Done when*: a fresh session (after `/clear`) continues a half-done task from the repo files alone; you
did this twice, improving your handoff in between, and compared how well each went.

**WK5 Independent review** ★★★
*Done when*: a fresh Claude session that never saw the work reviewed one of your PRs, every comment is
triaged with a reason, at least one is rejected, and you found at least one problem it missed.

---

## 4. JobRadar

Your job-search tool. It collects jobs from many sources, removes duplicates, picks what you should
apply to each day, tracks your applications, lives on a deployed dashboard, and finds signals a job list
does not show. Start collecting early: some insights need weeks of history.

**JR1 Sources** ★★★
You already have two floor sources: X (Recruiter Watch) and your job-alert emails. Find the rest.
*Done when*: a decision record that compares at least 6 candidate sources using numbers you measured
yourself, and picks 2–3 to add.
*Rules*: read and quote each source's terms. Never bypass a CAPTCHA or bot check. Browser automation on
your own accounts is your call: if you use it, the record covers the risk, and the system still works
without it.

**JR2 Collect** ★★★
*Done when*: every chosen source and your alert emails land in one store every day, and one broken source
does not stop the others.

**JR3 Same job, many sources** ★★★★
*Done when*: your definition of "the same job", and the precision and recall of your matching on pairs
you labeled [by hand].

**JR4 Application tracker** ★★
*Done when*: every application since this task, with its status over time, recorded in your tool.

**JR5 Evaluation set** ★★★
*Done when*: at least 80 jobs labeled with a written guide, a sealed holdout set (no results on it until
JR10; your git history shows when you first used it), and your agreement with yourself measured.

**JR6 Baseline recommender** ★★★
*Done when*: a recommender and a command that measures it with a metric you chose and justified, checked
[by hand] on 10 examples.

**C2 Gate**: walk us through your evaluation history; we test whether your `CLAUDE.md` stops a repeat
mistake.

**JR7 LLM scorer** ★★★
*Done when*: compared with the baseline, including cost.

**JR8 Your own agent** ★★★★ [hand-written]
An agent that uses tools to reach its decision. No agent framework: you write the loop.
*Done when*: a trace where it chains tool calls, and you can add a tool live without Claude.

**JR9 Guardrails** ★★★★
*Done when*: it cannot run away (turns, cost, failing tools), and it is tested against hostile job
descriptions you wrote, with an honest pass rate.

**JR10 Which one wins** ★★★
*Done when*: baseline, LLM and agent compared; the holdout opened once; an honest report.

**JR11 Daily picks** ★★
*Done when*: every morning your top picks arrive with reasons, and your reactions are captured.

**JR12 Dashboard** ★★★★
*Done when*: a deployed URL showing today's jobs, picks, your pipeline and the health of each source,
with nothing personal visible to someone who is not you.

**JR13 Insights** ★★★★
Find what a job list does not tell you: for example hiring surges, postings that never close, roles
reposted again and again, slowdowns, the share of junior roles, skill trends, salary ranges, your own
funnel.
*Done when*: at least 4 signals, each traceable to its data and showing its sample size, and 10 flagged
signals checked [by hand].

**JR14 It learns from you** ★★★★
*Done when*: a before/after evaluation on at least 2 weeks of new feedback.

**JR15 Interview-ready** ★★★
*Done when*: a design document, and resume bullets where every number traces back to this repo.

**C3 Gate**: a mock technical interview about JobRadar. We keep going deeper to find the edge of what
you can explain; that edge is what to work on next.
