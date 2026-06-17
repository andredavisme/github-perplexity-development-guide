# Chapter 1 — Introduction: Why GitHub + Perplexity?

---

## Tell

### What This Chapter Covers

Before writing a single line of code or opening a single issue, it's worth understanding *why* this workflow exists and what problem it solves.

Most projects — software or otherwise — don't fail because of a lack of ideas. They fail because:
- Work isn't broken into manageable pieces
- Progress isn't visible to collaborators (or to yourself, a week later)
- Context gets lost between sessions
- There's no shared language between contributors

**GitHub** solves the visibility and collaboration problem. It gives every piece of work a home: a repo, an issue, a pull request, a comment thread. Work becomes trackable, reviewable, and permanent.

**Perplexity** (with GitHub MCP integration) solves the *planning and execution* problem. Instead of switching between tools, writing boilerplate, or remembering exact syntax, you can describe what you need in plain language and Perplexity acts directly on your GitHub account — creating issues, updating records, fetching files, and more.

Together, they form a loop:

```
Idea → Perplexity plans → GitHub records → Perplexity executes → GitHub preserves
```

### Key Terms

| Term | Definition |
|---|---|
| **Repository (repo)** | A GitHub project folder containing all files, history, and discussion for a project |
| **Issue** | A trackable unit of work: a task, feature, bug, or question |
| **MCP Integration** | A connection that lets Perplexity read and write to your GitHub account directly |
| **Project Board** | A visual kanban/table/roadmap view that organizes issues by status |
| **Label** | A tag applied to an issue for filtering and categorization |

### After This Chapter You Will Be Able To
- Explain why structured project management matters for any project
- Describe the role GitHub and Perplexity each play in the workflow
- Identify the key components of a GitHub repository

---

## Show

### Demonstration: This Book as a Live Example

The repo you are reading right now — `github-perplexity-development-guide` — was created live as the first act of this textbook. Here is exactly what happened:

1. A conversation with Perplexity established the goals, structure, and audience for this guide
2. Perplexity created the repository directly via GitHub MCP integration
3. All chapter stubs, templates, and issue templates were pushed in a single structured commit
4. The result is a real, navigable GitHub repository that *is* the running example

This means you can browse the commit history, read the issues, and follow along with every decision made during the book's own development — all in the same place you're reading this text.

**What to notice:**
- The repo has a clear, descriptive name
- The README serves as the textbook's home page and table of contents
- The folder structure separates chapters, templates, and GitHub configuration
- Everything is readable by both humans and Perplexity

---

## Do — Lab 1.1

### Your First Repository

**Objective:** Create a GitHub repository for a project you want to work on. This repo will be your running example throughout the rest of the book.

**What you need before starting:**
- A GitHub account
- A project idea (can be simple — a personal site, a tool, a game, a writing project)

**Steps:**

1. Go to [github.com](https://github.com) and click **New repository**
2. Name it something descriptive and lowercase with hyphens (e.g., `my-portfolio-site`)
3. Add a short description (1–2 sentences about what it is)
4. Check **Add a README file**
5. Click **Create repository**

**Checkpoint:** You should now have a repo at `https://github.com/YOUR-USERNAME/your-repo-name` with a single `README.md` file.

**Reflection question:** What would someone need to know about your project if they found this repo for the first time?

---

## Wrap-Up

You now understand *why* this workflow exists and have a GitHub home for your project. A repo isn't just a file storage system — it's a living record of decisions, work, and progress.

In **Chapter 2**, we'll configure that repo properly: setting up labels, milestones, and the issue templates that give your project a shared language.
