# Chapter 5 — Labels, Milestones, and Shared Language

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

A single issue is easy to understand. Twenty issues start to blur. A hundred issues without organization become a liability — technically visible, practically invisible.

Labels and milestones are the organizational layer that keeps a growing project legible. But more than that, they establish a **shared language** — a set of agreed-upon terms that every contributor, human or AI, uses to mean the same thing.

This chapter covers:
- The difference between labels and milestones, and how they work together
- Building a label taxonomy that serves your project's specific needs
- Milestone strategy: how to use them to reflect real phases of work
- Why shared language matters for collaboration and how to enforce it
- How consistent conventions make Perplexity dramatically more effective

### Labels vs. Milestones: Two Different Questions

It helps to think of labels and milestones as answering different questions:

| Tool | Question It Answers |
|---|---|
| **Label** | *What kind of thing is this?* |
| **Milestone** | *When does this belong?* |

An issue can have multiple labels but should belong to only one milestone. Labels describe the nature of the work; milestones situate it in time or phase.

Example: An issue titled *"Fix nav menu collapse on mobile"* might have labels `bug` and `in-progress`, and belong to the milestone `v1.0 — Launch`.

### Building a Label Taxonomy

A taxonomy is a classification system. A good label taxonomy is:
- **Complete** — every issue can be categorized
- **Mutually exclusive where it matters** — type labels (feature, task, bug, question) shouldn't overlap
- **Extendable** — new labels can be added without breaking the existing system
- **Meaningful at a glance** — a filtered view by label should tell a coherent story

#### The Three Label Layers

The label system used in this book has three layers:

**Layer 1 — Type** (what kind of work)

| Label | Meaning |
|---|---|
| `feature` | New capability or deliverable |
| `task` | Discrete action to take |
| `bug` | Something broken |
| `question` | Decision or clarification needed |

**Layer 2 — Status** (where it stands right now)

| Label | Meaning |
|---|---|
| `in-progress` | Actively being worked on |
| `needs-review` | Complete, awaiting verification |
| `blocked` | Waiting on something external |
| `wont-fix` | Acknowledged, intentionally skipped |

**Layer 3 — Priority** (how urgent or important)

| Label | Meaning |
|---|---|
| `priority-high` | Needs attention before other work |
| `priority-low` | Can wait, not blocking anything |
| `good-first-issue` | Appropriate for new contributors |

Not every project needs all three layers. A solo project may only need Layer 1. A collaborative project benefits from all three.

### Milestone Strategy

Milestones work best when they map to something real: a release, a phase of work, a deadline, a deliverable. Avoid creating milestones that are too vague (*"Someday"*) or too granular (*"This week"*).

#### Three Milestone Patterns

**Version-based** — best for software projects with releases
```
v1.0 — Core features live
v1.1 — Performance and polish
v2.0 — Major feature expansion
```

**Phase-based** — best for projects with distinct stages
```
Phase 1: Research and planning
Phase 2: Build
Phase 3: Test and launch
```

**Part-based** — best for educational or content projects (like this book)
```
Part 1: Foundations
Part 2: Planning With AI
Part 3: Building and Collaborating
Part 4: Preservation and Review
```

### Shared Language and Why It Compounds

The real power of a label and milestone system isn't organization — it's **communication**.

When everyone on a project uses the same terms to mean the same things, a lot of overhead disappears:
- "What's blocking you?" becomes answerable with a filter: `label:blocked`
- "What's left for launch?" becomes answerable with a filter: `milestone:v1.0 state:open`
- "What should I pick up next?" becomes answerable with: `label:task label:good-first-issue`

This is equally true for Perplexity. When you say *"create an issue with the `bug` label in the `v1.0` milestone"*, Perplexity knows exactly what you mean — because those terms are defined and consistent in your repo.

Vague instructions produce vague results. Precise vocabulary produces precise execution.

### Key Terms

| Term | Definition |
|---|---|
| **Label Taxonomy** | A structured classification system of labels for a repository |
| **Milestone** | A named phase or checkpoint that groups related issues |
| **Filter** | A GitHub Issues view restricted by label, milestone, assignee, or state |
| **Shared Language** | A set of agreed-upon terms used consistently by all contributors |
| **Layer** | A category within the label system (type, status, priority) |

### After This Chapter You Will Be Able To
- Explain the difference between labels and milestones
- Build a three-layer label taxonomy suited to your project
- Choose a milestone pattern appropriate for your project type
- Use GitHub's filter system to answer project status questions
- Give Perplexity label and milestone instructions with precision

---

## Show

### Demonstration: The Guide's Own Label and Milestone System

