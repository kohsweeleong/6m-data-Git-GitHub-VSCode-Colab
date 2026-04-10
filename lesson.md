# Version Control Made Simple: Git, GitHub & VS Code

**Duration:** 1.5 Hours (90 minutes)

**Format:** 30% Concepts / 70% Hands-on Practice

**Goal:** Help non-technical learners confidently save, track, and share their work using Git, GitHub, and VS Code.

Watch before class: [Git & GitHub Zero to Hero](https://youtu.be/1I79WAZ4uSU) *(15 mins)*

---

## 🎯 Learning Objectives

By the end of this session, you will be able to:

1. Explain what Git and GitHub are — and why they matter
2. Describe the difference between "local" (your computer) and "remote" (GitHub)
3. Use the essential Git actions: Stage → Commit → Push → Pull
4. Connect VS Code to GitHub and keep your work in sync
5. *(Optional)* Explain what Google Colab is and how it connects to GitHub

---

## 🕒 Session Agenda

| Time | Activity | Type |
|------|----------|------|
| **0:00 – 0:15** | Module 1: What is Git & GitHub? | Concepts (15 min) |
| **0:15 – 0:30** | Module 2: Local vs. Remote | Concepts + Demo (15 min) |
| **0:30 – 0:55** | Exercise A: Your First Repository & Commit | Hands-on (25 min) |
| **0:55 – 1:20** | Exercise B: Make Changes & Stay in Sync | Hands-on (25 min) |
| **1:20 – 1:30** | Module 3: What is Colab? + Wrap Up | Concepts (10 min) |

---

## 📘 Module 1: What is Git & GitHub? (15 mins)

### The Problem Git Solves

Imagine you are writing an important report. You save it as `Report_Final.docx`. Then you make more changes: `Report_Final_v2.docx`. Then `Report_Final_REAL_v3.docx`. Sound familiar?

This is confusing, takes up space, and makes it hard to know which version is the "real" one.

**Git** solves this by acting like a **time machine** for your files. Every time you tell it to, Git takes a *snapshot* of your work. You can label each snapshot with a description, and jump back to any snapshot at any time — without creating dozens of copies.

### Git vs. GitHub — What's the Difference?

Think of it this way:

> **Git** is the camera that takes the snapshots.  
> **GitHub** is the photo album in the cloud where you store and share them.

| | Git | GitHub |
|---|---|---|
| What is it? | Software installed on your computer | A website (github.com) |
| What does it do? | Tracks changes to your files | Stores and shares those changes online |
| Do you need the internet? | No | Yes |

You use Git *locally* (on your computer), and GitHub *remotely* (in the cloud).

### Why Does This Matter?

- **Backup:** Your work is safely stored on GitHub, even if your laptop breaks.
- **History:** You can always go back to an earlier version.
- **Sharing:** Anyone with the link can view (or contribute to) your work.
- **Collaboration:** Multiple people can work on the same project without overwriting each other.

### Key Terms to Know

| Term | Plain English |
|------|--------------|
| **Repository (Repo)** | A project folder that Git is tracking |
| **Commit** | A saved snapshot with a label describing what changed |
| **Push** | Sending your snapshots from your computer up to GitHub |
| **Pull** | Downloading the latest snapshots from GitHub to your computer |

---

## 📘 Module 2: Local vs. Remote (15 mins)

### Two Places Your Work Lives

When you use Git and GitHub, your project exists in two places:

```
Your Computer (Local)          GitHub (Remote)
┌─────────────────────┐       ┌─────────────────────┐
│  Working Files      │       │                     │
│  (what you edit)    │ ─────►│  GitHub Repository  │
│                     │ Push  │  (the cloud copy)   │
│  Commit History     │◄───── │                     │
│  (your snapshots)   │ Pull  └─────────────────────┘
└─────────────────────┘
```

- **Local** = the files on your laptop in VS Code. This is where you do your work.
- **Remote** = the copy stored on GitHub. This is the shared, backed-up version.

### The Three-Zone Mental Model (Inside VS Code)

When you make a change in VS Code, it goes through three stages before reaching GitHub:

```
[1] Working Files  →  [2] Staging Area  →  [3] Local Commit  →  GitHub
 (you edited it)      (you selected it)     (you saved it)      (you shared it)
```

1. **Working Files** — You make changes (type, edit, delete).
2. **Staging Area** — You choose *which* changes to include in the next snapshot (clicking the `+` in VS Code).
3. **Commit** — You take the snapshot and write a label describing what you did.
4. **Push** — You send the snapshot up to GitHub.

> **Analogy:** Think of it like packing a suitcase. You lay out clothes (Working Files), choose what to pack (Staging), zip up the suitcase (Commit), then check it in at the airport (Push).

### Demo: Cloning a Repository

*The instructor will demonstrate cloning this repo to show how a remote repository becomes a local one.*

1. Go to a GitHub repository page
2. Click the green **Code** button → copy the HTTPS URL
3. Open VS Code → `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) → type **Git: Clone**
4. Paste the URL → choose a folder on your computer → click **Open**

Now the project is on your computer. You can edit it locally, then push changes back to GitHub.

---

## 💻 Exercise A: Your First Repository & Commit (25 mins)

*Goal: Create a GitHub repository and make your first commit using VS Code.*

### Step 1 — Create a Repository on GitHub

1. Go to [github.com](https://github.com) and log in.
2. Click the **+** icon (top right) → **New repository**.
3. Fill in:
   - **Repository name:** `my-learning-journal`
   - **Description:** `My notes from the Git & GitHub session`
   - **Visibility:** Public
   - **Check the box:** ✅ Add a README file
4. Click **Create repository**.

✅ You now have a repository on GitHub! Notice the `README.md` file that was created automatically.

### Step 2 — Clone It to Your Computer

1. On your new GitHub repository page, click the green **Code** button.
2. Make sure **HTTPS** is selected. Copy the URL (it looks like `https://github.com/yourname/my-learning-journal.git`).
3. Open **VS Code**.
   - *Windows users:* Click the blue "Open a Remote Window" button at the bottom-left, then connect to WSL if prompted.
4. Press `Ctrl+Shift+P` (Windows) or `Cmd+Shift+P` (Mac) to open the Command Palette.
5. Type **Git: Clone** and select it.
6. Paste the URL you copied.
7. Choose a folder on your computer (e.g., your Documents folder).
8. When prompted, click **Open Repository**.

✅ Your repository is now on your computer and open in VS Code!

### Step 3 — Create Your First File

1. In VS Code's left sidebar (Explorer), right-click in the empty space → **New File**.
2. Name the file `notes.txt`.
3. Type something inside — for example:
   ```
   Day 1: Git is like a time machine for files.
   GitHub is where those snapshots live in the cloud.
   ```
4. Save the file: `Ctrl+S` (Windows) or `Cmd+S` (Mac).

### Step 4 — Stage, Commit & Push

1. Click the **Source Control** icon in the left sidebar (it looks like a branching diagram, or press `Ctrl+Shift+G`).
2. You'll see `notes.txt` listed under **Changes**.
3. **Stage:** Hover over `notes.txt` and click the **+** button. It moves to **Staged Changes**.
4. **Commit:** Type a message in the box at the top, for example: `Add my first notes`. Then click the **✔ Commit** button (or press `Ctrl+Enter`).
5. **Push:** Click the **Sync Changes** button (or the cloud icon at the bottom of the screen).

✅ Go to your GitHub repository and refresh the page — you should see `notes.txt` there!

---

## 💻 Exercise B: Make Changes & Stay in Sync (25 mins)

*Goal: Edit your file, commit the change, and practice pulling updates from GitHub.*

### Part 1 — Edit a File and Push Again

1. Open `notes.txt` in VS Code.
2. Add a new line:
   ```
   Day 2: Stage → Commit → Push is the core workflow!
   ```
3. Save the file.
4. Go to **Source Control**, stage the change (**+**), commit with a message like `Add Day 2 notes`, and then push (Sync Changes).

✅ Check GitHub — your new line should be there.

### Part 2 — Edit Directly on GitHub (Simulating a Teammate's Change)

Sometimes a colleague (or your future self on another computer) will make a change on GitHub directly. Let's simulate that:

1. Go to your GitHub repository.
2. Click on `README.md`.
3. Click the **pencil icon** ✏️ (Edit this file) at the top right.
4. Add a line at the bottom:
   ```
   Updated from GitHub directly!
   ```
5. Scroll down and click **Commit changes** → then **Commit changes** again in the dialog.

✅ Now GitHub has a newer version than your local copy.

### Part 3 — Pull the Changes to Your Computer

1. Go back to VS Code.
2. Click the **Sync Changes** button at the bottom (or `Ctrl+Shift+P` → **Git: Pull**).
3. Open `README.md` in VS Code — you should see the line you added on GitHub.

✅ Your local copy is now up to date. This is the **Pull** action — bringing the latest from GitHub to your computer.

### The Golden Rule

> **Always Pull before you Push.** When you work with others (or across multiple computers), always pull the latest changes before making your own. This avoids conflicts.

---

## 📘 Module 3: What is Google Colab? (10 mins) — Optional

### Overview

**Google Colab** (short for Colaboratory) is a free tool from Google that lets you write and run Python code in your browser — no installation needed.

Think of it as a notebook where each "cell" can contain either text or runnable code. It's widely used in data science because:

- **No setup required** — just open your browser and start coding
- **Free computing power** — Google provides free access to fast processors (GPUs)
- **Easy sharing** — share a link like a Google Doc
- **Connects to GitHub** — you can save your Colab notebooks directly to your GitHub repository

### How Colab Connects to GitHub

You can save a Colab notebook to GitHub in two clicks:

1. In Colab: **File** → **Save a copy in GitHub**
2. Choose your repository and branch, write a commit message, click **OK**

Your notebook (`.ipynb` file) will appear in your GitHub repository — just like any other file.

### Try It (If Time Allows)

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **New Notebook**
3. In the first cell, type:
   ```python
   print("Hello from Colab!")
   ```
4. Run it with **Shift + Enter**
5. Go to **File** → **Save a copy in GitHub** → select `my-learning-journal` → write a commit message → click **OK**
6. Refresh your GitHub repository — the `.ipynb` file should be there!

---

## 🎓 Wrap Up & Key Takeaways (included in Module 3 time)

You've covered the complete beginner workflow for Git and GitHub!

**What you learned:**

- **Git** tracks changes to your files like a time machine
- **GitHub** stores those changes in the cloud
- **Local** = your computer; **Remote** = GitHub
- The core workflow: **Stage → Commit → Push**
- To get the latest from GitHub: **Pull**
- **VS Code** makes all of this accessible without needing to memorise commands

**What to do next:**

- Use this workflow for your next project — even a simple one
- The more you practise, the more natural it feels
- Reference the `git_command_cheatsheet.md` whenever you need a reminder

> "The best way to learn Git is to use it. Start with one file, one commit, one push. You've already done that today." 🎉
