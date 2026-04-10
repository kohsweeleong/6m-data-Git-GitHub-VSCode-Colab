# Git Essentials — Quick Reference

A simple, beginner-friendly reference for the commands and actions you'll use most often.

---

## The Big Picture

```
Your Computer (Local)                    GitHub (Remote)
┌────────────────────────┐              ┌───────────────┐
│ 1. Edit files in       │              │               │
│    VS Code             │   ─ Push ──► │  GitHub Repo  │
│ 2. Stage (select)      │              │  (the cloud)  │
│ 3. Commit (snapshot)   │ ◄─ Pull ──   │               │
└────────────────────────┘              └───────────────┘
```

**Stage → Commit → Push** is the core cycle you'll repeat every time.

---

## Part 1: First-Time Setup

*Do this once, before your very first commit.*

Open a terminal (Mac: Terminal app; Windows: Git Bash) and run:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Use the same email you used for GitHub.

To confirm it worked:
```bash
git config --global --list
```

---

## Part 2: Getting a Project onto Your Computer

### Option A — Clone from GitHub (Most Common)

1. Go to your GitHub repository
2. Click the green **Code** button → copy the HTTPS URL
3. In VS Code: press `Ctrl+Shift+P` (or `Cmd+Shift+P`) → type **Git: Clone** → paste URL
4. Choose where to save it on your computer

**Or in the terminal:**
```bash
git clone https://github.com/yourname/your-repo.git
```

### Option B — Start Fresh Locally

```bash
# Create a new folder and turn it into a Git repo
mkdir my-project
cd my-project
git init
```

---

## Part 3: The Daily Workflow

### Check what's changed
```bash
git status
```
*Shows which files you've changed, staged, or haven't touched yet.*

### Stage your changes

**In VS Code:** Source Control panel → click **+** next to a file

**In terminal:**
```bash
git add filename.txt        # Stage a specific file
git add .                   # Stage ALL changed files
```

### Commit (take the snapshot)

**In VS Code:** Type a message in the box → click **✔ Commit**

**In terminal:**
```bash
git commit -m "Describe what you changed"
```

Write a short, clear message. Think: "What did I do? Why?"  
Good examples: `"Add notes from session 1"` | `"Fix typo in README"` | `"Update data file"`

### Push to GitHub

**In VS Code:** Click **Sync Changes** at the bottom (or the cloud icon)

**In terminal:**
```bash
git push
```

### Pull from GitHub (get the latest)

**In VS Code:** Click **Sync Changes** (it pulls first, then pushes)

**In terminal:**
```bash
git pull
```

> **Tip:** Pull before you Push — always grab the latest version before adding your own changes.

---

## Part 4: See Your History

```bash
git log --oneline
```
Shows a compact list of all your commits. Each line looks like:
```
a1b2c3d Add notes from session 1
e4f5g6h Create README
```

---

## Part 5: VS Code Source Control — Quick Guide

| What you want to do | Where to find it |
|---|---|
| Open Source Control panel | Click the branch icon in left sidebar, or press `Ctrl+Shift+G` |
| Stage a file | Hover over the file → click **+** |
| Unstage a file | Hover over the file → click **−** |
| Write a commit message | Click in the message box at the top of the panel |
| Commit | Click the **✔** button or press `Ctrl+Enter` |
| Push / Pull | Click **Sync Changes** at the bottom |
| See commit history | Click **...** → **View History** (or use the Timeline panel) |

---

## Part 6: Useful Keyboard Shortcuts in VS Code

| Action | Mac | Windows |
|--------|-----|---------|
| Open Source Control | `Cmd+Shift+G` | `Ctrl+Shift+G` |
| Save file | `Cmd+S` | `Ctrl+S` |
| Command Palette | `Cmd+Shift+P` | `Ctrl+Shift+P` |
| Open terminal inside VS Code | `` Cmd+` `` | `` Ctrl+` `` |

---

## Part 7: Common Questions

**Q: What's the difference between `git add` and `git commit`?**  
A: `git add` = "select this for saving" (like putting items in a box). `git commit` = "seal the box and label it." You always do add first, then commit.

**Q: Can I use VS Code instead of the terminal?**  
A: Yes! VS Code's Source Control panel does everything. The terminal commands are just the "behind the scenes" version of the same actions.

**Q: What if I committed the wrong thing?**  
A: Don't panic — Git is designed to protect your work, not delete it. Ask your instructor or TA; it's always recoverable.

**Q: Do I need to `git add .` or add files one by one?**  
A: Either works. `git add .` stages everything at once. Adding files one by one gives you more control over what goes into each commit.

---

## Quick Command Summary

```bash
# First-time setup
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Get a project from GitHub
git clone https://github.com/yourname/repo.git

# Daily workflow
git status                    # See what changed
git add .                     # Stage all changes
git commit -m "Your message"  # Take a snapshot
git push                      # Send to GitHub
git pull                      # Get latest from GitHub

# See history
git log --oneline             # Compact commit list
```
