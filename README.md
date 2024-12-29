# Git Comprehensive Cheat Sheet

This repository contains an extensive Git cheat sheet, detailing commands and their usage with explanations for beginners and advanced users.

---

## Setup
### Configure user information across all local repositories:
```bash
git config --global user.name "[firstname lastname]"
```
- Sets the name associated with your commits, visible in the commit history.

```bash
git config --global user.email "[valid-email]"
```
- Sets the email associated with your commits. Ensure it matches your GitHub or other repository service account.

```bash
git config --global color.ui auto
```
- Enables colored output for Git commands, making it easier to read.

---

## Starting a Repository
### Initialize a new or clone an existing repository:
```bash
git init
```
- Initializes an empty Git repository in the current directory. Use this to start version control on a project.

```bash
git clone [url]
```
- Clones an existing repository from a given URL to your local machine. Useful for working on shared projects.

---

## Stage & Snapshot
### Working with the staging area:
```bash
git status
```
- Displays the state of the working directory and staging area, showing any changes tracked or untracked by Git.

```bash
git add [file]
```
- Stages changes in the specified file for the next commit.

```bash
git add .
```
- Stages all changes in the current directory for the next commit.

```bash
git reset [file]
```
- Unstages a file, keeping changes in the working directory but removing it from the staging area.

```bash
git diff
```
- Shows changes between the working directory and the staging area.

```bash
git diff --staged
```
- Shows changes between the staging area and the last commit.

```bash
git commit -m "[message]"
```
- Saves a snapshot of the changes in the repository with a descriptive commit message.

---

## Branch & Merge
### Managing branches and merging changes:
```bash
git branch
```
- Lists all branches in the repository, marking the current branch with `*`.

```bash
git branch [branch-name]
```
- Creates a new branch with the specified name.

```bash
git checkout [branch-name]
```
- Switches to the specified branch.

```bash
git checkout -b [branch-name]
```
- Creates a new branch and switches to it immediately.

```bash
git merge [branch-name]
```
- Merges changes from the specified branch into the current branch.

```bash
git log
```
- Displays the commit history for the current branch in reverse chronological order.

---

## Share & Update
### Working with remote repositories:
```bash
git remote add [alias] [url]
```
- Adds a remote repository under a specified alias for easier reference.

```bash
git fetch [alias]
```
- Retrieves the latest changes from the remote repository without merging.

```bash
git merge [alias]/[branch]
```
- Merges changes from a remote branch into your current branch.

```bash
git push [alias] [branch]
```
- Sends your local branch changes to the corresponding branch on the remote repository.

```bash
git pull
```
- Fetches changes from the remote repository and merges them into your current branch.

---

## Undoing Changes
### Reverting or discarding changes:
```bash
git reset [file]
```
- Removes the file from the staging area without deleting its changes in the working directory.

```bash
git reset --hard [commit]
```
- Resets the repository to a specific commit, discarding all subsequent changes.

```bash
git revert [commit]
```
- Creates a new commit that undoes the changes made by the specified commit.

---

## Inspect & Compare
### Viewing logs and diffs:
```bash
git log
```
- Displays a detailed commit history.

```bash
git log --stat
```
- Shows commit history with file changes and stats.

```bash
git log --graph
```
- Visualizes the commit history as a tree graph.

```bash
git diff
```
- Shows the difference between the working directory and the last commit.

```bash
git diff HEAD
```
- Compares the working directory with the latest commit.

```bash
git show [SHA]
```
- Displays the details of a specific commit.

---

## Tracking Path Changes
### Managing files and directories:
```bash
git rm [file]
```
- Deletes the specified file from the working directory and stages the removal.

```bash
git mv [old-path] [new-path]
```
- Moves or renames a file and stages the change.

```bash
git log --stat -M
```
- Shows commit logs with detailed information about file path changes.

---

## Temporary Commits
### Stashing changes:
```bash
git stash
```
- Temporarily saves changes that are not ready to be committed.

```bash
git stash list
```
- Lists all stashed changes.

```bash
git stash pop
```
- Applies the latest stash and removes it from the stash list.

```bash
git stash drop
```
- Deletes the latest stash without applying it.

---

## Rewriting History
### Modifying commits:
```bash
git rebase [branch]
```
- Moves or applies changes from the current branch onto another branch.

```bash
git reset --hard [commit]
```
- Completely resets the branch to a previous commit.

---

## Ignoring Patterns
### Prevent staging or committing specific files:
- Create a `.gitignore` file and include patterns to exclude specific files or directories:
```
logs/
*.notes
pattern*/
```
- Set global ignore patterns for all repositories:
```bash
git config --global core.excludesfile [file]
```

---

## Miscellaneous
### Other helpful commands:
```bash
git reflog
```
- Displays a log of reference updates (e.g., branch movements).

```bash
git config --global --edit
```
- Opens the global Git configuration file for manual editing.

```bash
git clean -n
```
- Displays files to be removed from the working directory.

```bash
git clean -f
```
- Permanently removes untracked files from the working directory.

---

This cheat sheet includes comprehensive explanations for each Git command. For further reading, consult the official Git documentation or other resources.
