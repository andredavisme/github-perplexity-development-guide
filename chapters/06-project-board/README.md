# Chapter 6 — Creating Your Project Board

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

At this point in the book, your project has a repository, a vocabulary of labels and milestones, and a structured backlog of issues. All of that information exists — but it's scattered across individual issue pages and filter views. The **project board** brings it together into a single, scannable surface.

A project board doesn't add new information to your project. It *surfaces* the information you've already organized, arranging it so the current state of your work is visible at a glance — to you, to collaborators, and to anyone reviewing the project for the first time.

This chapter covers:
- What GitHub Projects v2 is and how it differs from older GitHub boards
- The three board views and when each is most useful
- How to create a project board and configure it for your workflow
- How to link issues to the board and set up automation
- How the board and Perplexity work together — and where the boundary is

### GitHub Projects v2

GitHub offers two generations of project boards. This book uses **Projects v2**, the current generation, which is more powerful and flexible than the original.

| Feature | Projects v1 (Classic) | Projects v2 (Current) |
|---|---|---|
| Layout options | Kanban only | Board, Table, Roadmap |
| Custom fields | No | Yes (text, number, date, select) |
| Automation | Basic | Advanced, including GitHub Actions |
| Cross-repo support | No | Yes |
| Filter and group by | Limited | Extensive |

If you see a board in your GitHub account that looks like a simple kanban with notes cards, that's v1. Projects v2 boards live under your profile or organization's **Projects** tab.

### The Three Views

A single Projects v2 board can display your work in three different ways. You can switch between them anytime — the underlying data is the same, only the presentation changes.

| View | Best For | Looks Like |
|---|---|---|
| **Board** | Day-to-day status tracking | Kanban columns (Backlog, In Progress, Done) |
| **Table** | Bulk editing, sorting, filtering | Spreadsheet rows with custom columns |
| **Roadmap** | Timeline and sequencing | Horizontal Gantt-style bars |

For most projects in this book, the **Board view** is the primary view. It answers the most common question: *"What's being worked on right now?"*

### Anatomy of a Board

A well-configured board has:

- **Columns** that map to the stages of your workflow
- **Cards** that represent individual issues
- **Automation** that moves cards when issue state changes
- **Filters** that let you focus on a subset (by label, milestone, assignee)

The four-column structure used throughout this book:

| Column | What Belongs Here |
|---|---|
| **Backlog** | Issues that exist but aren't being actively worked on |
| **In Progress** | Issues currently being worked on |
| **In Review** | Work complete, awaiting verification or feedback |
| **Done** | Closed and verified issues |

### The MCP Boundary

This is an important constraint to understand clearly:

> **Perplexity cannot create, update, or move items on a GitHub Project board.** Project boards use GitHub's GraphQL API (Projects v2), which is not accessible through the MCP tools available in this workflow.

What this means in practice:
- The board must be **created manually** (once)
- Issues must be **added to the board manually** (or via GitHub automation)
- **Card movement** is handled by GitHub's built-in automation, not Perplexity

What Perplexity *can* do is manage the underlying issues — updating labels, closing issues, adding comments — and the board reflects those changes automatically through automation.

This is not a significant limitation once you understand it. The board is a *mirror* of issue state, not a separate system to maintain.

### Key Terms

| Term | Definition |
|---|---|
| **Projects v2** | The current generation of GitHub's project management boards, supporting multiple views and custom fields |
| **Board view** | A kanban-style column layout showing issues grouped by status |
| **Table view** | A spreadsheet-style layout for bulk editing and filtering |
| **Roadmap view** | A timeline layout for sequencing work over time |
| **Card** | The representation of an issue on a project board |
| **Automation** | Rules that move cards automatically when issue state changes |
| **GraphQL API** | The programming interface GitHub uses for Projects v2, distinct from the REST API used by MCP tools |

### After This Chapter You Will Be Able To
- Create a GitHub Projects v2 board
- Configure columns that reflect your workflow stages
- Link your repository's issues to the board
- Set up automation so cards move when issues are closed
- Explain the boundary between what Perplexity manages and what the board handles automatically

---

## Show

### Demonstration: The Guide's Project Board

Here is exactly how a project board for `github-perplexity-development-guide` would be configured — and the reasoning behind each decision.

#### Creating the Board

1. Go to `https://github.com/andredavisme` (the profile page)
2. Click the **Projects** tab
3. Click **New project**
4. Select **Board** as the template
5. Name it: `GitHub + Perplexity Development Guide`
6. Click **Create project**

