# Chapter 4 — Breaking Projects into Issues

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

A project without structure is just a list of hopes. The moment you break it into discrete, named, trackable pieces of work, it becomes something you can actually execute — and something others can join.

In GitHub, that unit of work is the **issue**. An issue is not just a bug report or a feature request. It's anything worth tracking: a task to complete, a decision to make, a question to answer, a piece of content to write. If it matters to the project, it deserves an issue.

This chapter covers:
- How to think about decomposing a project into issues
- The four issue types and when to use each
- How to write issues that are clear enough to act on
- How to use Perplexity to generate a structured issue list from a plain-language project description
- The difference between creating issues via Perplexity vs. the GitHub UI

### Why Decomposition Is a Skill

Breaking a large goal into small, actionable pieces is harder than it sounds. Most people naturally think in outcomes (*"I want a working website"*) rather than steps (*"Create the HTML structure for the homepage"*). Issues live at the step level — specific enough to start, specific enough to finish.

A well-written issue has three qualities:
1. **It has a clear owner** — someone (or something) responsible for completing it
2. **It has a clear end state** — you can tell when it's done
3. **It's small enough to complete in one session** — if it would take weeks, it should be broken into smaller issues

This last point is worth emphasizing. Large, vague issues tend to stall. Small, specific issues get done.

### The Four Issue Types

| Type | Use When | Example |
|---|---|---|
| **Feature** | You're adding a new capability or deliverable | *"Add user login page"* |
| **Task** | You have a discrete action to take | *"Update README with setup instructions"* |
| **Bug** | Something is broken or behaving incorrectly | *"Form submission fails on mobile"* |
| **Question** | You need a decision or clarification before work can proceed | *"Should the nav be fixed or static?"* |

Using the right type matters because it signals priority and approach. A bug demands urgency. A question blocks other work. A feature is additive. A task is execution.

### Verb-Noun Issue Titles

A consistent naming convention makes issues scannable and unambiguous. The standard used throughout this book:

> **[Verb] [Noun]** — *what action is being taken on what thing*

| Good | Why It Works |
|---|---|
| *"Add contact form to homepage"* | Clear action, clear target |
| *"Fix broken image on About page"* | Specific, actionable |
| *"Write Chapter 4 content"* | Unambiguous scope |
| *"Decide on color palette"* | Question/decision framed as action |

| Avoid | Why It Doesn't Work |
|---|---|
| *"Homepage"* | Not an action — just a topic |
| *"Stuff for v2"* | No scope, no action |
| *"Bug"* | No context whatsoever |
| *"Maybe add dark mode?"* | Uncertainty baked into the title |

### Key Terms

| Term | Definition |
|---|---|
| **Issue** | A trackable unit of work in GitHub. Can represent a feature, task, bug, or question. |
| **Decomposition** | The process of breaking a large goal into smaller, actionable pieces |
| **Issue Body** | The description field of an issue. Should include context, steps, and acceptance criteria. |
| **Acceptance Criteria** | The specific conditions that must be true for an issue to be considered complete |
| **Assignee** | The person (or team) responsible for completing the issue |

### After This Chapter You Will Be Able To
- Identify what belongs in an issue vs. what doesn't
- Choose the correct issue type for any unit of work
- Write issue titles using the verb-noun convention
- Ask Perplexity to generate a structured issue list from a project description
- Create issues in your repository via Perplexity

---

## Show

### Demonstration: Generating Issues for This Guide

Here is how the issues for this textbook's own development could be created using Perplexity. This is the exact kind of prompt and output that makes the workflow efficient.

#### The Prompt

> *"We're working on `andredavisme/github-perplexity-development-guide`. This is an educational textbook teaching GitHub + Perplexity workflows. Please create a set of issues for writing the remaining chapter stubs. Use the `task` label and assign them to the `Part 2: Planning With AI` milestone where appropriate. Use verb-noun titles."*

#### What Perplexity Does

1. Reads the existing repo structure to see what's already written
2. Identifies the stub chapters that need content
3. Generates issues with consistent titles, descriptions, and labels
4. Creates them directly in the repository via MCP

#### Example Issues Created

| Title | Label | Milestone |
|---|---|---|
| Write Chapter 4: Breaking Projects into Issues | `task` | Part 2: Planning With AI |
| Write Chapter 5: Labels, Milestones, and Shared Language | `task` | Part 2: Planning With AI |
| Write Chapter 6: Creating Your Project Board | `task` | Part 2: Planning With AI |

Each issue would include a body describing the chapter's scope, the Tell/Show/Do structure to follow, and a checklist of sections to complete.

#### Perplexity vs. GitHub UI: When to Use Each

| Method | Best For |
|---|---|
| **Perplexity** | Creating multiple issues at once, bulk labeling, issues derived from a plan or conversation |
| **GitHub UI** | One-off issues, issues with screenshots or attachments, issues that need careful manual formatting |

Neither is always better. Use Perplexity when speed and consistency matter. Use the UI when detail and nuance matter.

---

## Do — Lab 4.1

### Build Your Project's Issue List

**Objective:** Use Perplexity to generate and create a structured set of issues for your own project, then verify them in GitHub.

**What you need before starting:**
- Your configured repository from Labs 1–3
- A clear enough sense of your project to describe it in 2–3 sentences

---

### Part A — Describe Your Project to Perplexity

Start a new Perplexity conversation. Paste your session context prompt from Lab 3.1, then add:

> *"Here is a description of my project: [your description]. Please suggest a list of 6–10 issues that would represent the first phase of work. Use verb-noun titles. Identify the type (feature, task, bug, or question) for each. Don't create them yet — just list them so I can review."*

Review the list. Ask Perplexity to adjust any titles, add missing issues, or remove ones that don't belong.

**Checkpoint:** You have a reviewed list of 6–10 issues you're happy with.

---

### Part B — Create the Issues

Once the list looks right, tell Perplexity:

> *"Please create these issues in my repository. Apply the appropriate label to each and assign them to my [milestone name] milestone."*

Perplexity will create each issue directly in your repo.

**Checkpoint:** Go to your repository's Issues tab on GitHub. You should see the new issues with labels and milestones applied.

---

### Part C — Add One Issue Manually

Create one additional issue using the GitHub UI to experience both methods:

1. Go to your repo → **Issues** → **New issue**
2. Choose the appropriate template (feature, task, bug, or question)
3. Fill in the title using verb-noun convention
4. Complete the template fields
5. Apply a label and milestone
6. Click **Submit new issue**

**Checkpoint:** Your Issues tab now contains both Perplexity-created and manually created issues.

---

### Reflection Questions

1. Did Perplexity's suggested issues match what you had in mind? What did it get right? What did it miss?
2. Were any of your issues too large to complete in one session? How did you break them down?
3. What's the difference in *feel* between creating issues via Perplexity vs. the GitHub UI? When would you choose each?

---

## Wrap-Up

Your project now has a backlog — a set of named, labeled, milestone-assigned units of work that represent the first phase of what you're building. That backlog is visible, shareable, and actionable.

But a list of issues, even a well-structured one, can still be hard to navigate as a project grows. In **Chapter 5**, you'll go deeper into the organizational tools that keep a growing issue list legible: label taxonomies, milestone strategy, and the shared language conventions that make collaboration across contributors — human or AI — frictionless.

---

**Next:** [Chapter 5 — Labels, Milestones, and Shared Language](../05-organization/README.md)
