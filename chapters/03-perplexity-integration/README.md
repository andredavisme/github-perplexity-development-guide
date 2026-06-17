# Chapter 3 — Connecting Perplexity to GitHub

[← Table of Contents](../../README.md)

---

## Tell

### What This Chapter Covers

In the previous two chapters, you built a GitHub repository and configured it with labels, milestones, issue templates, and a project board. That structure is now readable — not just by you, but by Perplexity.

This chapter covers how to establish and use the connection between Perplexity and GitHub, so that the work you've organized can be acted on directly through conversation. You'll learn:

- What the GitHub MCP integration is and how it works
- How to connect your GitHub account to Perplexity
- How to verify the connection is working
- How to orient Perplexity to your specific project at the start of a session
- Best practices for making AI-assisted work as efficient as possible

### What Is MCP?

MCP stands for **Model Context Protocol** — a standardized way for AI assistants like Perplexity to connect to external tools and services. Think of it as a translator that allows Perplexity to speak GitHub's language: reading repositories, creating issues, updating files, and more — all without you leaving the conversation.

When the GitHub MCP integration is active, Perplexity doesn't just *know about* GitHub — it can *act on* your GitHub account in real time.

### What Perplexity Can Do via MCP

| Capability | Examples |
|---|---|
| **Read** | List repos, fetch file contents, view issues and PRs |
| **Create** | New repos, issues, branches, files, pull requests |
| **Update** | Issue titles, labels, assignees, state (open/closed), comments |
| **Search** | Issues by label or state, code across repos, commits |
| **Review** | Add PR review comments, approve or request changes |

### What Perplexity Cannot Do via MCP

| Limitation | Workaround |
|---|---|
| Create or update **GitHub Project boards** | Create manually once; Perplexity manages the underlying issues |
| Move cards between **board columns** | Use GitHub's built-in automation (close issue → move to Done) |
| Manage **GitHub Actions** workflows | Configure workflows manually in the GitHub UI |

Understanding these boundaries upfront prevents confusion and helps you design a workflow that plays to Perplexity's strengths.

### The Session Context Problem

Perplexity doesn't automatically know which of your repositories you're working on, what your labels mean, or what milestone you're targeting. At the start of every session, a small amount of context-setting goes a long way.

Think of it like briefing a collaborator who is highly capable but needs to be caught up on where things stand. The more precisely you brief them, the less time you spend on clarifying questions.

### Key Terms

| Term | Definition |
|---|---|
| **MCP (Model Context Protocol)** | A protocol that allows AI assistants to connect to and act on external services |
| **MCP Integration** | The active connection between Perplexity and a specific service (e.g., GitHub) |
| **Session Context** | The project-specific information you give Perplexity at the start of a conversation |
| **Repo Reference** | Specifying `owner/repo-name` so Perplexity knows exactly which repository to act on |

### After This Chapter You Will Be Able To
- Connect your GitHub account to Perplexity via MCP
- Verify the connection by asking Perplexity to list your repositories
- Orient Perplexity to a specific project using a session context prompt
- Ask Perplexity to read a file from your repository

---

## Show

### Demonstration: How This Book Was Built

Every chapter of this guide was written by having a conversation with Perplexity. Here is what that process looked like in practice — and what made it work.

#### Step 1: The Connection Was Already Active

Before any work began, the GitHub MCP integration was connected to the account `andredavisme`. This is a one-time setup done through Perplexity's settings. Once connected, every conversation has access to that account's repositories.

#### Step 2: Context Was Established in the First Message

The opening conversation didn't start with "write me a textbook." It started with a discussion of goals, audience, structure, and approach — building shared understanding before any action was taken. By the time the first file was created, Perplexity understood:

- The repo name: `github-perplexity-development-guide`
- The owner: `andredavisme`
- The purpose: an educational textbook using Tell/Show/Do structure
- The audience: developers, learners, and non-technical readers
- The running example: the guide's own repository

#### Step 3: Actions Were Taken Directly

With context established, instructions like *"create the repo"* and *"push the full scaffold"* were executed without needing to specify every detail. Perplexity referenced the repo by name, used the agreed structure, and confirmed each action.

#### Step 4: Sessions Were Resumed Efficiently

In longer projects, sessions don't always continue in one sitting. A good session opener looks like this:

> *"We're working on `andredavisme/github-perplexity-development-guide`. The last thing we completed was Chapter 2. Labels are: `feature`, `task`, `bug`, `question`. Active milestone: Part 1: Foundations. Let's write Chapter 3."*

This single paragraph gives Perplexity everything it needs to pick up exactly where you left off.

#### What to Notice

- The repo reference (`owner/repo-name`) is always explicit
- Labels and milestones are named, not described
- The current state is stated, not assumed
- The next action is clear

---

## Do — Lab 3.1

### Connect and Verify

**Objective:** Connect your GitHub account to Perplexity, verify the connection, and practice orienting Perplexity to your project.

**What you need before starting:**
- A Perplexity account
- Your GitHub repository from Labs 1.1 and 2.1

---

### Part A — Connect GitHub to Perplexity

1. Open [perplexity.ai](https://www.perplexity.ai)
2. Navigate to **Settings**
3. Find the **Integrations** or **Connected Apps** section
4. Locate **GitHub** and click **Connect**
5. Authorize Perplexity to access your GitHub account when prompted

**Checkpoint:** GitHub appears as a connected integration in your Perplexity settings.

---

### Part B — Verify the Connection

Start a new Perplexity conversation and type:

> *"List my GitHub repositories."*

Perplexity should return a list of your repositories. If it does, the connection is working.

**Checkpoint:** Perplexity lists at least one repository you recognize.

> **Troubleshooting:** If Perplexity says it can't access GitHub, return to Settings and confirm the integration is active. You may need to re-authorize.

---

### Part C — Read a File from Your Repo

Now ask Perplexity to fetch something specific:

> *"Show me the README.md from my `your-repo-name` repository."*

Replace `your-repo-name` with your actual repo name.

**Checkpoint:** Perplexity returns the contents of your README file.

---

### Part D — Write Your Session Context Prompt

Create a short paragraph you can paste at the start of any future session to orient Perplexity to your project. Use this template:

```
We're working on [owner/repo-name].
The project is: [one sentence description].
Labels in use: feature, task, bug, question, in-progress, needs-review, blocked.
Active milestone: [milestone name].
Last completed: [what was done most recently].
Next: [what you want to work on today].
```

Fill this in for your own project and save it somewhere easy to find — a note, a README comment, or even as a pinned issue in your repo.

**Checkpoint:** You have a completed session context prompt for your project.

---

### Reflection Questions

1. What happened when Perplexity listed your repositories? Did anything surprise you about what it could see?
2. How would your workflow change if you had to re-explain your entire project from scratch at the start of every session? What does that tell you about the value of the context prompt?
3. Are there things about your project that are hard to capture in a short paragraph? How might you handle those?

---

## Wrap-Up

Perplexity is now connected to your GitHub account and oriented to your project. The setup phase is complete.

You have a repository, a shared vocabulary of labels and milestones, issue templates that enforce consistency, a project board that reflects progress, and an AI collaborator that can act on all of it.

From here, the work begins. In **Chapter 4**, you'll use Perplexity to break your project down into a structured list of issues — transforming a vague idea or a long to-do list into a set of clear, actionable, trackable units of work.

This is where planning becomes execution.

---

**Next:** [Chapter 4 — Breaking Projects into Issues](../04-issues/README.md)
