# Chapter 2 — Setting Up Your GitHub Repository

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

A GitHub repository is more than a place to store files. When configured thoughtfully, it becomes a **shared workspace** — one where every contributor, human or AI, understands the conventions, speaks the same language, and can navigate work without needing to ask basic questions.

This chapter covers the one-time setup that turns a blank repository into a structured project environment. You'll configure:

- **Labels** — tags that categorize issues by type, status, or priority
- **Milestones** — groupings that tie issues to a phase, deadline, or goal
- **Issue Templates** — forms that ensure every issue follows a consistent format
- **A Project Board** — a visual overview of where all work stands

Done once, this setup pays dividends for the entire life of the project. It's also what allows Perplexity to work efficiently on your behalf — consistent structure means fewer clarifying questions and faster execution.

### Why Structure Matters Before Work Begins

Imagine inheriting a filing cabinet with no labels on the folders, no consistent naming, and papers stuffed in wherever there was space. You could probably find things — eventually — but every search would cost time and mental energy.

A well-configured GitHub repo is the opposite of that cabinet. Labels tell you *what kind* of work an issue represents. Milestones tell you *when* it belongs. Templates ensure every issue arrives with the same essential information. The project board shows you the whole picture at a glance.

This structure isn't bureaucracy. It's the scaffolding that lets creative, complex work happen without getting buried.

### Key Terms

| Term | Definition |
|---|---|
| **Label** | A colored tag applied to an issue. Used for filtering, searching, and categorizing work. |
| **Milestone** | A named checkpoint (e.g., "v1.0" or "Phase 1") that groups related issues together. |
| **Issue Template** | A pre-formatted form that appears when a new issue is created. Ensures consistent structure. |
| **Project Board** | A GitHub Projects view (kanban, table, or roadmap) that visualizes issue status. |
| **Default Branch** | The primary branch of a repo (usually `main`). The stable, canonical version of the project. |

### After This Chapter You Will Be Able To
- Create and apply a standard set of labels to a repository
- Create milestones that map to project phases or goals
- Install issue templates so new issues are consistently structured
- Create a GitHub Project board and link it to your repository

---

## Show

### Demonstration: Configuring the Guide's Own Repository

The `github-perplexity-development-guide` repository was configured with this exact setup. Here's what was done and why.

#### Labels

Labels were established to match the four issue types used throughout this book:

| Label | Color | Purpose |
|---|---|---|
| `feature` | Green | A new capability or deliverable |
| `task` | Blue | A discrete, actionable work item |
| `bug` | Red | Something broken or incorrect |
| `question` | Yellow | A discussion point or clarification needed |

Additional status labels worth adding as a project grows:

| Label | Purpose |
|---|---|
| `in-progress` | Work has started |
| `needs-review` | Ready for a collaborator to look at |
| `blocked` | Waiting on something external |
| `wont-fix` | Acknowledged but intentionally not addressed |

**How to create labels:**
1. Go to your repository on GitHub
2. Click the **Issues** tab
3. Click **Labels** (top right of the issues list)
4. Click **New label**, enter a name, choose a color, and save

#### Milestones

For this guide, milestones map to the four parts of the book:

| Milestone | Description |
|---|---|
| `Part 1: Foundations` | Chapters 1–3 — Setup and orientation |
| `Part 2: Planning With AI` | Chapters 4–6 — Issue creation and organization |
| `Part 3: Building and Collaborating` | Chapters 7–9 — Active project management |
| `Part 4: Preservation and Review` | Chapters 10–12 — Documentation and closing |

**How to create milestones:**
1. Go to the **Issues** tab
2. Click **Milestones** (top right)
3. Click **New milestone**, add a title and optional due date

#### Issue Templates

The four issue templates (`feature`, `task`, `bug`, `question`) were pre-loaded into this repo during initial setup. They live in `.github/ISSUE_TEMPLATE/` and appear automatically as a menu when anyone clicks **New Issue**.

This means every issue created in this repo — whether by a human or by Perplexity — starts with the right fields already present.

#### Project Board

The project board for this guide uses a simple kanban layout with four columns:

| Column | Meaning |
|---|---|
| **Backlog** | Issues that exist but aren't being worked on yet |
| **In Progress** | Issues actively being worked on |
| **In Review** | Issues that are complete but awaiting verification |
| **Done** | Closed and verified issues |

GitHub's built-in automation can move issues to **Done** automatically when they are closed — reducing manual board maintenance.

> **Note:** GitHub Project boards must be created manually through the GitHub UI. Once created and linked to your repository, Perplexity can manage the underlying issues — and the board reflects that progress automatically.

**How to create a Project board:**
1. Go to your GitHub profile or organization
2. Click the **Projects** tab
3. Click **New project**
4. Choose **Board** (kanban) layout
5. Name it and click **Create**
6. In the project settings, link it to your repository
7. Enable automation: *When issue is closed → move to Done*

---

## Do — Lab 2.1

### Configure Your Repository

**Objective:** Apply the standard label set, create at least one milestone, and create a Project board for the repository you started in Chapter 1.

**What you need before starting:**
- Your repository from Lab 1.1
- A rough sense of your project's phases or goals (even just "Phase 1" and "Phase 2" is enough)

---

### Part A — Labels

1. Go to your repo → **Issues** → **Labels**
2. Delete any default labels you won't use (optional but keeps things clean)
3. Create the following labels:

| Label | Suggested Color |
|---|---|
| `feature` | `#0e8a16` (green) |
| `task` | `#0075ca` (blue) |
| `bug` | `#d73a4a` (red) |
| `question` | `#e4e669` (yellow) |
| `in-progress` | `#f9d0c4` (light orange) |
| `needs-review` | `#c5def5` (light blue) |
| `blocked` | `#b60205` (dark red) |

**Checkpoint:** Your Labels page should show at least the four core labels (`feature`, `task`, `bug`, `question`).

---

### Part B — Milestones

1. Go to your repo → **Issues** → **Milestones**
2. Create at least two milestones that reflect meaningful phases of your project
3. Add a short description to each

**Example milestones for a personal portfolio site:**
- `v1.0 — Core Pages` — Home, About, Contact pages live
- `v1.1 — Projects Section` — Portfolio work added and styled

**Checkpoint:** You have at least one milestone with a description.

---

### Part C — Project Board

1. Go to your GitHub profile → **Projects** → **New project**
2. Select **Board** layout
3. Name it after your project
4. Add four columns: `Backlog`, `In Progress`, `In Review`, `Done`
5. In project settings, link it to your repository
6. Enable the automation: *When issue closed → move to Done*

**Checkpoint:** Your project board exists, has four columns, and is linked to your repo.

---

### Reflection Questions

1. What phases or milestones make sense for your specific project? How did you decide where one phase ends and another begins?
2. Are there label types you'd add beyond the standard set? What does that tell you about your project's nature?
3. Who else might use this repo? What would they need to know to understand the label and milestone system you just created?

---

## Wrap-Up

Your repository is no longer just a folder — it's a structured workspace with a shared vocabulary. Labels categorize work. Milestones organize it into phases. Issue templates ensure consistency. The project board makes everything visible at a glance.

This setup is what allows the next step to happen smoothly: in **Chapter 3**, you'll connect Perplexity to your GitHub account and verify that it can read and act on the structure you just built. When Perplexity sees labels like `feature` and milestones like `v1.0`, it can work within your system — not around it.

The structure you built today is the foundation everything else stands on.

---

**Next:** [Chapter 3 — Connecting Perplexity to GitHub](../03-perplexity-integration/README.md)
