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

- `git checkout -b <branch_name>` : Create a new branch if doesnt exists or switch to existing branch. (do not include **-b**)

- `git chekout <branch_name>` : switch to branch

- `git switch <branch_name>` : Switch branch

- 
