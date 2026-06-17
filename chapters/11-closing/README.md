# Chapter 11 — Closing Out and Carrying Forward

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

This is the last chapter. The project is (nearly) done.

Closing a project well is a skill in its own right. It's tempting to simply stop working when the deliverables are finished — but a project that ends without a proper close-out leaves loose ends, unresolved questions, and missed opportunities to learn. A project that *does* close out properly leaves a clean record, a useful retrospective, and a foundation that makes the next project faster and better.

This chapter covers:
- How to formally close a project in GitHub
- What a complete project record looks like
- How to write a final retrospective
- How to extract reusable assets from this project for the next one
- How to carry the workflow forward independently

### What "Closed" Means

A project is closed when:

1. All planned issues are either **closed** (completed) or **deliberately deferred** (with a comment explaining why)
2. All open PRs are **merged or closed**
3. All milestones are **marked complete** or carried forward with updated dates
4. The project board reflects the **actual final state** of the work
5. A **final retrospective** exists in the repo

Note that "closed" doesn't mean "perfect." Some issues will be deferred. Some features won't make the cut. That's normal — what matters is that every open item has been *consciously resolved*, not just abandoned.

### Closing Issues That Won't Be Completed

Not every issue gets done. The right response is not to leave them open indefinitely — it's to close them with intent.

| Situation | Label to Apply | Closing Comment |
|---|---|---|
| Decided not to build this | `wontfix` | *"Descoped. Not aligned with final project direction."* |
| Worth doing later | `deferred` | *"Moving to v2. Will revisit after launch."* |
| Duplicate of another issue | `duplicate` | *"Covered by #[number]."* |
| No longer relevant | `stale` | *"Context changed. No longer applicable."* |

Every closed issue — even a deferred or wontfix one — should have a closing comment. Future you will thank present you.

### Archiving vs. Leaving Open

GitHub allows repositories to be **archived** — made read-only while preserving the full history. Archived repos:
- Cannot receive new issues, PRs, or commits
- Remain fully visible and browsable
- Are clearly marked as archived in the GitHub UI

Archive a repository when:
- The project is genuinely complete and won't be continued
- You want to preserve the record without the overhead of maintaining it
- The repo is a course project being handed off or submitted

Don't archive if you expect to return to the project, fork it, or build on it.

### The Reusable Assets

Every project produces assets worth carrying forward. For the GitHub + Perplexity workflow, those assets are:

| Asset | Where It Lives | How to Reuse |
|---|---|---|
| **Session context prompt** | Lab 3.1 notes or a saved file | Update the repo name and milestone; reuse immediately |
| **Label taxonomy** | `.github/labels.yml` (if exported) | Import directly into a new repo |
| **Issue templates** | `.github/ISSUE_TEMPLATE/` | Copy the folder to any new repo |
| **PR template** | `.github/pull_request_template.md` | Copy to any new repo |
| **Milestone structure** | Model from this project | Adapt phase names; keep the pattern |
| **Retrospective** | `retro.md` in the repo | Read before starting the next project |

The session context prompt and templates are the highest-value items. With those two things, a new project can be set up in under ten minutes.

### Carrying the Workflow Forward

The practices in this book work because they're consistent. The value compounds across projects: each retro informs the next plan, each template gets refined, each prompt gets sharper.

The three habits that matter most in the long run:

1. **Start every project with structure** — repo, labels, milestones, templates, session context prompt. Don't start work until the scaffold is in place.
2. **Close issues with comments** — always, without exception. The habit is more important than the length of the comment.
3. **Run a retro at the end of every phase** — not just the end of the project. Short phases with frequent retros improve faster than long phases with one final review.

Perplexity makes all of this faster. But the discipline behind it is yours.

### Key Terms

| Term | Definition |
|---|---|
| **Project close-out** | The deliberate process of resolving all open items, documenting outcomes, and formally ending a project |
| **Archived repository** | A GitHub repository set to read-only, preserving the full record without ongoing maintenance |
| **Reusable asset** | A template, prompt, or configuration file created during one project that can be directly reused in the next |
| **Final retrospective** | A structured reflection written at the end of the whole project, covering the full arc from start to finish |

### After This Chapter You Will Be Able To
- Close all open issues deliberately, with appropriate labels and comments
- Mark milestones complete and resolve any outstanding PRs
- Write a final retrospective for the whole project
- Identify and export the reusable assets from this project
- Set up a new project using those assets in under ten minutes

---

## Show

### Demonstration: Closing Out This Guide

Here is what the close-out of `github-perplexity-development-guide` looks like — the final sequence of actions that completes the project record.

#### Step 1: Final Status Check

> *"List all open issues and open PRs in `andredavisme/github-perplexity-development-guide`. Group them by milestone."*

Perplexity returns the full open list. The author reviews each item and decides: complete it, defer it, or close it as wontfix.

#### Step 2: Close or Defer Everything Open

