# Git: version controller
Git is a distributed **version control system** (DVCS) used to track changes in source code during software development.
It helps multiple developers work together on the same project — keeping a complete history of every change, allowing you to revert, compare, or branch your work safely.
# 🧠 Git Commands Reference
---

## 🔧 Configuration

| Command                                            | Description                           |
| -------------------------------------------------- | ------------------------------------- |
| `git config --global user.name "Your Name"`        | Set global username for commits.      |
| `git config --global user.email "you@example.com"` | Set global email for commits.         |
| `git config --list`                                | Show all Git configuration settings.  |
| `git config --global core.editor "code --wait"`    | Set default editor (e.g., VS Code).   |
| `git help <command>`                               | Show help for a specific Git command. |

---

## 📁 Repository Setup

| Command                       | Description                      |
| ----------------------------- | -------------------------------- |
| `git init`                    | Initialize a new Git repository. |
| `git clone <url>`             | Clone a remote repository.(copy to local)|
| `git remote add origin <url>` | Link local repo to a remote one. |
| `git remote -v`               | View current remotes.            |
| `git remote remove <name>`    | Remove a remote repository.      |

---

## 📋 Checking Status

| Command                                | Description                                      |
| -------------------------------------- | ------------------------------------------------ |
| `git status`                           | Display changed files and staging info.          |
| `git diff`                             | Show unstaged changes.                           |
| `git diff --staged`                    | Show changes between index and last commit.      |
| `git log`                              | Show commit history.                             |
| `git log --oneline --graph --decorate` | Compact, visual log.                             |
| `git show <commit>`                    | Display info about a commit.                     |
| `git reflog`                           | Show all HEAD movements (history of operations). |

---

## 🧱 Staging & Committing

| Command                       | Description                                  |
| ----------------------------- | -------------------------------------------- |
| `git add <file>`              | Stage a specific file.                       |
| `git add .`                   | Stage all changes in current directory.      |
| `git restore --staged <file>` | Unstage a file (keep changes).               |
| `git commit -m "message"`     | Commit staged changes.                       |
| `git commit -am "message"`    | Stage and commit all modified tracked files. |
| `git amend -m "new message"`  | Edit the last commit message.                |

---

## 🌿 Branching & Merging

| Command                    | Description                                |
| -------------------------- | ------------------------------------------ |
| `git branch`               | List all local branches.                   |
| `git branch <name>`        | Create a new branch.                       |
| `git branch -d <name>`     | Delete a branch (safe).                    |
| `git branch -D <name>`     | Force delete a branch.                     |
| `git checkout <branch>`    | Switch to another branch.                  |
| `git checkout -b <branch>` | Create and switch to a new branch.         |
| `git switch <branch>`      | Switch branches (modern syntax).           |
| `git merge <branch>`       | Merge another branch into the current one. |
| `git rebase <branch>`      | Reapply commits on top of another branch.  |
| `git cherry-pick <commit>` | Apply a specific commit to current branch. |

---

## ☁️ Working with Remotes

| Command                             | Description                                      |
| ----------------------------------- | ------------------------------------------------ |
| `git fetch`                         | Download objects and refs from a remote repo.    |
| `git pull`                          | Fetch and merge remote branch into local branch. |
| `git push`                          | Push local commits to remote repository.         |
| `git push -u origin <branch>`       | Push and set upstream tracking.                  |
| `git push origin --delete <branch>` | Delete a branch on the remote.                   |
| `git remote show origin`            | Show remote details and tracking info.           |

---

## 🧰 Undoing Changes

| Command                     | Description                                     |
| --------------------------- | ----------------------------------------------- |
| `git restore <file>`        | Discard local changes to a file.                |
| `git reset <file>`          | Unstage a file, keeping local changes.          |
| `git reset --hard <commit>` | Reset everything to a specific commit.          |
| `git revert <commit>`       | Create a new commit that undoes a previous one. |
| `git clean -f`              | Remove untracked files.                         |
| `git clean -fd`             | Remove untracked files and directories.         |

---

## 📦 Stashing Changes

| Command           | Description                             |
| ----------------- | --------------------------------------- |
| `git stash`       | Temporarily save uncommitted changes.   |
| `git stash list`  | List all stashed changes.               |
| `git stash pop`   | Reapply and remove last stash.          |
| `git stash apply` | Reapply last stash without removing it. |
| `git stash drop`  | Delete a stash entry.                   |
| `git stash clear` | Remove all stashes.                     |

---

## 🏷️ Tagging

| Command                             | Description               |
| ----------------------------------- | ------------------------- |
| `git tag`                           | List all tags.            |
| `git tag <name>`                    | Create a lightweight tag. |
| `git tag -a <name> -m "message"`    | Create an annotated tag.  |
| `git push origin <tag>`             | Push a tag to remote.     |
| `git push origin --tags`            | Push all tags to remote.  |
| `git tag -d <name>`                 | Delete a local tag.       |
| `git push origin :refs/tags/<name>` | Delete a remote tag.      |

---

## 🧮 Viewing & Comparing

| Command                        | Description                         |
| ------------------------------ | ----------------------------------- |
| `git log --stat`               | Show commit logs with file changes. |
| `git diff <commit1> <commit2>` | Compare two commits.                |
| `git shortlog`                 | Summarize commits by author.        |
| `git blame <file>`             | Show who last modified each line.   |
| `git show-branch`              | Show branches and their commits.    |

---

## ⚙️ Advanced / Maintenance

| Command                              | Description                                   |
| ------------------------------------ | --------------------------------------------- |
| `git gc`                             | Cleanup unnecessary files and optimize repo.  |
| `git fsck`                           | Check repo for errors or corruption.          |
| `git bisect start`                   | Start binary search to find buggy commit.     |
| `git bisect bad` / `git bisect good` | Mark commits during bisect search.            |
| `git archive`                        | Create archive (e.g., zip/tar) of repo files. |
| `git submodule add <url>`            | Add a submodule repository.                   |
| `git submodule update --init`        | Initialize and update submodules.             |

---

## 🧭 Tips & Shortcuts

| Command                              | Description                                       |
| ------------------------------------ | ------------------------------------------------- |
| `git alias.<alias-name> "<command>"` | Create a custom git alias.                        |
| `git log -p`                         | Show patches (changes) in log.                    |
| `git diff --name-only`               | List changed file names only.                     |
| `git show HEAD~1`                    | View details of the previous commit.              |
| `git describe --tags`                | Show the most recent tag reachable from a commit. |

---

## 📚 Notes

* Use `--help` with any command for detailed documentation.
* Always **commit or stash** before rebasing, merging, or resetting.
* `git status` is your best friend when unsure what’s going on.

---

Would you like me to generate this as a downloadable **README.md file** so you can save or upload it directly to GitHub?
