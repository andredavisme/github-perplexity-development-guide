# Chapter 12 — Presenting and Sharing Your Project

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

Your project is complete. The issues are closed, the retrospective is written, the repository is clean. Now someone else needs to understand it — a professor reviewing a submission, a hiring manager evaluating your portfolio, a collaborator deciding whether to contribute, or a future version of you returning after six months away.

This chapter is about making your project legible to an outside audience.

Legibility isn’t the same as documentation. Documentation is for people who will *use* the project. Legibility is for people who need to *evaluate* or *understand* it quickly — people who won’t read every file but will form a strong impression from the first things they see.

This chapter covers:
- What a reader-facing repository looks like vs. a working repository
- How to write a README that communicates the project’s value and structure
- How to use GitHub’s built-in features to present your work professionally
- How to share a project — as a portfolio piece, a submission, or a public contribution
- How Perplexity can help draft and refine the reader-facing layer

### The Two Audiences for Your Repository

While building, your primary audience is yourself and your collaborators. Issues use shorthand, commit messages are functional, labels are operational.

When presenting, a second audience appears: someone who wasn’t there.

| Audience | What They Need | Where They Look |
|---|---|---|
| **Builder** | Operational detail, current state, next actions | Issues, project board, PR queue |
| **Reader** | Context, scope, outcomes, how to navigate | README, closed milestones, commit history |

A repository built with good habits — verb-noun issue titles, closing comments, milestone structure — is already most of the way to reader-ready. The remaining step is a well-written README and a clean top-level structure.

### The README as Front Door

The README is the first thing anyone sees when they open your repository. It has one job: answer *"What is this, and should I keep reading?"* within 30 seconds.

A strong project README has five elements:

| Element | Purpose | Example |
|---|---|---|
| **Project name + one-line description** | Immediate orientation | *"BudgetTrack — A personal finance tracker built with React and GitHub Actions"* |
| **What it does** | 2–3 sentences on scope and outcome | What problem it solves, what it produces |
| **How to use it / navigate it** | Entry point for the reader | Setup instructions, or folder structure for non-code projects |
| **What’s included** | Key deliverables and where to find them | Links to chapters, reports, templates, or deployed output |
| **Status** | Honest current state | *"Complete — v1 submitted June 2026"* or *"Active — v2 in progress"* |

What to leave out: setup instructions for contributors (that’s a CONTRIBUTING.md), exhaustive feature lists, and anything that would only matter to someone already working on the project.

### GitHub’s Built-In Presentation Features

GitHub surfaces several signals that communicate project quality without any extra effort — if the underlying work is structured:

| Feature | What It Shows | How to Optimise |
|---|---|---|
| **Closed milestones** | Phases of work completed | Name milestones clearly; close them when done |
| **Contributor graph** | Who worked on it and when | Natural outcome of good commit and PR habits |
| **Issue history** | The decision trail | Closing comments and label changes tell the story |
| **Commit messages** | What changed and why | Verb-noun titles; reference issue numbers |
| **Topics/tags** | Discoverability | Add 3–5 relevant topics in repo Settings |

A reader who clicks through closed milestones, scans closed issues, and reads a handful of PR descriptions can reconstruct the entire arc of the project — without asking you a single question.

### Sharing Formats

Depending on the purpose, a project can be shared in different ways:

| Format | When to Use | How to Prepare |
|---|---|---|
| **Public repository link** | Portfolio, open-source, peer review | Ensure README is complete; add repo topics |
| **Archived repository** | Course submission, version snapshot | Archive after final commit (see Chapter 11) |
| **GitHub Pages** | Published output (site, docs, report) | Enable Pages in Settings; point to correct branch/folder |
| **Exported report** | Non-GitHub audiences (professors, clients) | Use Perplexity to draft from issue/milestone data |

### How Perplexity Helps With Presentation

Perplexity can draft the reader-facing layer from the project’s existing data:
- Generate a README draft from the repo structure and issue history
- Summarise closed milestones into a project narrative
- Draft a project summary suitable for a portfolio or CV
- Identify gaps in the repo that a reader would notice

As with the retrospective in Chapter 10, Perplexity’s draft is a starting point. The author’s voice, judgment, and honest account of outcomes are what make it credible.

### Key Terms

| Term | Definition |
|---|---|
| **README** | The markdown file displayed on a repository’s main page; the primary reader-facing document |
| **GitHub Pages** | A GitHub feature that publishes a repository’s content as a live website |
| **Repo topics** | Tags added to a repository that improve discoverability in GitHub search |
| **CONTRIBUTING.md** | A file explaining how external contributors can participate in a project |
| **Portfolio piece** | A project presented as evidence of skill or process for an external audience |

### After This Chapter You Will Be Able To
- Write a README that orients a reader in under 30 seconds
- Identify which GitHub built-in features signal project quality to an outside reader
- Choose the right sharing format for your audience
- Use Perplexity to draft reader-facing content from your project’s existing data
- Present your project confidently as a portfolio piece or course submission

---

## Show

### Demonstration: Making This Guide Reader-Ready

