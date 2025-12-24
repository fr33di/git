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
Set your Git Repo
```
git remote set-url origin https://github.com/user/repo.git
```

```
git remote get-url origin
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
Add all new and modified files to the staging area
```
git add .
```

Add only modified and deleted files to the staging area
```
git add -u
```
Add all changes (new, modified, and deleted files) to the staging area
```
git add -A
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

Show differences between two branches
```
git diff branch1 branch2
```

Merge a branch into the current branch
```
git merge branch-name
```

Push the current branch to the remote 'main' and set upstream
```
git push -u origin main
```

Pull changes from a remote branch
```
git pull origin branch-name
```

Rebase current branch with changes from remote 'main'
```
git pull --rebase origin main
```

---

### 🔐 Credential Management

Save credentials globally so you don't have to enter them every time
```
git config --global credential.helper store
```
Stop saving credentials globally
```
git config --global --unset credential.helper
```
---

## 🚀 Create and Link GitHub Repo (Using GitHub CLI)

Install GitHub CLI (example for Termux or similar environments)
```
pkg install gh
```

Authenticate with GitHub
```
gh auth login
```

Create a new GitHub repository (Use --private if you want a private repo)
```
gh repo create my-project --public
```

Link local repository to remote and push
```
git remote add origin https://github.com/user/my-project.git
```
```
git branch -M main
```
```
git push -u origin main
```


## Restore to a Previous Commit

To restore the project to a previous stable state, use the following command:

Reset the current branch to a specific commit, discarding all local changes
```
git reset --hard <commit-hash>
```

Force push the current branch to the remote 'main'
```
git push origin main --force
```
---

## Add directory segure

Mark a directory as "safe" for Git operations globally
```
git config --global --add safe.directory /path/to/directory
```
---