> *"Close issue #18 with the label `deferred` and the comment: 'Glossary appendix deferred to v2. Scope finalized without it.'"*

> *"Close issue #19 with the label `wontfix` and the comment: 'Video companion content descoped. Out of scope for v1.'"*

Every open issue is now resolved — completed, deferred, or explicitly declined.

#### Step 3: Verify the Board

The project board is checked manually. All cards should be in Done or have been removed. Any card still in Backlog or In Progress corresponds to an issue that needs to be closed.

#### Step 4: Write the Final Retrospective

> *"Based on the full issue and PR history of `andredavisme/github-perplexity-development-guide` — from the first commit to today — help me write a final project retrospective. Cover: what the project set out to do, what was completed, what was deferred, what worked well in the workflow, and what I'd do differently if starting over."*

Perplexity drafts a data-informed retrospective. The author revises it with honest personal reflection and saves it as `retro-final.md` in the repo root.

#### Step 5: Export Reusable Assets

The author confirms the following files are in good shape for reuse:
- `.github/ISSUE_TEMPLATE/` — all four templates
- `.github/pull_request_template.md`
- Session context prompt (saved locally)
- Milestone structure notes

#### Step 6: Archive (Optional)

If the project is being submitted as a course deliverable:

1. Repo → **Settings** → scroll to **Danger Zone**
2. Click **Archive this repository**
3. Confirm

The repo is now read-only and preserved exactly as submitted.

#### What to Notice

- Every open item was resolved *consciously* — no issue was simply abandoned
- The final retro is data-informed (Perplexity) but author-voiced (human revision)
- The reusable assets mean the next project starts with this project's best practices already in place
- The archive step is optional — but if it's used, it signals a clean, intentional ending

---

## Do — Lab 11.1

### Close Out Your Project

**Objective:** Bring your project to a clean, complete close — resolving all open items, writing a final retrospective, and extracting your reusable assets for the next project.

**What you need before starting:**
- Your repository in whatever state it's in right now
- Honest answers about what's actually done vs. what isn't

---

### Part A — Final Status Check

> *"List all open issues and open PRs in `your-username/your-repo-name`. Group them by milestone and label."*

For each open item, decide:
- **Complete it now** — if it's small and worth doing
- **Defer it** — if it belongs in a future phase
- **Close it as wontfix** — if it's no longer relevant

**Checkpoint:** Zero open issues that haven't been consciously resolved.

---

### Part B — Close or Resolve Everything

For each remaining open issue, ask Perplexity:

> *"Close issue #[number] in `your-username/your-repo-name` with label `[deferred/wontfix/stale]` and comment: '[one sentence explaining the decision].'"*

**Checkpoint:** Every issue in your repo is either closed or has an active owner and a next action.

---

### Part C — Write the Final Retrospective

> *"Based on the full issue and PR history of `your-username/your-repo-name`, help me write a final project retrospective. Cover: what the project set out to do, what was completed, what was deferred, what worked well, and what I'd do differently."*

Read the draft carefully. Revise it in your own voice. Be specific and honest — a retro that says "everything went fine" is not useful.

Save the final version as `retro-final.md` in your repo root and commit it.

**Checkpoint:** `retro-final.md` exists in your repo with specific, honest content.

---

### Part D — Collect Your Reusable Assets

Confirm each of the following is in good shape:

- [ ] `.github/ISSUE_TEMPLATE/` — all four templates present and correct
- [ ] `.github/pull_request_template.md` — complete and using the standard structure
- [ ] Session context prompt — saved somewhere you'll find it (a notes app, a local file, a new repo)
- [ ] Milestone structure — noted for reuse (phase names, the pattern)

**Checkpoint:** You could set up a new project with these assets in under ten minutes.

---

### Part E — Archive or Leave Open

Decide: is this project complete, or will you continue building on it?

- **If complete:** Archive the repo (Settings → Danger Zone → Archive)
- **If continuing:** Leave it open, create a new milestone for the next phase, and move any deferred issues into it

**Checkpoint:** The repository's state reflects your honest intent for it.

---

### Final Reflection

This isn't a set of questions to answer in your repo. These are questions to sit with.

1. At the start of this project, what did you think "using GitHub" meant? What does it mean to you now?
2. What did Perplexity make genuinely easier? What still required your judgment, your knowledge, your decisions?
3. If you were explaining this workflow to someone starting their first project tomorrow, what would you tell them first?

---

## Closing

You started this book with an empty repository and a set of habits to build.

You now have a structured project record — labeled issues, milestone-assigned work, PR history, closing comments, a retrospective — and a set of reusable assets that make the next project faster from day one.

The workflow is yours. Perplexity is a capable partner, but the discipline behind it — the consistency, the honesty, the habit of closing things cleanly — is something you bring. That's not something a tool can do for you.

Use it well.

---

*End of the GitHub + Perplexity Development Guide.*

[← Table of Contents](../../README.md)
