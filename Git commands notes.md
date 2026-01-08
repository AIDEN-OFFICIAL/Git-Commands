# Git: version controller
Git is a distributed **version control system** (DVCS) used to track changes in source code during software development.
It helps multiple developers work together on the same project — keeping a complete history of every change, allowing you to revert, compare, or branch your work safely.

- Working Directory → where you edit files.
- Staging Area (Index) → where you prepare files for commit.
- Repository (.git folder) → where Git permanently stores all versions.

## 🔑 Why Developers Use Git
- To track every change in a project.
- To collaborate without overwriting each other’s work.
- To experiment safely with branches.
- To revert mistakes easily.
- To synchronize code between local and remote repositories.

---
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
| `git commit --amend -m "new message"`  | Edit the last commit message.                |

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

# ⚖️ Git Commands – Common Differences Explained

A quick guide to understanding the differences between similar or easily confused Git commands.

## 🌀 git fetch vs git pull
| Command      | Description                                                                                        |
| ------------ | -------------------------------------------------------------------------------------------------- |
| `git fetch` | Downloads commits, branches, and files from a remote repository but doesn’t merge them into your current branch. |
| `git pull` | Does everything fetch does, plus merges the fetched commits into your current branch.      |

Example:
- `git fetch origin main`   # Updates remote tracking branch only
- `git merge origin/main`   # Merge manually (safer)
**Example:**

```bash
git fetch origin main  # Updates remote tracking branch only
git merge origin/main   # Merge manually (safer)
```
**Note:**
Use `fetch` when you want to review changes before merging, and pull when you’re confident and ready to update your branch immediately.

---


---

## 🌿 git merge vs git rebase

| Command      | Description                                                                                        |
| ------------ | -------------------------------------------------------------------------------------------------- |
| `git merge`  | Combines changes from one branch into another, preserving commit history (creates a merge commit). |
| `git rebase` | Reapplies commits from one branch on top of another, resulting in a linear, cleaner history.       |

**Example:**

```bash
git merge feature-branch    # Keeps both histories
git rebase main             # Moves commits as if made on top of main
```

**Note:**
Use `merge` for shared/public branches.
Use `rebase` for cleaning up local feature branches before merging.

---

## 📥 git clone vs git fork

| Command     | Description                                                                                           |
| ----------- | ----------------------------------------------------------------------------------------------------- |
| `git clone` | Creates a local copy of an existing repository.                                                       |
| `git fork`  | (On platforms like GitHub) creates your own copy of someone else's repository in your GitHub account. |

**Example:**

```bash
git clone https://github.com/user/repo.git
```

**Note:**
Forking is done online (GitHub UI), cloning is done locally via Git.

---

## 🧰 git reset vs git revert

| Command      | Description                                                                     |
| ------------ | ------------------------------------------------------------------------------- |
| `git reset`  | Moves the HEAD pointer to a specific commit — can change history (destructive). |
| `git revert` | Creates a new commit that undoes a previous one — keeps history intact (safe).  |

**Example:**

```bash
git reset --hard HEAD~1    # Delete last commit
git revert HEAD            # Undo last commit safely
```

**Note:**
Use `revert` for public branches; use `reset` only locally when no one else has pulled your changes.

---

## 🧺 git stash vs git commit

| Command      | Description                                                      |
| ------------ | ---------------------------------------------------------------- |
| `git stash`  | Temporarily saves uncommitted changes without creating a commit. |
| `git commit` | Permanently records changes into repo history.                   |

**Example:**

```bash
git stash        # Save for later
git stash pop    # Reapply stashed changes
```

**Note:**
Use `stash` when you need to switch branches quickly but aren’t ready to commit.

---

## 🪶 git checkout vs git switch vs git restore

| Command        | Description                                                                |
| -------------- | -------------------------------------------------------------------------- |
| `git checkout` | Old multi-purpose command used for switching branches and restoring files. |
| `git switch`   | Newer, clearer command for switching branches only.                        |
| `git restore`  | Newer command for restoring file changes.                                  |

**Example:**

```bash
git switch feature-branch     # Switch branch
git restore file.txt          # Discard changes
```

**Note:**
`switch` and `restore` are safer and more readable replacements for `checkout`.

---

## 🔄 git push vs git push -u

| Command                       | Description                                                         |
| ----------------------------- | ------------------------------------------------------------------- |
| `git push`                    | Pushes your local commits to a remote branch (if tracking is set).  |
| `git push -u origin <branch>` | Pushes your branch and sets it as upstream, linking local ↔ remote. |

**Example:**

```bash
git push -u origin feature-branch
```

**Note:**
Use `-u` the first time you push a branch; afterward, you can just use `git push`.

--

## 🏷️ git tag vs git branch

| Command      | Description                                                 |
| ------------ | ----------------------------------------------------------- |
| `git tag`    | Marks a specific commit as a version or milestone (static). |
| `git branch` | Creates a new line of development (active).                 |

**Example:**

```bash
git tag v1.0
git branch feature-x
```

**Note:**
Tags are snapshots; branches are ongoing lines of work.

---

## 🔍 git log vs git reflog

| Command      | Description                                                           |
| ------------ | --------------------------------------------------------------------- |
| `git log`    | Shows commit history of the repository.                               |
| `git reflog` | Shows all actions affecting HEAD (including resets, checkouts, etc.). |

**Example:**

```bash
git log
git reflog
```

**Note:**
Use `reflog` to recover commits after accidental resets or deletes.

---

## 🧩 git fetch vs git clone

| Command     | Description                                           |
| ----------- | ----------------------------------------------------- |
| `git fetch` | Updates your existing local repo with remote changes. |
| `git clone` | Downloads the entire remote repo as a new local copy. |

**Example:**

```bash
git clone https://github.com/user/repo.git
git fetch origin
```

**Note:**
`clone` = first-time setup.
`fetch` = update an existing repo.

---

## 📦 git pull vs git merge

| Command     | Description                                                               |
| ----------- | ------------------------------------------------------------------------- |
| `git pull`  | Fetches and merges the remote branch automatically.                       |
| `git merge` | Combines any branch (local or fetched) into your current branch manually. |

**Example:**

```bash
git pull origin main   # Fetch + Merge
git merge feature      # Merge manually
```

**Note:**
`pull` = automated merge from remote.
`merge` = manual, flexible integration of branches.

---


## 📚 Notes

* Use `--help` with any command for detailed documentation.
* Always **commit or stash** before rebasing, merging, or resetting.
* `git status` is your best friend when unsure what’s going on.

---
