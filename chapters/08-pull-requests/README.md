# Chapter 8 — Pull Requests and Code Review

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

In Chapter 7, you learned how to manage issues — the units of work. This chapter introduces the mechanism GitHub uses to manage *changes*: the **pull request**.

A pull request (PR) is a proposal to merge a set of changes from one branch into another. It's where code (or content) is reviewed before it becomes part of the main project. But a PR is more than a technical handoff — it's a structured conversation about the work: what changed, why it changed, and whether it's ready.

This chapter covers:
- What a pull request is and how it relates to branches and issues
- The anatomy of a well-written PR
- How to create a PR that links to its source issue
- How to review and comment on a PR
- What happens when a PR is merged — and how it connects back to issues
- What Perplexity can do with pull requests

### Branches: The Foundation of Pull Requests

Before you can understand pull requests, you need to understand **branches**.

A branch is an independent copy of your project's files that you can change without affecting the main version. Think of it like a draft — you make your changes in the draft, and only when you're satisfied do you incorporate them into the final version.

```
main branch  ────────────────────────────────► (stable, live version)
                    └─ feature-branch ───► PR ──► merged back into main
```

The workflow is:
1. Create a branch for your work
2. Make changes on that branch
3. Open a pull request proposing to merge those changes into `main`
4. Review, discuss, revise
5. Merge — the changes become part of `main`
6. Delete the branch (it's served its purpose)

### Why Not Just Commit Directly to Main?

For solo projects, committing directly to `main` is common and often fine. Pull requests become important when:
- **Collaboration is involved** — PRs give others a chance to review before changes land
- **Quality matters** — the review step catches errors, inconsistencies, and oversights
- **History matters** — merged PRs create a clear record of what changed and why
- **The project is complex** — branching prevents incomplete work from breaking the stable version

Even on solo projects, developing the PR habit pays off when collaborators join or when you return to a project after time away.

### Anatomy of a Well-Written Pull Request

A PR without context is just a diff — a list of changes with no explanation. A well-written PR tells a story:

| Section | What It Communicates |
|---|---|
| **Title** | What changed, in verb-noun form (mirrors the issue title) |
| **What changed** | A summary of the specific modifications made |
| **Why** | The reason for the change — links to the source issue |
| **How to review** | What the reviewer should focus on |
| **Checklist** | Confirmation that standard steps were followed |

This structure is exactly what the PR template in `.github/pull_request_template.md` provides — it loads automatically whenever a new PR is opened in your repository.

### Linking PRs to Issues

GitHub recognizes special keywords in PR descriptions that automatically close the linked issue when the PR is merged:

| Keyword | Effect |
|---|---|
| `Closes #[number]` | Closes the issue when PR merges |
| `Fixes #[number]` | Same behavior |
| `Resolves #[number]` | Same behavior |

This is a powerful connection: merging the PR closes the issue, which triggers board automation, which moves the card to Done. One action completes the chain.

### The Review Process

A PR review is a structured response to proposed changes. Reviewers can:
- **Comment** — leave feedback on specific lines or the PR overall
- **Approve** — signal the changes are ready to merge
- **Request changes** — block the merge until specific concerns are addressed

Good reviews are specific, constructive, and focused on the work, not the person. A review comment like *"This function is confusing"* is less useful than *"This function does two things — consider splitting it into `validateInput()` and `formatOutput()`."*

### What Perplexity Can Do with Pull Requests

| Action | Available via Perplexity |
|---|---|
| Create a pull request | ✓ Yes |
| Update PR title or description | ✓ Yes |
| Add a comment to a PR | ✓ Yes |
| Add a review comment to a specific line | ✓ Yes |
| Approve a PR | ✓ Yes |
| Request changes on a PR | ✓ Yes |
| Merge a PR | ✓ Yes |
| List open PRs | ✓ Yes |
| Get the diff of a PR | ✓ Yes |

Perplexity has broad capability with pull requests. The main limitation is that it can only act on existing branches — it cannot run code or resolve complex merge conflicts.

### Key Terms

| Term | Definition |
|---|---|
| **Branch** | An independent line of development. Changes made on a branch don't affect other branches until merged. |
| **Pull Request (PR)** | A proposal to merge changes from one branch into another, with a structured review process. |
| **Diff** | The set of line-by-line changes between two versions of a file. What a PR shows. |
| **Merge** | The act of incorporating changes from a PR branch into the target branch (usually `main`). |
| **Review** | A structured response to a PR: comment, approve, or request changes. |
| **Closing keyword** | A phrase in a PR description (`Closes #N`) that automatically closes a linked issue when the PR merges. |
| **Merge conflict** | A situation where two branches have changed the same part of a file in incompatible ways, requiring manual resolution. |

### After This Chapter You Will Be Able To
- Explain what a branch is and why it matters
- Create a pull request that links to a source issue
- Write a PR description using the standard template
- Review a PR and leave specific, constructive comments
- Merge a PR and observe the linked issue close automatically
- Use Perplexity to create, comment on, and merge pull requests

---

## Show

### Demonstration: A PR for This Guide

Here is how a pull request would be created and merged for a chapter addition to `github-perplexity-development-guide`.

#### The Scenario

Chapter 8 content has been written on a branch called `chapter-8-content`. It's ready to be reviewed and merged into `main`.

#### Step 1: Create the Branch

Before content is written, a branch is created:

> *"Create a branch called `chapter-8-content` in `andredavisme/github-perplexity-development-guide` from `main`."*

Perplexity creates the branch via MCP.

#### Step 2: Push Changes to the Branch

Chapter 8 content is written and pushed to `chapter-8-content`:

> *"Push the Chapter 8 content to the `chapter-8-content` branch in `andredavisme/github-perplexity-development-guide`."*

#### Step 3: Open a Pull Request

> *"Open a pull request in `andredavisme/github-perplexity-development-guide` from `chapter-8-content` to `main`. Title: 'Add Chapter 8: Pull Requests and Code Review'. Description: 'Adds full Tell/Show/Do/Wrap-Up content for Chapter 8. Closes #8.'"*

Perplexity creates the PR. The `Closes #8` keyword links it to the Chapter 8 issue.

#### Step 4: Review

A collaborator (or the author reviewing their own work) opens the PR and reads through the changes. They might leave a comment:

> *"Add a review comment to PR #8 on line 45 of `chapters/08-pull-requests/README.md`: 'Consider adding an example of a merge conflict and how to resolve it — this is a common stumbling block for new contributors.'"*

#### Step 5: Respond and Update

> *"Add a comment to PR #8: 'Good call. Adding a merge conflict note to the Key Terms and a tip in the Wrap-Up.'"*

Changes are made, pushed to the same branch, and the PR updates automatically.

#### Step 6: Merge

> *"Merge PR #8 in `andredavisme/github-perplexity-development-guide` using squash merge."*

The PR merges. The `Closes #8` keyword fires, closing the Chapter 8 issue. The board card moves to Done.

#### What to Notice

- The PR title mirrors the issue title (verb-noun)
- The closing keyword connects PR and issue in one action
- Review comments are specific to lines, not general reactions
- The author acknowledges feedback and states the planned response before changing anything
- One merge action completes three things: merges the code, closes the issue, updates the board

---

## Do — Lab 8.1

### Create, Review, and Merge a Pull Request

**Objective:** Make a change to your project on a branch, open a PR, review it, and merge it — observing the linked issue close automatically.

**What you need before starting:**
- Your repository with at least one open issue
- A small change you want to make (update a README section, add a file, revise content)

---

### Part A — Create a Branch

Ask Perplexity:

> *"Create a branch called `[descriptive-branch-name]` in `your-username/your-repo-name` from `main`."*

Branch names should be lowercase, hyphenated, and descriptive: `update-readme-intro`, `add-contact-page`, `fix-broken-link`.

**Checkpoint:** The new branch appears in your repo's branch list.

---

### Part B — Make a Change on the Branch

Ask Perplexity to make a small change on your new branch:

> *"Update [file] in `your-username/your-repo-name` on the `[branch-name]` branch to [describe the change]."*

Or make the change yourself via the GitHub UI (edit a file, select your branch from the dropdown before saving).

**Checkpoint:** Your branch has at least one commit that `main` doesn't have.

---

### Part C — Open a Pull Request

> *"Open a pull request in `your-username/your-repo-name` from `[branch-name]` to `main`. Title: '[verb-noun title]'. Add 'Closes #[issue-number]' in the description."*

**Checkpoint:** A PR exists in your repo's Pull Requests tab, linked to an issue via closing keyword.

---

### Part D — Review the PR

Open the PR in the GitHub UI and read through the diff. Then either:
- Ask Perplexity to add a review comment on a specific line
- Or add a comment yourself via the GitHub UI

Approve the PR:

> *"Approve PR #[number] in `your-username/your-repo-name`."*

**Checkpoint:** The PR has at least one comment and an approval.

---

### Part E — Merge and Verify

> *"Merge PR #[number] in `your-username/your-repo-name`."*

Then check:
1. Is the change visible in `main`?
2. Is the linked issue now closed?
3. Has the board card moved to Done (if automation is set up)?

**Checkpoint:** All three are true.

---

### Reflection Questions

1. What does the PR diff show you that looking at the final file alone wouldn't?
2. How does the closing keyword change your mental model of the relationship between issues and pull requests?
3. For a solo project, when would you bother with a PR instead of committing directly to `main`? What's the threshold?

---

## Wrap-Up

Pull requests complete the change loop: a branch holds the work in progress, the PR proposes it for review, the merge makes it permanent, and the closing keyword ties it back to the issue that motivated it in the first place.

This chain — issue → branch → PR → merge → closed issue — is the fundamental unit of structured, reviewable, preservable work in GitHub.

In **Chapter 9**, you'll expand this workflow to include other people. Collaboration introduces new challenges — shared conventions, peer review, forking, and the etiquette of contributing to someone else's project — and new rewards: the perspectives, catches, and improvements that only come from a second set of eyes.

---

**Next:** [Chapter 9 — Collaboration and Shared Conventions](../09-collaboration/README.md)
