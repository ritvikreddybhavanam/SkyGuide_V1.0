# 🚀 Complete Git Commands Cheat Sheet

A complete Git reference guide for beginners and developers.
Works with platforms like GitHub and editors like VS Code.

---

# 📦 What is Git?

Git is a distributed version control system used to:

* Track code changes
* Collaborate with teams
* Manage project versions
* Push code to GitHub
* Restore previous versions

---

# ⚙️ Git Installation

## Check Git Version

```bash
git --version
```

---

# 👤 Configure Git

## Set Username

```bash
git config --global user.name "Your Name"
```

## Set Email

```bash
git config --global user.email "youremail@example.com"
```

## Check Configuration

```bash
git config --list
```

## Open Config File

```bash
git config --global --edit
```

---

# 📁 Create Repository

## Initialize Git

```bash
git init
```

## Clone Existing Repository

```bash
git clone <repo-url>
```

Example:

```bash
git clone https://github.com/user/project.git
```

## Clone Specific Branch

```bash
git clone -b branch-name <repo-url>
```

---

# 📄 File Tracking Commands

## Check Status

```bash
git status
```

## Add Single File

```bash
git add file.txt
```

## Add Multiple Files

```bash
git add file1.txt file2.txt
```

## Add All Files

```bash
git add .
```

## Remove File

```bash
git rm file.txt
```

## Stop Tracking File

```bash
git rm --cached file.txt
```

## Rename File

```bash
git mv old.txt new.txt
```

---

# 💾 Commit Commands

## Create Commit

```bash
git commit -m "Initial commit"
```

## Add and Commit Together

```bash
git commit -am "Updated project"
```

## Amend Last Commit

```bash
git commit --amend
```

## Amend Without Changing Message

```bash
git commit --amend --no-edit
```

---

# 🌿 Branch Commands

## Show Branches

```bash
git branch
```

## Create Branch

```bash
git branch feature-login
```

## Switch Branch

```bash
git checkout feature-login
```

OR

```bash
git switch feature-login
```

## Create and Switch Branch

```bash
git checkout -b feature-login
```

OR

```bash
git switch -c feature-login
```

## Rename Branch

```bash
git branch -m old-name new-name
```

## Delete Branch

```bash
git branch -d branch-name
```

## Force Delete Branch

```bash
git branch -D branch-name
```

---

# 🌐 Remote Repository Commands

## Add Remote

```bash
git remote add origin <repo-url>
```

## Show Remotes

```bash
git remote -v
```

## Change Remote URL

```bash
git remote set-url origin <new-url>
```

## Remove Remote

```bash
git remote remove origin
```

---

# 🚀 Push Commands

## Push First Time

```bash
git push -u origin main
```

## Push Changes

```bash
git push
```

## Push Specific Branch

```bash
git push origin branch-name
```

## Force Push

```bash
git push --force
```

## Safer Force Push

```bash
git push --force-with-lease
```

## Push Tags

```bash
git push origin --tags
```

---

# 🔄 Pull and Fetch Commands

## Pull Latest Changes

```bash
git pull
```

## Pull Specific Branch

```bash
git pull origin main
```

## Fetch Changes

```bash
git fetch
```

## Fetch All Branches

```bash
git fetch --all
```

---

# 🔀 Merge Commands

## Merge Branch

```bash
git merge branch-name
```

## Abort Merge

```bash
git merge --abort
```

---

# 🔁 Rebase Commands

## Rebase Branch

```bash
git rebase main
```

## Interactive Rebase

```bash
git rebase -i HEAD~3
```

## Abort Rebase

```bash
git rebase --abort
```

## Continue Rebase

```bash
git rebase --continue
```

---

# ⚔ Merge Conflict Commands

## Check Conflicts

```bash
git status
```

## After Resolving Conflicts

```bash
git add .
git commit
```

---

# ⏪ Undo Commands

## Unstage File

```bash
git reset file.txt
```

## Undo Changes in File

```bash
git checkout -- file.txt
```

## Restore File

```bash
git restore file.txt
```

## Restore All Files

```bash
git restore .
```

## Undo Last Commit Keep Changes

```bash
git reset --soft HEAD~1
```

## Undo Last Commit Delete Changes

```bash
git reset --hard HEAD~1
```

## Reset to Specific Commit

```bash
git reset --hard <commit-id>
```

---

# 🕒 History Commands

## Show Commit History

```bash
git log
```

## One Line History

```bash
git log --oneline
```

## Graph History

