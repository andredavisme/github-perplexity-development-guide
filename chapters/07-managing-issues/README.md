# Chapter 7 — Managing Issues with Perplexity

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

Part 2 was about setting up the conditions for good work. Part 3 is about doing it.

With your repository structured, your backlog populated, and your project board live, you now have everything Perplexity needs to act as an active project partner. This chapter covers the day-to-day mechanics of that partnership — how to use Perplexity to keep your project moving, your issues accurate, and your progress visible.

Specifically, you'll learn how to:
- Update issue labels, assignees, and status via conversation
- Add comments to issues as a running log of progress
- Close issues cleanly when work is complete
- Create new issues mid-project as scope evolves
- Handle the natural messiness of real projects without losing structure

### Issues as a Living Record

An issue isn't just a to-do item. Over the course of its life, it becomes a **record** — of what was planned, what changed, what decisions were made, and what was ultimately done.

This happens through comments. A comment thread on an issue is a lightweight log:
- *"Starting this today. Current approach: X."*
- *"Hit a blocker — waiting on decision about Y."*
- *"Resolved. Went with approach Z. Closing."*

When Perplexity adds a comment before closing an issue, that record is preserved automatically. Six months later, anyone (including you) can open that issue and understand exactly what happened.

### The Issue Lifecycle

Every issue moves through a predictable lifecycle. Understanding it helps you know which action to take at each stage.

```
Created → Labeled → Assigned → In Progress → Needs Review → Closed
```

| Stage | What It Means | Action in GitHub |
|---|---|---|
| **Created** | Issue exists in the backlog | Add to board, assign milestone |
| **Labeled** | Type and status are clear | Apply `feature`, `task`, `bug`, or `question` |
| **Assigned** | Someone owns it | Set assignee |
| **In Progress** | Work has started | Add `in-progress` label |
| **Needs Review** | Work is done, awaiting check | Swap to `needs-review` label |
| **Closed** | Verified complete | Close issue (triggers board automation) |

Perplexity can act at every one of these stages through conversation.

### What Good Issue Management Looks Like

Good issue management is not about perfection — it's about **consistency**. A project where every issue has a label, every closed issue has a closing comment, and every blocker is flagged is a project that's easy to navigate, easy to hand off, and easy to resume after a break.

The habits that matter most:
- **Label before starting** — apply `in-progress` when you pick up an issue
- **Comment before closing** — leave a one-sentence note about what was done
- **Create issues for new work immediately** — don't let undocumented work accumulate
- **Flag blockers explicitly** — apply `blocked` and describe what's blocking in a comment

None of these take more than a sentence. Perplexity can handle all of them in a single instruction.

### Key Terms

| Term | Definition |
|---|---|
| **Issue Lifecycle** | The stages an issue moves through from creation to closure |
| **Comment** | A message added to an issue thread, used for progress updates, decisions, and notes |
| **Closing Comment** | A final comment added just before closing an issue that summarizes what was done |
| **Scope Creep** | The gradual expansion of a project beyond its original boundaries, often discovered mid-work |
| **Backlog Hygiene** | The practice of keeping the issue list accurate, labeled, and free of stale or irrelevant items |

### After This Chapter You Will Be Able To
- Update issue labels and assignees via Perplexity
- Add progress comments to issues through conversation
- Close issues with a closing comment in a single instruction
- Create new issues mid-project without disrupting existing structure
- Flag and describe blockers in a way that's visible to collaborators

---

## Show

### Demonstration: A Day of Active Issue Management

Here is what a realistic working session with Perplexity looks like on an active project. Each interaction is a single instruction — Perplexity handles the GitHub action directly.

#### Starting the Session

First, orient Perplexity with the session context prompt:

> *"We're working on `andredavisme/github-perplexity-development-guide`. Last completed: Chapter 6. Active milestone: Part 3: Building and Collaborating. Open issues include writing Chapters 7, 8, and 9. Let's work on Chapter 7 today."*

#### Picking Up an Issue

> *"Find the issue for writing Chapter 7. Add the `in-progress` label and assign it to `andredavisme`."*

Perplexity finds the issue, applies the label, and sets the assignee. The board card, if automation is configured, reflects the status change.

#### Logging Progress Mid-Work

