# Git Troubleshooting Guide
## Step-by-Step Help When Something Goes Wrong

Don't panic — every error you see has been seen by thousands of other learners. This guide will walk you through the most common issues.

---

## Before You Panic

Remember:
- Git is **designed to protect your work**, not delete it
- There is almost no "unfixable" Git problem
- When in doubt: take a screenshot of the error and ask your instructor or TA

---

## SECTION 1: Git Setup & First Commit

```
Problem: You see "command not found: git"
    ↓
→ Git is NOT installed on your computer.
  Solution:
    - Mac: Open Terminal, type: xcode-select --install
    - Windows: Download from git-scm.com/downloads and run the installer
    - Then close and reopen your terminal and try again.
```

---

```
Problem: "Author identity unknown" error when committing
    ↓
→ You haven't told Git your name and email yet.
  Solution — run these two commands in the terminal:

    git config --global user.name "Your Name"
    git config --global user.email "your.email@example.com"

  Use the same email as your GitHub account.
  Then try committing again.
```

---

```
Problem: You typed "git init" but got an error
    ↓
→ You're probably in the wrong folder.
  Solution:
    - Type: pwd   (Mac/Linux)  or  cd   (Windows)
    - This shows you which folder you're in.
    - Use cd to navigate to your project folder, then try git init again.
```

---

## SECTION 2: Pushing to GitHub

```
Problem: "fatal: remote origin already exists"
    ↓
→ You already added a GitHub connection. No need to add it again.
  Solution — remove the old one and add the correct URL:

    git remote remove origin
    git remote add origin https://github.com/yourname/repo.git
```

---

```
Problem: "Permission denied" or "401 Unauthorized" when pushing
    ↓
→ GitHub couldn't verify who you are.
  Solution:
    1. Make sure you're using HTTPS (not SSH). Your URL should start with https://
    2. When VS Code or the terminal asks for a username/password,
       use your GitHub username and a Personal Access Token (not your password).
       You can create one at: github.com → Settings → Developer settings → Personal access tokens
    3. If still stuck, ask your instructor.
```

---

```
Problem: "Your branch is ahead of 'origin/main' by X commits"
    ↓
→ You have commits on your computer that haven't been sent to GitHub yet.
  Solution — just push:

    git push

  Or in VS Code: click "Sync Changes".
```

---

```
Problem: "Your branch is behind 'origin/main'"
    ↓
→ GitHub has newer changes that you don't have locally yet.
  Solution — pull first:

    git pull

  Or in VS Code: click "Sync Changes" (it pulls before pushing).
```

---

## SECTION 3: VS Code Source Control

```
Problem: You can't find the Source Control panel
    ↓
→ Look for the branching-lines icon in the left sidebar.
  Keyboard shortcut: Ctrl+Shift+G (Windows) or Cmd+Shift+G (Mac)
  
  If you still don't see your changed files:
    1. Make sure you saved the file first (Ctrl+S / Cmd+S)
    2. Make sure your folder is inside a Git repo
       (the folder should have been created via "Git: Clone" or "git init")
```

---

```
Problem: The "+" button isn't showing when you hover over a file
    ↓
→ Try hovering directly over the filename (not the folder).
  If that doesn't work:
    - Click on the file name — it will open a diff view
    - Then look for the Stage button in the top-right of that view
```

---

```
Problem: "Sync Changes" is greyed out or nothing happens
    ↓
→ You may not have committed anything yet, or VS Code needs to authenticate.
  Check:
    1. Did you write a commit message AND click the checkmark (✔)?
    2. Is your GitHub account connected to VS Code?
       - Click the profile/account icon at the bottom-left of VS Code
       - Sign in with your GitHub account if prompted
```

---

## SECTION 4: Common Error Lookup

| Error Message | What It Means | Fix |
|---|---|---|
| `fatal: not a git repository` | You're not in a Git project folder | Navigate into your project folder first |
| `no changes added to commit` | You forgot to stage your files | Run `git add .` then `git commit` |
| `nothing to commit, working tree clean` | No changes have been made | Edit a file, save it, then try again |
| `fatal: remote origin already exists` | GitHub connection already set up | Remove with `git remote remove origin`, then re-add |
| `Author identity unknown` | Git doesn't know your name/email | Run `git config --global user.name` and `user.email` |
| `Could not resolve host: github.com` | No internet connection | Check your Wi-Fi and try again |
| `Your branch is ahead of 'origin/main'` | Local commits not pushed yet | Run `git push` |
| `Your branch is behind 'origin/main'` | GitHub has newer changes | Run `git pull` |

---

## Still Stuck? Follow These Steps

```
Step 1: Read the error message carefully.
        Look for key words like: "denied", "not found", "conflict", "unknown"
        Check the table above for that word.

    ↓

Step 2: Try running "git status" in the terminal.
        It will tell you the current state of your project and often suggest what to do next.

    ↓

Step 3: Take a screenshot of the error.
        Share it in your class channel or show your instructor.
        You'll have help within minutes.
```

---

## You've Got This 💪

Every developer — from beginners to professionals — runs into these errors. The difference is just knowing how to read them. You're doing great.