Here is the complete label and milestone system used in `github-perplexity-development-guide` — and the thinking behind each choice.

#### Labels in Use

This project is primarily a content project, so Layer 1 (type) does the heaviest lifting. Layer 2 (status) was added because multiple contributors may work on chapters simultaneously. Layer 3 (priority) was kept minimal.

| Label | Layer | Reasoning |
|---|---|---|
| `feature` | Type | New chapters or sections being added |
| `task` | Type | Discrete writing or editing actions |
| `bug` | Type | Errors, broken links, incorrect content |
| `question` | Type | Structural or editorial decisions |
| `in-progress` | Status | Chapter currently being written |
| `needs-review` | Status | Draft complete, needs a read-through |
| `blocked` | Status | Waiting on a decision or prior chapter |

#### Milestones in Use

The part-based pattern was chosen because the book has four clearly defined parts with sequential dependencies:

| Milestone | Issues It Contains |
|---|---|
| `Part 1: Foundations` | Chapters 1–3 |
| `Part 2: Planning With AI` | Chapters 4–6 |
| `Part 3: Building and Collaborating` | Chapters 7–9 |
| `Part 4: Preservation and Review` | Chapters 10–12 |

#### A Filtered View in Practice

To answer *"What chapter work is currently in progress?"*:

```
GitHub Issues filter:
label: in-progress
milestone: Part 2: Planning With AI
state: open
```

This returns exactly the issues being actively worked on for the current part — no noise, no scrolling.

#### The Perplexity Equivalent

> *"Show me open issues in `andredavisme/github-perplexity-development-guide` with the `in-progress` label in the Part 2 milestone."*

Same result, conversational interface.

---

## Do — Lab 5.1

### Build and Apply Your Organization System

**Objective:** Refine your label taxonomy, confirm your milestones, and apply them to the issues you created in Chapter 4.

**What you need before starting:**
- Your repository with issues from Lab 4.1
- A sense of your project's phases or release stages

---

### Part A — Audit and Extend Your Labels

1. Go to your repo → **Issues** → **Labels**
2. Review the labels you created in Lab 2.1
3. Add any Layer 2 (status) or Layer 3 (priority) labels that make sense for your project
4. Delete any labels you know you won't use

**Decide:** Which layers does your project actually need?
- Solo project, early stage → Layer 1 only
- Solo project, active build → Layers 1 + 2
- Collaborative project → All three layers

**Checkpoint:** Your label set is complete, intentional, and free of labels you don't plan to use.

---

### Part B — Confirm Your Milestones

1. Go to your repo → **Issues** → **Milestones**
2. Review the milestones you created in Lab 2.1
3. Choose a milestone pattern (version-based, phase-based, or part-based) and confirm your milestones fit it
4. Add descriptions to any milestones that don't have them

**Checkpoint:** Each milestone has a name, a description, and a clear scope.

---

### Part C — Apply Labels and Milestones to Existing Issues

Ask Perplexity to help:

> *"Review the open issues in `your-username/your-repo-name`. For any issues missing a label or milestone, suggest the appropriate label (feature, task, bug, or question) and milestone based on the issue content. Then apply them."*

Or do it manually:
1. Go to **Issues**
2. Open each issue
3. Use the right sidebar to assign labels and a milestone

**Checkpoint:** Every open issue has at least one label and belongs to a milestone.

---

### Part D — Practice Filtering

Use GitHub's Issues filter to answer these questions about your project:

1. How many open issues are tagged `feature`?
2. How many issues belong to your first milestone?
3. If you have `blocked` or `in-progress` labels applied, what does that filtered view show?

**Checkpoint:** You can answer project status questions using filters alone.

---

### Reflection Questions

1. Did you find yourself wanting labels that don't fit neatly into type, status, or priority? What does that reveal about your project's specific needs?
2. How would a new contributor to your project learn the label system? Is it self-documenting, or would they need an explanation?
3. Looking at your filtered issue views, what does the data tell you about the current state of your project?

---

## Wrap-Up

Your project now has a vocabulary. Labels describe what work is, status labels describe where it stands, and milestones describe when it belongs. Filters turn that vocabulary into instant answers.

This is the organizational foundation that makes everything else scalable. A project with 10 issues and no labels is manageable. A project with 100 issues and a clear taxonomy is *still* manageable — because the structure does the work of keeping it legible.

In **Chapter 6**, you'll take one more step: creating the Project board that makes this entire system visible at a glance. The board doesn't add new information — it surfaces the information you've already organized into a format that's immediately scannable for anyone who joins the project.

---

**Next:** [Chapter 6 — Creating Your Project Board](../06-project-board/README.md)