> *"Add a comment to the Chapter 7 issue: 'Tell and Show sections complete. Working on the Do section now.'"*

This comment becomes part of the issue's permanent record. If work is interrupted, anyone returning to the issue knows exactly where it stands.

#### Hitting a Blocker

> *"On the Chapter 7 issue: add the `blocked` label and a comment explaining that we're waiting on a decision about whether to include a glossary appendix before finalizing the Key Terms structure."*

The `blocked` label makes this visible in filtered views. The comment explains the specific dependency.

#### Resolving and Closing

> *"The Chapter 7 issue is complete. Remove the `blocked` and `in-progress` labels, add `needs-review`, and leave a comment: 'Full Tell/Show/Do/Wrap-Up written and pushed. Ready for review.'"*

Later, after review:

> *"Close the Chapter 7 issue with a comment: 'Reviewed and approved. Chapter live in repo.'"*

The issue closes. The board card moves to Done automatically.

#### Creating a New Issue Mid-Project

During work on Chapter 7, a new need was identified:

> *"Create a new task issue titled 'Add glossary appendix to repo'. Label it `feature`, assign it to the Part 3 milestone, and add a description: 'A reference glossary of all key terms defined across chapters 1–7. Format as a single alphabetized markdown file at /appendix/glossary.md.'"*

New scope is captured immediately, structured correctly, and added to the backlog — without disrupting work in progress.

#### What to Notice

- Every instruction is a single, plain-language sentence or two
- The repo reference is established once at session start, not repeated each time
- Comments are used as a log, not just for communication
- New issues are created with full structure (label, milestone, description) from the start

---

## Do — Lab 7.1

### Run a Full Issue Lifecycle

**Objective:** Use Perplexity to move one of your project issues through its complete lifecycle — from backlog to closed — logging progress at each stage.

**What you need before starting:**
- Your session context prompt from Lab 3.1
- At least one open issue in your repository from Labs 4 or 5
- A small piece of actual work you can complete during this lab (even just writing a paragraph or updating a file)

---

### Part A — Start the Session

Open a new Perplexity conversation. Paste your session context prompt, then ask:

> *"List my open issues in `your-username/your-repo-name` with their current labels and milestones."*

**Checkpoint:** Perplexity returns a list of your open issues with labels and milestones visible.

---

### Part B — Pick Up an Issue

Choose one issue to work on. Tell Perplexity:

> *"Apply the `in-progress` label to issue #[number] and assign it to me."*

**Checkpoint:** The issue now has the `in-progress` label in GitHub.

---

### Part C — Do the Work and Log Progress

Do a small piece of actual work related to that issue (write something, update a file, make a decision). Then:

> *"Add a comment to issue #[number]: '[Brief description of what you just did and what's next].'"*

**Checkpoint:** The issue has a comment describing your progress.

---

### Part D — Close the Issue

When the work is done:

> *"Close issue #[number] with a comment: '[One sentence describing what was completed].'"*

**Checkpoint:** The issue is closed. If your board automation is set up, verify the card has moved to Done.

---

### Part E — Create a New Issue

Think of something new that came up during your work — a follow-on task, a question that needs answering, or a feature you want to add. Create it immediately:

> *"Create a [type] issue titled '[verb-noun title]'. Label it `[label]`, assign it to the `[milestone]` milestone, and describe it as: '[one or two sentences].'"*

**Checkpoint:** A new, fully structured issue appears in your backlog.

---

### Reflection Questions

1. How did leaving a closing comment change the way the closed issue reads now? What would it look like without one?
2. Did anything come up during the work that you didn't anticipate? How did you handle it in terms of issues?
3. Imagine handing this project to someone else right now. Based on the issue state alone, what would they know? What would still be unclear?

---

## Wrap-Up

You've now run a complete issue lifecycle with Perplexity as your active partner — picking up work, logging progress, handling interruptions, closing cleanly, and capturing new scope as it emerges.

This is the core loop of the workflow. Everything else in this book is a refinement of it.

In **Chapter 8**, the loop expands to include code changes and collaboration. Pull requests are the mechanism GitHub uses to propose, review, and merge changes — and they connect directly to issues in ways that make the project record even richer and more complete.

---

**Next:** [Chapter 8 — Pull Requests and Code Review](../08-pull-requests/README.md)
