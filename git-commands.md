apt list --upgradable# Git Commands Cheat-sheet

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

- `git checkout -b <branch_name>` : Create a new branch if doesnt exists or switch to existing branch. (do not include **-b**)

- `git chekout <branch_name>` : switch to branch

- `git switch <branch_name>` : Switch branch

- `git merge <branch_needed_to_merge>` : Merge the branch with the current branch

- `git branch -d <branch_name>` : Delete the branch

## Stash & pop

- `git stash` : git stash temporarily saves uncommitted work and clears the working directory.

- **Example:** In the middle of a feature, you need to switch to main to fix a bug → run **git stash**, later use **git stash pop** to restore.

- `git stash pop` : Retrieve unsaved work done with git stash and it clears the stash references.

- `git stash apply` : Retrieve unsaved work done with git stash but keep the reference in stash list for later use.

## Cherry pick

- `git cherry-pick <commit_hash>`: Git cherry-pick allows you to apply a specific commit from one branch onto another without merging the entire branch.

- `git merge --squash <feature_branch>` : Squashing means combining multiple commits into a single commit

