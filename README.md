# 🧰 Git Commands Guide

A quick reference of useful Git commands for initializing repositories, managing commits, working with branches, and connecting to GitHub. Ideal for beginners and intermediate users.

---

## 📁 Initialize a Local Repository

```bash
git init
```

---

## 👤 Configure Git User

```bash
git config --global user.name "YourName"
git config --global user.email "youremail@example.com"
git config --global user.password "your_password"      # ⚠️ Not recommended
git remote add origin https://github.com/user/repo.git
```

---

## ✅ Check Status and Commit Changes

```bash
git clone https://github.com/user/repo.git
git status
git add .             # Add all new/modified files
git add -u            # Add only modified/deleted files
git add -A            # Add all changes (new, modified, deleted)
git commit -m "My first commit"
git log               # View commit history
```

---

## 🌿 Branch Management

```bash
git branch new-branch                  # Create a new branch
git branch -m old-name new-name        # Rename a branch
git switch branch-name                 # Switch to a branch
git switch -c new-branch               # Create and switch to a new branch
git checkout branch-name               # Alternate way to switch
git checkout <commit-hash>            # Go to a specific commit
git branch -d branch-name              # Delete a branch (safe)
git branch -D branch-name              # Force delete a branch
```

---

## 🔀 GitHub and Remote Operations

```bash
git diff branch1 branch2              # Show differences between branches
git merge branch-name                 # Merge branch into current
git push -u origin main               # Push to remote main
git pull origin branch-name           # Pull from remote branch
git pull --rebase origin main         # Rebase changes from remote
```

---

### 🔐 Credential Management

```bash
git config --global credential.helper store       # Save credentials
git config --global --unset credential.helper     # Stop saving credentials
```

---

## 🚀 Create and Link GitHub Repo (Using GitHub CLI)

```bash
pkg install gh                         # Install GitHub CLI (e.g., in Termux)
gh auth login                          # Authenticate with GitHub

# Create a new GitHub repository
gh repo create my-project --public     # Use --private if preferred

# Link to remote and push
git remote add origin https://github.com/user/my-project.git
git branch -M main
git push -u origin main
```
## Restore to a Previous Commit

To restore the project to a previous stable state, use the following command:

```bash
git reset --hard <commit-hash>
git push origin main --force

---

📌 *Keep this as a cheat sheet for day-to-day Git usage. Modify the URLs, names, and branches to fit your own project.*
