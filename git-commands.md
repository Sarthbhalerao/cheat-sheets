# Git Commands Cheat-sheet

---

## Installation

- `git --version` → Check installed Git version.
  
- `sudo apt install git -y` → Install Git on Linux.

---

## Setup & Configuration

- `git config --global user.name "your_name"` → Sets your global Git Username.
  
- `git config --global user.email "email"` → Sets your global Git Email.
  
- `git config --list` → Show all Git configuration.
  
- **📌Note → Git uses these details to label your commits**

---

## Repository Setup

- `git init` → Initialize the empty repository into **Git** repository.
  
- `git clone <repo-url>` → Clone existing repository.

---

## Basic Workflow

- `git status` → Shows the current state of the working directory, including modified/untracked files.
  
- `git add <file_name>` → Stage specific file.
  
- `git add .` → Stage all files.
  
- `git commit -m "commit_message"` → Commit staged changes.
  
- `git commit -am "commit_message"` → Stage + commit tracked files.

---

## Viewing Changes

- `git diff` → Show File differences
  
- `git log` → View commit history
  
- `git log --oneline` → View history in a compact view.
  
- `git log --oneline --graph --all` → Visual commit graph.

---

## Branching

- `git branch` → Get the list of all present branches

-  `git branch <branch-name>` → Create branch.

- `git chekout <branch_name>` → switch to branch
  
- `git checkout -b <branch_name>` → Create a new branch if it doesn't exist or switch to an existing branch. (do not include **-b** if only switch required)

- `git switch <branch_name>` → Switch branch

- `git switch -c <branch_name>` → creates a new branch and switches to that branch immediately.

- `git branch -d <branch_name>` → Delete the branch
- `git branch -m <old_branch_name> <new_branch_name>` → rename branch
    - Example: `git branch -m feature/login feature/auth-login`
- `git push origin --delete <branch_name>` → Delete remote branch
    - Example: `git push origin --delete feature/login`

---

## Merging & Rebasing

- `git merge <branch_needed_to_merge>` → Merge the branch with the current branch

- `git merge --squash <branch_name>`→ Squashing means combining multiple commits into a single commit

- `git rebase <branch>` → It integrates changes by replaying your commits on top of the latest state of another branch, creating cleaner and linear history.

- `git rebase -i HEAD~3` → Edit last 3 commits
  
---

## Restore & Unstage

- `git restore <file>` → When you messed up a file and want to discard changes.
- `git restore --staged <file>` → When you accidentally staged a file
---

## Handling Conflicts

- `git status` → Shows conflict files.

- `git add <file_name>` → Mark conflict resolved.

- `git merge --abort` → Cancel merge.
  
---

## Stashing Work

- `git stash` → git stash temporarily saves uncommitted work and clears the working directory.

    - **📌Example→** In the middle of a feature, you need to switch to main to fix a bug → run **git stash**, later use **git stash pop** to restore.

- `git stash list` → List saved stashes.
  
- `git stash pop` → Retrieve unsaved work done with git stash, and it clears the stash references.

- `git stash apply` → Retrieve unsaved work done with git stash, but keep the reference in the stash list for later use.

---

## Cherry pick

- `git cherry-pick <commit_hash>` → Git cherry-pick allows you to apply a specific commit from one branch onto another without merging the entire branch.

---

## Inspect

- `git show <commit_hash>` → See exactly what changed in a commit
- `git blame <file>` → Find who wrote or changed each line

---

## Undo changes

- `git reset`→ git reset moves the HEAD pointer to a specified commit and updates the staging area and/or working directory depending on the reset mode.

  - `git reset --soft <commit_hash>` → It removes the commit ID only, keeps the changes staged so you can commit again
  - `git reset --mixed <commit_hash>` → It removes the commit ID and keeps the changes in the working directory, but unstaged.
  - `git reset --hard <commit_hash>` → Remove the commit ID and also permanently remove the changes.

- `git reflog` → View git history including deleted commits.

- `git revert <commit_hash>` → Safely creates new commits that undo changes but keep the history.

- `git revert --continue` → Continue the revert process.
  
---

## File Removal

- `git rm <file_name>` → Remove file and stage deletion.

- `git rm -f <file_name>` → Forcefully remove file.

---

## Tagging

- `git tag` → List all tags
- `git tag v1.0` → Create a release tag
- `git push origin v1.0` → Push tag to remote

---

## Cleaning

- `git clean -f` → Delete untracked files
      - WARNING: This is irreversible — use `-n` first always
---

## Short Status

- `git status -s` → Quick status view

---

## Amend

- `git commit --amend -m "message"` → Fix last commit

---

## Logs Advanced

- `git log -p` → See commits + code changes

- `git log --stat` → See summary of changes
---

## Working with Remotes

- `git remote add origin <url>` → Add a remote to the repository.

- `git remote -v` → List all remote repositories.

- `git remote set-url origin <url>` → Change the origin URL.

- `git fetch` → Download remote changes

- `git fetch origin <branch_name>` → Fetches the changes from a specific branch, but does not merge the changes

- `git pull origin <branch_name>` → Fetch and merge changes from the remote repository 

- `git push` → Push commits.
  
- `git push origin <branch_name>` → push the changes from local to the remote repository.

- `git push -u origin <branch>` → Push and set upstream.

---

# GitHub CLI (gh) Commands

## Authentication & Setup

- `gh --version` → Displays the installed GitHub CLI version.

- `gh auth login` → Authenticates your GitHub account with the GitHub CLI.

- `gh auth status` → Shows the currently authenticated GitHub account and login status.

---

## Repository Management

- `gh repo create <name> --public --clone --add-readme` → Creates a new public repository on GitHub, initializes it with a README, and clones it locally.

- `gh repo clone owner/repo` → Clones a GitHub repository using GitHub CLI.

- `gh repo view` → Displays details of the current repository in the terminal.

- `gh repo view --web` → Opens the current repository in your default web browser.

- `gh repo list` → Lists repositories associated with your GitHub account.

- `gh repo delete <repo-name> --confirm` → Deletes a repository from GitHub (permanent action).

---

## Issues Management

- `gh issue create --title "<title>" --body "<body>" --label <label>` → Creates a new issue from the terminal.

- `gh issue list` → Lists all open issues in the repository.

- `gh issue view <issue-number>` → Displays details of a specific issue.

- `gh issue close <issue-number>` → Closes an issue directly from the terminal.

---

## Pull Requests

- `gh pr create --fill` –→ Creates a pull request using commit message for title and description.

- `gh pr list` → Lists all open pull requests.

- `gh pr view` → Shows detailed information about a specific pull request.

- `gh pr checkout <pr-number>` → Checks out a pull request locally for review.

- `gh pr review --approve` → Submits an approval review for a pull request.

- `gh pr merge --merge` → Merges a pull request using the default merge method.

- `gh pr merge --squash` → Merges a pull request by squashing all commits into one.

- `gh pr merge --rebase` → Merges a pull request using rebase strategy.

---

## GitHub Actions (Workflows)

- `gh run list --repo owner/repo` → Lists GitHub Actions workflow runs for a repository

- `gh run view <run-id> --repo owner/repo` → Displays details of a specific workflow run.

---

## Advanced & Useful Commands

- `gh api <endpoint>` → Makes a direct GitHub REST API call from the terminal.

- `gh gist create <file>` → Creates a GitHub Gist from a file.

- `gh release create <tag>` → Creates a new GitHub release with a specified tag.

- `gh alias set <alias> "<command>"` → Creates a custom shortcut for frequently used commands.

- `gh search repos <keyword>` → Searches public GitHub repositories from the terminal.

---