Here is how `github-perplexity-development-guide` would be prepared for a reader who had no involvement in its creation.

#### Step 1: Draft the README

> *"Based on the structure and issue history of `andredavisme/github-perplexity-development-guide`, draft a README that would orient a reader who has never seen this project. Include: what the project is, who it’s for, how it’s structured, and its current status."*

Perplexity reads the repo and drafts a README. The author reviews it, adjusts the tone, updates the status line, and commits it.

#### Step 2: Add Repository Topics

In the repo → **About** (gear icon, top right of the main page):

Add topics: `github`, `perplexity`, `project-management`, `education`, `workflow`

Topics make the repo discoverable and signal its category at a glance.

#### Step 3: Verify the Closed Milestones Tell the Story

Click through each closed milestone. Check that:
- The milestone name is clear to an outsider (*"Part 1: Getting Started"* ✔, *"Phase 1"* ✘)
- The closed issues within it have closing comments
- The completion date is reasonable

If any milestone names are too internal, rename them before presenting.

#### Step 4: Check the Commit History

Scan the last 20 commits. A reader will see these. Ask:
- Are the messages descriptive? (*"Write Chapter 7: Managing Issues with Perplexity"* ✔, *"updates"* ✘)
- Is there a commit that looks unfinished or confusing?

One cleanup commit with a clear message is better than leaving visible mess.

#### Step 5: Draft a Portfolio Summary

> *"Based on `andredavisme/github-perplexity-development-guide`, write a 3–5 sentence portfolio description I could use on a CV or personal site. Emphasise the scope, the workflow demonstrated, and the outcome."*

Perplexity drafts it. The author refines it in their own voice.

#### What to Notice

- Most of the presentation work was already done by good habits during the project — the README draft and milestone story are only possible because the issues and commits were structured
- Adding topics takes 90 seconds and significantly improves discoverability
- The portfolio summary is Perplexity’s draft, but the final voice must be the author’s — a portfolio piece that sounds like an AI wrote it is not a strong portfolio piece

---

## Do — Lab 12.1

### Make Your Project Reader-Ready

**Objective:** Prepare your repository for an outside audience — write a clear README, verify the project record is legible, and produce one piece of shareable output.

**What you need before starting:**
- Your completed (or substantially complete) repository
- A sense of who will be reading it (professor, peers, portfolio reviewers, future self)

---

### Part A — Draft the README

> *"Based on the structure and content of `your-username/your-repo-name`, draft a README for an outside reader. Include: what the project is, who it’s for, what’s included, and its current status."*

Review the draft. Edit for accuracy, tone, and your own voice. Make sure the status line is honest.

Commit the updated README to `main`.

**Checkpoint:** The README answers *"What is this, and should I keep reading?"* within 30 seconds.

---

### Part B — Add Topics and Clean Up the About Section

1. Go to your repo → click the gear icon next to **About**
2. Add 3–5 relevant topics
3. Add a one-line description if it’s missing
4. Add your project website if applicable (GitHub Pages URL, or leave blank)

**Checkpoint:** Your repo’s About section accurately describes the project in one line, with topics visible.

---

### Part C — Verify the Record

Spend five minutes navigating your repo as if you’d never seen it before:
- Read the closed milestones — do they tell the story of the project?
- Open three closed issues at random — do they have closing comments?
- Scan the last 20 commit messages — are they descriptive?

Fix anything that would leave a reader confused. One cleanup commit is fine.

**Checkpoint:** A reader navigating the repo for the first time can reconstruct the project arc without asking you anything.

---

### Part D — Produce One Shareable Output

Choose one output appropriate for your audience:

**Option A — Portfolio summary:**
> *"Write a 3–5 sentence portfolio description of `your-username/your-repo-name` I could use on a CV or personal site."*

**Option B — Course submission summary:**
> *"Write a one-page project summary for `your-username/your-repo-name` covering: what was planned, what was built, what was learned. Suitable for academic submission."*

**Option C — Public README for GitHub Pages:**
Enable GitHub Pages (Settings → Pages → Deploy from branch: `main`, folder: `/ (root)`) and verify your README renders as a readable web page.

Revise Perplexity’s draft in your own voice before using it.

**Checkpoint:** One shareable output exists that you would be comfortable sending to its intended audience today.

---

### Reflection Questions

1. What did you change in the README draft Perplexity produced? What did it get right about your project that surprised you?
2. When you navigated the repo as an outsider, what was the strongest signal of quality you found? What was the weakest?
3. Who is the most important reader of this project — and what would they need to see to be impressed?

---

## Wrap-Up

A project that ends with a clean repository, a clear README, and a legible record isn’t just done — it’s useful. It can be forked, built on, submitted, cited, and returned to. The work doesn’t disappear when the deadline passes.

That’s the full arc of this book: from an empty repository and a vague project idea, through structured planning, active building, honest tracking, and now — a project worth showing.

The workflow is documented in the chapters behind you. The habits are the ones you’ve been practising since Chapter 1. The next project starts whenever you’re ready.

---

*End of the GitHub + Perplexity Development Guide.*

[← Table of Contents](../../README.md)