```bash
git log --oneline --graph --all
```

## Show Specific Commit

```bash
git show <commit-id>
```

## Show File History

```bash
git log file.txt
```

---

# 🔍 Difference Commands

## Show Unstaged Changes

```bash
git diff
```

## Show Staged Changes

```bash
git diff --staged
```

## Compare Branches

```bash
git diff main..feature
```

---

# 📌 Stash Commands

## Save Temporary Changes

```bash
git stash
```

## Save With Message

```bash
git stash save "work in progress"
```

## Show Stashes

```bash
git stash list
```

## Apply Stash

```bash
git stash apply
```

## Apply and Remove Stash

```bash
git stash pop
```

## Delete Stash

```bash
git stash drop
```

## Delete All Stashes

```bash
git stash clear
```

---

# 🏷 Tag Commands

## Create Tag

```bash
git tag v1.0
```

## Annotated Tag

```bash
git tag -a v1.0 -m "Release version"
```

## Show Tags

```bash
git tag
```

## Delete Tag

```bash
git tag -d v1.0
```

---

# 🔐 GitHub Authentication

## Login with GitHub CLI

```bash
gh auth login
```

## Generate SSH Key

```bash
ssh-keygen -t ed25519 -C "youremail@example.com"
```

## Start SSH Agent

```bash
eval "$(ssh-agent -s)"
```

## Add SSH Key

```bash
ssh-add ~/.ssh/id_ed25519
```

## Test GitHub SSH

```bash
ssh -T git@github.com
```

---

# 🧹 Cleanup Commands

## Remove Untracked Files

```bash
git clean -fd
```

## Remove Ignored Files

```bash
git clean -fdX
```

---

# 📂 .gitignore

## Create .gitignore

```bash
touch .gitignore
```

## Example .gitignore

```gitignore
node_modules/
.env
build/
dist/
*.log
```

---

# 🛠 Advanced Commands

## Cherry Pick Commit

```bash
git cherry-pick <commit-id>
```

## Show Who Changed Lines

```bash
git blame file.txt
```

## Search Commit Message

```bash
git log --grep="bug"
```

## View References

```bash
git reflog
```

## Revert Commit

```bash
git revert <commit-id>
```

---

# 🔥 Delete Git Completely

## Windows CMD

```cmd
rmdir /s /q .git
```

## Linux / Mac

```bash
rm -rf .git
```

---

# 🧠 Most Common Daily Workflow

```bash
# Clone repository
git clone <repo-url>

# Open project
cd project-name

# Create branch
git checkout -b feature-name

# Add changes
git add .

# Commit changes
git commit -m "Added feature"

# Push branch
git push origin feature-name
```

---

# 🚨 Common Problems & Fixes

## Permission Denied

```bash
ssh -T git@github.com
```

## Undo Wrong Push

```bash
git reset --hard HEAD~1
git push --force
```

## Remove Last Commit Only

```bash
git revert HEAD
```

## Pull Before Push Error

```bash
git pull origin main --rebase
```

---

# 📚 Git Workflow Types

## Basic Workflow

```bash
git add .
git commit -m "message"
git push
```

## Feature Branch Workflow

```bash
git checkout -b feature
git add .
git commit -m "feature added"
git push origin feature
```

---

# 🏁 Final Tips

* Commit frequently
* Use meaningful commit messages
* Pull before pushing
* Use branches for features
* Never force push on shared branches
* Keep .gitignore updated

---

# 📖 Useful Git Terms

| Term       | Meaning                   |
| ---------- | ------------------------- |
| Repository | Project storage           |
| Commit     | Saved version             |
| Branch     | Separate development line |
| Merge      | Combine branches          |
| Clone      | Copy repository           |
| Pull       | Download updates          |
| Push       | Upload changes            |
| Stash      | Temporary save            |
| Remote     | Online repository         |

---

# 🎯 Quick Command Summary

| Situation      | Command                  |
| -------------- | ------------------------ |
| Initialize Git | `git init`               |
| Clone Repo     | `git clone url`          |
| Check Status   | `git status`             |
| Add Files      | `git add .`              |
| Commit         | `git commit -m "msg"`    |
| Push           | `git push`               |
| Pull           | `git pull`               |
| Create Branch  | `git checkout -b branch` |
| Merge Branch   | `git merge branch`       |
| Undo Changes   | `git restore .`          |
| View History   | `git log --oneline`      |
| Delete Git     | `rm -rf .git`            |

---

# ✅ End of Git Cheat Sheet