At this point you have a blank board with default columns. The next step is shaping it.

#### Configuring Columns

Delete the default columns and create four new ones:

| Column Name | Purpose |
|---|---|
| `Backlog` | All chapter stubs and planned issues not yet started |
| `In Progress` | The chapter currently being written |
| `In Review` | Chapters drafted and ready for a read-through |
| `Done` | Completed and merged chapters |

> **Why four columns and not three?** The `In Review` column creates a visible handoff point — a clear signal that work is complete but not yet verified. Without it, "done" gets used prematurely and quality review gets skipped.

#### Linking the Repository

1. In the project, click the **⋮** menu (top right) → **Settings**
2. Scroll to **Repositories**
3. Click **Add repository** and select `github-perplexity-development-guide`

Now issues from that repo can be added to the board.

#### Adding Issues to the Board

1. In the board, click **+ Add item** at the bottom of the Backlog column
2. Type `#` to search for issues by number or title
3. Select each issue and it appears as a card

Repeat for all open issues. They all start in **Backlog**.

#### Setting Up Automation

1. Click the **⋮** menu on the **Done** column
2. Select **Set column automation**
3. Enable: *When an issue is closed → move to this column*

Now, whenever Perplexity (or anyone) closes an issue, it automatically moves to Done on the board — no manual card dragging required.

#### The Result

The board now reflects the live state of the project. As chapters are written and issues are closed by Perplexity, cards migrate from Backlog → In Progress → In Review → Done automatically.

Perplexity manages the issues. The board manages the visualization. Neither system needs to know about the other — they connect through issue state.

---

## Do — Lab 6.1

### Create and Configure Your Project Board

**Objective:** Create a GitHub Projects v2 board for your project, link your repository, add your issues, and configure automation.

**What you need before starting:**
- Your repository with labeled, milestone-assigned issues from Labs 4 and 5
- A GitHub account (boards live at the profile level, not the repo level)

---

### Part A — Create the Board

1. Go to your GitHub profile page: `https://github.com/YOUR-USERNAME`
2. Click the **Projects** tab
3. Click **New project**
4. Select **Board**
5. Name it after your project
6. Click **Create project**

**Checkpoint:** A blank board exists under your GitHub Projects tab.

---

### Part B — Configure Columns

1. Delete any default columns you don't want
2. Create (or rename) columns to match your workflow

If you're unsure, use the four-column structure from the Show section: `Backlog`, `In Progress`, `In Review`, `Done`.

**Checkpoint:** Your board has at least three columns that map to real stages of your workflow.

---

### Part C — Link Your Repository

1. In your project, click the **⋮** menu → **Settings**
2. Find the **Repositories** section
3. Click **Add repository** and select your project repo

**Checkpoint:** Your repository appears in the project's linked repositories list.

---

### Part D — Add Issues to the Board

1. In the **Backlog** column, click **+ Add item**
2. Type `#` and select each open issue from your repository
3. Add all open issues to the board

**Checkpoint:** Every open issue from your repo appears as a card on the board, in the Backlog column.

---

### Part E — Set Up Automation

1. Click the **⋮** menu on your **Done** column
2. Select **Set column automation** (or **Workflows** depending on your GitHub version)
3. Enable the rule: *When issue is closed → move to Done*

**Test it:** Ask Perplexity to close one of your issues:
> *"Close issue #[number] in `your-username/your-repo-name` with a comment: 'Completed in Lab 6.1.'"*

Then check your board. The card should have moved to Done automatically.

**Checkpoint:** A closed issue appears in the Done column without manual intervention.

---

### Reflection Questions

1. Looking at your board, what does the distribution of cards across columns tell you about your project's current state?
2. What would the board look like if you came back to this project after a month away? What information would it give you immediately?
3. The board and Perplexity operate on the same data (issues) but through different interfaces. In your own words, how do they complement each other?

---

## Wrap-Up

Your project now has a complete organizational foundation: a repository, a vocabulary, a structured backlog, and a visual board that reflects the live state of all your work. Part 2 is complete.

Everything built so far has been preparation. In **Part 3: Building and Collaborating**, the work itself begins. Chapter 7 covers how to use Perplexity as an active project partner — updating issues, logging progress, responding to changes, and keeping the backlog accurate as the project evolves.

The setup is done. Now we build.

---

**Next:** [Chapter 7 — Managing Issues with Perplexity](../07-managing-issues/README.md)
