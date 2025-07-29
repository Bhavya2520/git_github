# git_github
This repository serves as a comprehensive guide to understanding Git and GitHub, curated for learning purposes. It covers everything from the basics of version control to more advanced Git operations, making it ideal for beginners and intermediate users alike.
# Git & GitHub Guide

## What is Git?
Git is a free and open-source distributed version control system that manages everything GitHub-related locally on your machine.

---

## Alternatives to GitHub
Platforms similar to GitHub used for version control and collaboration:

- **GitLab**: Best for all-in-one DevOps lifecycle
- **Bitbucket**
- **SourceForge**
- **AWS CodeCommit**
- **Azure Repos**

---

## Common Git Commands

### `git init`
- Creates a hidden `.git` folder in your directory containing metadata.

### `git status`
- Shows the current state of the working directory and staging area.

### `git add .`
- Stages all changes (new, modified, deleted files).

### `git add <filename>`
- Stages a specific file.

### `git commit -m "message"`
- Commits staged changes with a message.

### `git restore --staged <filename>`
- Unstages a file without discarding changes.

### `git log`
- Views the commit history.

### Undo Last Commits
- Use `git log`, copy the hash before the last 2 commits, and reset:
