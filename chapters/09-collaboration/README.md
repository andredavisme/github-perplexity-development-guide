# Chapter 9 — Collaboration and Shared Conventions

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

Everything covered so far has assumed a single person working on a single project. That's a reasonable starting point — most projects begin alone. But GitHub is fundamentally a collaborative platform, and the conventions you've been building (labels, milestones, verb-noun titles, PR templates, closing keywords) pay their biggest dividends when other people are involved.

Collaboration introduces new complexity: multiple contributors making changes at the same time, different interpretations of conventions, questions about who has permission to do what, and the social dynamics of reviewing someone else's work. This chapter covers how to navigate all of it.

Specifically, you'll learn:
- The difference between collaborators and contributors
- How to add collaborators to a repository
- How forking works and when it's used
- The etiquette of contributing to someone else's project
- How shared conventions protect collaboration from confusion
- How Perplexity fits into a multi-contributor workflow

### Collaborators vs. Contributors

Not everyone who contributes to a project has the same relationship to it. GitHub distinguishes two main roles:

| Role | Access | How They Contribute |
|---|---|---|
| **Collaborator** | Direct write access to the repository | Commits to branches, opens PRs, manages issues directly |
| **Contributor** | No direct access | Forks the repo, makes changes in their fork, opens a PR from fork to original |

For a class project or small team, **collaborators** is the right model — everyone works in the same repository with shared access. For open-source projects or external contributions, **forking** is the norm.

### Adding Collaborators

To give someone direct access to your repository:

1. Go to your repo → **Settings** → **Collaborators**
2. Click **Add people**
3. Enter their GitHub username
4. They receive an invitation by email; access is granted when they accept

Collaborators can push to branches, open and close issues, and merge PRs (depending on branch protection rules). They cannot change repository settings unless given admin access.

### Forking

A **fork** is a personal copy of someone else's repository, stored under your own GitHub account. Forking is how you contribute to a project you don't have direct write access to.

The fork workflow:

```
Original repo (andredavisme/project)
        |
        ▼
Fork (contributor/project)     ← your personal copy
        |
        ▼
Branch in your fork            ← make your changes here
        |
        ▼
Pull Request: fork → original  ← propose your changes
        |
        ▼
Merged into original repo      ← if accepted
```

The original repository's owner reviews and decides whether to accept your PR. You never touch their `main` branch directly.

### Branch Protection Rules

In collaborative repositories, it's common to protect the `main` branch from direct pushes. **Branch protection rules** enforce that all changes to `main` must go through a reviewed and approved PR.

Common rules to enable:
- **Require a pull request before merging** — no direct commits to `main`
- **Require at least 1 approval** — someone else must review before merge
- **Require status checks to pass** — automated tests must succeed
- **Dismiss stale reviews** — approval resets if new commits are pushed

To configure: repo → **Settings** → **Branches** → **Add rule**.

### The Role of Shared Conventions

Shared conventions are agreements about *how* work gets done — and they matter most when more than one person is doing it.

Without conventions, a collaborative project quickly becomes:
- Issues with inconsistent titles (some verb-noun, some not)
- Labels used differently by different contributors
- PRs that don't link to issues
- Commits with messages like "fixes" or "updates"
- No clear way to tell what's in progress vs. abandoned

With conventions, a new collaborator can open the repo, read the issues and PRs, and understand exactly what's happening — without asking anyone.

The conventions in this book aren't arbitrary preferences. They're the minimum shared vocabulary that makes collaboration legible.

### Contribution Etiquette

When contributing to someone else's project — or reviewing a contribution to yours — a few principles apply:

**As a contributor:**
- Read the existing issues and PRs before opening a new one — your idea may already exist
- Follow the project's conventions exactly, even if you'd do it differently
- Keep PRs focused — one change, one PR
- Respond to review feedback promptly and professionally
- Don't take it personally if a PR is declined

**As a maintainer reviewing contributions:**
- Review promptly — leaving a PR unreviewed for weeks discourages future contributors
- Be specific in feedback (see Chapter 8)
- Acknowledge the contribution even when requesting changes
- Close PRs that won't be merged with a clear, respectful explanation

### How Perplexity Fits in a Multi-Contributor Workflow

Perplexity's role doesn't change in a collaborative context, but its value compounds. Because Perplexity uses the same structured issue data that all collaborators share, it can:

- Give any contributor an instant summary of project status
- Create issues that follow the team's conventions automatically
- Review open PRs and summarize what's waiting for attention
- Flag issues that are unassigned, mislabeled, or past their milestone

One important note: **Perplexity acts as the authenticated user**. In a shared repository, any issue Perplexity creates, closes, or comments on will appear under your account. Make this clear to collaborators so actions taken via Perplexity aren't attributed to you unexpectedly.

### Key Terms

| Term | Definition |
|---|---|
| **Collaborator** | A GitHub user with direct write access to a repository |
| **Contributor** | A GitHub user who contributes via a fork and pull request, without direct write access |
| **Fork** | A personal copy of another user's repository, stored under your own account |
| **Branch protection rule** | A repository setting that restricts how changes can be made to a specific branch |
| **Upstream** | The original repository that a fork was created from |
| **Maintainer** | The person (or team) responsible for reviewing contributions and managing the repository |

### After This Chapter You Will Be Able To
- Add a collaborator to your repository
- Explain the difference between a collaborator and a fork-based contributor
- Configure basic branch protection rules on `main`
- Describe the conventions that make a project legible to a new collaborator
- Contribute to someone else's repository using the fork workflow
- Use Perplexity to surface project status for any collaborator

