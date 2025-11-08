# 🧰 Git Commands Guide

A quick reference of useful Git commands for initializing repositories, managing commits, working with branches, and connecting to GitHub. Ideal for beginners and intermediate users.

---

## 📁 Initialize a Local Repository

Initializes a new Git repository in the current folder

```
git init
```

---

## 👤 Configure Git User

Sets your global Git username
```
git config --global user.name "YourName"
```
Sets your global Git email
```
git config --global user.email "youremail@example.com"
```

---

## ✅ Check Status and Commit Changes

Clone a remote repository from GitHub to your local machin
```
git clone https://github.com/user/repo.git
```

Check the current status of your repositor
```
git status
```

Add all new and modified files to the staging are
```
git add .
```

Add only modified and deleted files to the staging area
```
git add -
```

Add all changes (new, modified, and deleted files) to the staging are
```
git add -
```

Commit the staged changes with a descriptive messag
```
git commit -m "My first commit"
```


View the commit history of the repository
```
git log
```
---

## 🌿 Branch Management
Create a new branch (does not switch)
```
git branch new-branch
```
Rename a branch
```
git branch -m old-name new-name
```

Switch to another branch
```
git switch branch-name
```

Create and switch to a new branch
```
git switch -c new-branch
```

Switch to another branch (older syntax)
```
git checkout branch-name
```

Go to a specific commit (detached HEAD)
```
git checkout <commit-hash>
```

Delete a branch safely (merged)
```
git branch -d branch-name
```

Force delete a branch
```
git branch -D branch-name
```

List local branches
```
git branch
```

List local and remote branches
```
git branch -a
```

Show last commit of each branch
```
git branch -v
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

## Add directory segure

git config --global --add safe.directory /ruta

---

📌 *Keep this as a cheat sheet for day-to-day Git usage. Modify the URLs, names, and branches to fit your own project.*
