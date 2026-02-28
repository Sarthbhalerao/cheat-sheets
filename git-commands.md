# Git Commands Cheat-sheet

---

- `git --version` : Used to check the git version.
- `sudo apt install git -y` : Install git if not found.

## Setup & Configuration

- `git config --global user.name "your_name"` : Sets your global Git Username.
- `git config --global user.email "email"` : Sets your global Git Email.
- **Note: Git use this details to label your commits**

## Basic Workflow

- `git init` : Initialize the empty repository into **Git** repository.

## View Changes

- `git status` : Shows the current state of working directory including modified/untracked files.

- `git add <file_name>` : Stage your file.

- `git status` : check staged files.

- `git commit -m "commit message"` : commit your changes.

- `git log` : view history

- `git log --oneline` : View history in compact view.

- `git diff` : See changes

## Branching

- `git branch` : Get the list of all present branches 

- `git checkout -b <branch_name>` : Create a new branch if doesnt exists or switch to existing branch. (do not include **-b** if only switch required)

- `git chekout <branch_name>` : switch to branch

- `git switch <branch_name>` : Switch branch

- `git switch -c <branch_name>`: creates a new branch and switches to that branch immediately.

- `git merge <branch_needed_to_merge>` : Merge the branch with the current branch

- `git branch -d <branch_name>` : Delete the branch

## Stash & pop

- `git stash` : git stash temporarily saves uncommitted work and clears the working directory.

- **Example:** In the middle of a feature, you need to switch to main to fix a bug → run **git stash**, later use **git stash pop** to restore.

- `git stash pop` : Retrieve unsaved work done with git stash and it clears the stash references.

- `git stash apply` : Retrieve unsaved work done with git stash but keep the reference in stash list for later use.

## Cherry pick

- `git cherry-pick <commit_hash>`: Git cherry-pick allows you to apply a specific commit from one branch onto another without merging the entire branch.

- `git merge --squash <branch_name>` : Squashing means combining multiple commits into a single commit

- `git revert <hash>` : Sfaely creates new commits that undo changes but keeps the history.

- `git reset` : It moves HEAD pointer back by one , deleting commits & without laving history behind.

  - `git reset --soft <hash>` : It removes commit id only, keeps the changes staged so you can commit again
  - `git reset --mixed <hash>` : It removes commit id and keeps the chnages in working directory but unstaged.
  - `git reset --hard <hash>` ; remove commit id and also permanently removes the changes.

- `git rebase <branch>` : It integrates changes by replaying your commits on top of the latest state of another branch , creating cleaner and linear history.

- `git rm <file_name>` : Remove file

- `git remove -f <file_name>` : Forcefully remove file.

- `git remote add origin <url>` : Add a remote to the repository.

- `hit remote set-url origin <url>` : change the origin url.

- `git fetch origin <main>` : Fetches the changes not merges the changes

- `git pull origin <main>` : Fetch and merge changes from remote repo

- `git push origin <main>` : push the changes from local to remote repository.


# GitHub CLI (gh) Commands

## Authentication & Setup

`gh --version` – Displays the installed GitHub CLI version.

`gh auth login` – Authenticates your GitHub account with the GitHub CLI.

`gh auth status` – Shows the currently authenticated GitHub account and login status.

---

## Repository Management

`gh repo create <name> --public --clone --add-readme` – Creates a new public repository on GitHub, initializes it with a README, and clones it locally.

`gh repo clone owner/repo` – Clones a GitHub repository using GitHub CLI.

`gh repo view` – Displays details of the current repository in the terminal.

`gh repo view --web` – Opens the current repository in your default web browser.

`gh repo list` – Lists repositories associated with your GitHub account.

`gh repo delete <repo-name> --confirm` – Deletes a repository from GitHub (permanent action).

---

## Issues Management

`gh issue create --title "<title>" --body "<body>" --label <label>` – Creates a new issue from the terminal.

`gh issue list` – Lists all open issues in the repository.

`gh issue view <issue-number>` – Displays details of a specific issue.

`gh issue close <issue-number>` – Closes an issue directly from the terminal.

---

## Pull Requests

`gh pr create --fill` – Creates a pull request using commit message for title and description.

`gh pr list` – Lists all open pull requests.

`gh pr view` – Shows detailed information about a specific pull request.

`gh pr checkout <pr-number>` – Checks out a pull request locally for review.

`gh pr review --approve` – Submits an approval review for a pull request.

`gh pr merge --merge` – Merges a pull request using the default merge method.

`gh pr merge --squash` – Merges a pull request by squashing all commits into one.

`gh pr merge --rebase` – Merges a pull request using rebase strategy.

---

## GitHub Actions (Workflows)

`gh run list --repo owner/repo` – Lists GitHub Actions workflow runs for a repositor[Oy.

`gh run view <run-id> --repo owner/repo` – Displays details of a specific workflow run.

---

## Advanced & Useful Commands

`gh api <endpoint>` – Makes a direct GitHub REST API call from the terminal.

`gh gist create <file>` – Creates a GitHub Gist from a file.

`gh release create <tag>` – Creates a new GitHub release with a specified tag.

`gh alias set <alias> "<command>"` – Creates a custom shortcut for frequently used commands.

`gh search repos <keyword>` – Searches public GitHub repositories from the terminal.