---

## Show

### Demonstration: Onboarding a Collaborator

Here is what it looks like to bring a new collaborator into `github-perplexity-development-guide` and get them oriented using Perplexity.

#### Step 1: Add the Collaborator

Via GitHub UI:
1. Repo → **Settings** → **Collaborators** → **Add people**
2. Enter their username, send the invitation

They accept the invitation and now have write access.

#### Step 2: Orient Them with Perplexity

The new collaborator starts their first session:

> *"I'm a new collaborator on `andredavisme/github-perplexity-development-guide`. Can you give me an overview of the current project state — what milestones exist, how many open issues are in each, and which issues are currently labeled `in-progress`?"*

Perplexity reads the repository and returns a structured summary — milestones, open issue counts, active work — in seconds. No lengthy onboarding document required.

#### Step 3: Assign First Work

> *"Assign issue #12 to `new-collaborator-username` and add a comment: 'Picked up by [name] as first contribution. Starting with the Tell section.'"*

#### Step 4: They Work on a Branch

The new collaborator creates a branch, makes their changes, and opens a PR:

> *"Open a pull request from `chapter-10-draft` to `main` in `andredavisme/github-perplexity-development-guide`. Title: 'Add Chapter 10: Tracking Progress and Reporting'. Description: 'First draft of Chapter 10 Tell and Show sections. Closes #12. Ready for review.'"*

#### Step 5: Review the PR

The maintainer reviews:

> *"Get the diff of PR #12 in `andredavisme/github-perplexity-development-guide`."*

Perplexity returns the full diff. The maintainer reads it and leaves review comments:

> *"Add a review comment to PR #12 on line 34 of `chapters/10-tracking/README.md`: 'The Key Terms table is missing the definition for Sprint. Can you add it?'"*

#### Step 6: Approve and Merge

After revisions:

> *"Approve PR #12 and merge it into `main` in `andredavisme/github-perplexity-development-guide`."*

Issue #12 closes. The collaborator's first contribution is merged and recorded.

#### What to Notice

- The new collaborator got a full project briefing from Perplexity without any manual preparation by the maintainer
- Every action followed established conventions — verb-noun PR title, closing keyword, review comment on a specific line
- Perplexity participated on both sides: orienting the collaborator and helping the maintainer review
- The project record is richer for having the contributor's branch, PR, and comments in the history

---

## Do — Lab 9.1

### Add a Collaborator and Run a Shared Workflow

**Objective:** Add a classmate as a collaborator, assign them an issue, review their PR, and merge it — using Perplexity to orient them and assist the review.

**What you need before starting:**
- Your repository with at least two open issues
- A classmate willing to be your collaborator (you can do this lab in pairs, each being the other's collaborator)

---

### Part A — Add the Collaborator

1. Go to your repo → **Settings** → **Collaborators** → **Add people**
2. Enter your classmate's GitHub username
3. They accept the invitation

**Checkpoint:** Your classmate appears in the Collaborators list with Pending or Active status.

---

### Part B — Orient Them with Perplexity

Your classmate runs this prompt in their own Perplexity session:

> *"I'm a new collaborator on `your-username/your-repo-name`. Give me an overview of the project: what milestones exist, how many open issues are in each, and which issues are unassigned."*

**Checkpoint:** Perplexity returns a coherent project summary without any manual explanation from you.

---

### Part C — Assign and Work

Assign one open issue to your classmate:

> *"Assign issue #[number] in `your-username/your-repo-name` to `classmate-username` and add a comment welcoming them to the project."*

Your classmate creates a branch, makes a change, and opens a PR with a closing keyword.

**Checkpoint:** A PR exists from your classmate's branch to `main`, linked to the assigned issue.

---

### Part D — Review and Merge

Review the PR:

> *"Get the diff of PR #[number] in `your-username/your-repo-name`."*

Leave at least one specific review comment. Then approve and merge:

> *"Approve and merge PR #[number] in `your-username/your-repo-name`."*

**Checkpoint:** The PR is merged, the issue is closed, and the board card (if set up) has moved to Done.

---

### Part E — Reflect on the Record

Go to the now-closed issue in GitHub. Read through the full thread from creation to close.

**Checkpoint:** The issue thread tells the complete story of the work — assignment, progress, review, and resolution — without needing any external explanation.

---

### Reflection Questions

1. When your classmate used Perplexity to get a project overview, what did it get right? What context was missing that you would have included in a manual onboarding?
2. As the reviewer, what did reading the diff tell you that you wouldn't have known from the issue alone?
3. Look at the closed issue thread end-to-end. If someone who wasn't involved read it six months from now, what would they understand? What would still be unclear?

---

## Wrap-Up

Collaboration is where structure proves its value. Every convention built across Parts 1 and 2 — labels, milestones, verb-noun titles, closing keywords, PR templates — exists to make shared work legible without requiring constant coordination.

When conventions hold, a collaborator can join a project mid-stream, understand its state in minutes, pick up an issue, and contribute without friction. When they don't, every new contributor becomes a source of entropy.

Part 3 ends here. In **Part 4: Reporting and Reflection**, the focus shifts from doing to understanding. Chapter 10 covers how to use GitHub's data — issue history, PR records, milestone completion rates — to track progress, report on outcomes, and learn from how the project actually went.

---

**Next:** [Chapter 10 — Tracking Progress and Reporting](../10-tracking/README.md)
