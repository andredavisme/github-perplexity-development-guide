# Chapter 10 — Tracking Progress and Reporting

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

A project that's running well generates data constantly. Every issue created, labeled, moved, and closed is a data point. Every PR merged, every milestone completed, every comment left is part of the record. Most of this data goes unread.

This chapter is about reading it.

Tracking progress isn't just about knowing how much is done — it's about understanding *how* the project is going: whether the pace is sustainable, whether blockers are accumulating, whether the original plan still reflects reality. That understanding is what makes retrospectives honest, reports credible, and future planning more accurate.

This chapter covers:
- The data GitHub already captures about your project
- How to use Perplexity to query and summarize that data
- How to structure a progress report from issue and milestone data
- How to run a lightweight project retrospective
- How to update your plan when reality diverges from it

### What GitHub Tracks Automatically

You don't need to maintain a separate spreadsheet or status document. GitHub captures the following automatically as you work:

| Data | Where It Lives | What It Tells You |
|---|---|---|
| Open vs. closed issues | Issues tab, filterable | How much work remains |
| Issues by label | Label filter view | Distribution by type and status |
| Issues by milestone | Milestone view | Progress toward each phase |
| Milestone completion % | Milestone page | Percentage of issues closed |
| PR merge history | Pull Requests tab | What changed and when |
| Commit history | Commits tab | Activity over time |
| Issue timeline | Individual issue page | Full history of each unit of work |
| Time to close | Issue created/closed dates | How long work actually takes |

All of this is queryable by Perplexity via MCP — in plain language.

### Progress vs. Velocity vs. Health

Three distinct questions about a project's state:

| Question | What You're Measuring | Example |
|---|---|---|
| **Progress** | How much is done relative to the total | *"14 of 20 issues closed in Milestone 2"* |
| **Velocity** | How fast work is moving | *"Averaging 3 issues closed per week"* |
| **Health** | Whether the project is sustainable and on track | *"5 issues are blocked; milestone deadline is in 2 weeks"* |

Progress tells you where you are. Velocity tells you when you'll finish. Health tells you whether there's a problem.

Perplexity can help surface all three — but the interpretation is yours.

### Structuring a Progress Report

A progress report doesn't need to be long. It needs to be honest and specific. A good one answers four questions:

1. **What was planned?** — The original scope (milestone, issue list)
2. **What was completed?** — Closed issues, merged PRs
3. **What's still open?** — Remaining issues, blockers
4. **What changed?** — Scope additions, removals, pivots

This structure works for a weekly check-in, a mid-project review, or a final submission. The data is always the same — the audience and level of detail vary.

### The Retrospective

A **retrospective** (retro) is a structured reflection run at the end of a project phase or the whole project. It's not a status report — it's a learning exercise.

The simplest retro format asks three questions:

- **What went well?** — Practices, decisions, and patterns worth repeating
- **What didn't go well?** — Friction, mistakes, and patterns to avoid
- **What would we do differently?** — Concrete changes for next time

The honest answer to these questions lives in your issue history, your PR comments, and your milestone data. Perplexity can help surface it — issues that took much longer than expected, blockers that appeared repeatedly, milestones that slipped.

### When Reality Diverges from the Plan

It always does. The question isn't whether your plan will change — it's whether you update it when it does.

Common divergences and how to handle them:

| Situation | Response |
|---|---|
| Issue is larger than expected | Break it into sub-issues; update the milestone |
| New work is discovered | Create an issue immediately; decide which milestone it belongs to |
| A milestone will slip | Move incomplete issues to the next milestone; document why |
| A feature is cut | Close the issue with a comment explaining the decision; apply a `wontfix` or `deferred` label |
| A collaborator drops out | Reassign their open issues; flag blockers |

In every case, the right move is to update GitHub to reflect reality — not to leave stale issues and outdated milestones in place.

### Key Terms

| Term | Definition |
|---|---|
| **Velocity** | The rate at which issues are being closed over time |
| **Retrospective** | A structured end-of-phase reflection on what went well, what didn't, and what to change |
| **Milestone completion rate** | The percentage of issues in a milestone that have been closed |
| **Scope creep** | The gradual addition of unplanned work, often without updating the plan to reflect it |
| **Wontfix** | A label convention applied to issues that are deliberately not being resolved |
| **Deferred** | Work that was planned but intentionally moved to a future phase or version |

### After This Chapter You Will Be Able To
- Ask Perplexity for a structured project status summary
- Identify progress, velocity, and health signals in your issue data
- Write a progress report using milestone and issue data
- Run a lightweight retrospective using the three-question format
- Update your plan in GitHub when reality diverges from the original scope

---

## Show

### Demonstration: A Mid-Project Review

Here is how a mid-project review for `github-perplexity-development-guide` would be conducted using Perplexity.

#### Getting a Status Snapshot

> *"Give me a status summary for `andredavisme/github-perplexity-development-guide`. How many issues are open vs. closed? What's the completion rate for each milestone? Are any issues currently labeled `blocked`?"*

Perplexity returns:
- Total open: 6 / Total closed: 14
- Part 1 — Getting Started: 100% complete
- Part 2 — Planning With AI: 100% complete
- Part 3 — Building and Collaborating: 67% complete (4 of 6 closed)
- Part 4 — Reporting and Reflection: 0% complete (not yet started)
- Blocked issues: 1 (issue #11 — waiting on decision about appendix structure)

This is a progress snapshot. It took one prompt.

#### Checking Velocity

> *"Look at the closed issues in `andredavisme/github-perplexity-development-guide`. Based on the created and closed dates, how many issues were closed per week on average? Is the pace accelerating or slowing?"*

Perplexity analyzes the issue timestamps and returns a week-by-week summary, noting whether the pace is holding, accelerating, or has a gap.

#### Identifying Health Signals

> *"List any issues in `andredavisme/github-perplexity-development-guide` that have been open for more than 14 days without a comment. Also list any issues labeled `blocked`."*

This surfaces stale and blocked work — the two most common early-warning signals of a project in trouble.

#### Drafting a Progress Report

> *"Using the issue and milestone data from `andredavisme/github-perplexity-development-guide`, draft a one-page progress report. Structure it as: What was planned, What was completed, What's still open, What changed. Use plain language suitable for a non-technical reader."*

Perplexity drafts the report. The author reviews it for accuracy, adjusts the tone, and uses it as the basis for a submission or team update.

#### Running a Retrospective

At the end of Part 3:

> *"Based on the issue history in `andredavisme/github-perplexity-development-guide` for the Part 3 milestone — including comment threads, label changes, and time to close — help me run a retrospective. What patterns do you see? Which issues took longest? Were there repeated blockers?"*

Perplexity reviews the data and surfaces patterns: which chapters were fastest, where blockers appeared, whether scope additions changed the milestone's shape.

The author adds the human interpretation — *why* those patterns appeared, and *what* to do differently in Part 4.

#### What to Notice

- None of this required maintaining a separate status spreadsheet
- The data was already there — Perplexity surfaced it on request
- The progress report draft is a starting point, not a finished document — the author's judgment is still required
- The retrospective is data-informed, not data-determined — patterns suggest, humans interpret

---

## Do — Lab 10.1

### Run a Project Review

**Objective:** Use Perplexity to generate a status snapshot, draft a progress report, and run a lightweight retrospective on your project so far.

**What you need before starting:**
- Your repository with at least 5–6 closed issues across at least one completed milestone
- Your session context prompt from Lab 3.1

---

### Part A — Get a Status Snapshot

> *"Give me a status summary for `your-username/your-repo-name`. How many issues are open vs. closed? What's the completion rate for each milestone? Are there any blocked or stale issues?"*

Read the response carefully.

**Checkpoint:** You have a clear picture of where the project stands right now.

---

### Part B — Check for Health Signals

> *"List any issues in `your-username/your-repo-name` that have been open for more than 7 days without a comment or label update. Also list any issues currently labeled `blocked`."*

For any issues that surface: update them. Add a comment, reassign, close if irrelevant, or move to a different milestone.

**Checkpoint:** No stale or mislabeled issues remain in your open backlog.

---

### Part C — Draft a Progress Report

> *"Using the issue and milestone data from `your-username/your-repo-name`, draft a progress report covering: what was planned, what was completed, what's still open, and what changed from the original plan. Keep it to one page."*

Review the draft. Edit it for accuracy and tone. Save it as a comment on your most recent milestone issue, or as a file in your repo at `/reports/progress-01.md`.

**Checkpoint:** A progress report exists in your repo or issue history that accurately reflects the project's current state.

---

### Part D — Run a Retrospective

> *"Based on the closed issues and PR history in `your-username/your-repo-name`, help me run a retrospective. What went well? Where did work stall? What took longer than expected?"*

After reading Perplexity's response, write your own answers to:
1. What went well?
2. What didn't go well?
3. What would you do differently from the start?

Keep these brief — three to five bullet points each. Add them as a comment on your project's main tracking issue, or save as `retro.md` in your repo.

**Checkpoint:** A retro document exists with your honest, specific answers.

---

### Part E — Update the Plan

Based on what you learned in the retro:
- Move any incomplete issues from a past milestone into the appropriate upcoming milestone
- Close any issues that are no longer relevant (with a comment explaining why)
- Create any new issues that the retro surfaced

**Checkpoint:** Your backlog accurately reflects what you actually intend to do next.

---

### Reflection Questions

1. What did the status snapshot tell you that you didn't already know? What surprised you?
2. Compare the progress report Perplexity drafted with what you would have written from memory. What did it include that you would have missed? What did it miss that you knew?
3. What's the most useful thing a retrospective does that a status report doesn't?

---

## Wrap-Up

The data was always there. This chapter was about learning to read it.

A project tracked in GitHub — with labeled issues, milestone-assigned work, closing comments, and structured PRs — generates a complete record of how the work actually went. Perplexity can surface that record on demand, in plain language, at any level of detail.

That record is the foundation of **Chapter 11**, the final chapter: a full project retrospective and guide to carrying these practices forward into the next project — and the one after that.

---

**Next:** [Chapter 11 — Closing Out and Carrying Forward](../11-closing/README.md)
