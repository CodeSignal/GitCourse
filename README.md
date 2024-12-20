## Welcome

<p>
  Welcome to the <strong>Git Cheat sheet Repository</strong>. This repository is created to support the <strong>Git Version Control for Beginners</strong> CodeSignal Course Path, designed to help learners master Git fundamentals and advanced workflows. <img src="https://k3-production-bucket.s3.amazonaws.com/uploads/ZuF4WKfiXWD9P3Cme_cosmo-greeting.svg" alt="Cosmo" width="160" style="float: right; margin-left: 10px;">
</p>

## About CodeSignal

**CodeSignal Learn** is a platform for skill assessment and development. It offers a variety of courses, challenges, and learning paths that help individuals improve their technical skills in areas like programming and data science, enhance soft skills and sales expertise, and prepare effectively for interviews.

The **Git Version Control for Beginners** course path focuses on building practical knowledge of Git for real-world software development. The course path covers a variety of topics, starting from basic Git commands to mastering working with remote repositories. 

For more information about this course path, visit this [link](#). 


## About This Repository

This repository is your **companion to the Git Course Path** and serves as a quick reference for essential Git commands. It's designed to help you:
- Quickly recall **frequently used commands**.
- Reinforce your learning through a **structured cheat sheet**.

Whether you're starting with Git or looking to 
solidify your knowledge, this cheat sheet provides an organized view of the most important commands.

---

## Table of Contents
- [Getting Started with Git](#getting-started-with-git)
- [Tracking and Managing Changes](#tracking-and-managing-changes)
- [Branching and Collaboration](#branching-and-collaboration)
- [Undoing and Modifying Changes](#undoing-and-modifying-changes)
- [Exploring and Comparing](#exploring-and-comparing)
- [Ignoring Files](#ignoring-files)
- [Stashing Changes](#stashing-changes)

---

## Getting Started with Git

### Setting Up Your Environment

These commands configure your identity and preferences:

- `git config --global user.name "[Your Name]"`  
  Set your username for commits.
- `git config --global user.email "[Your Email]"`  
  Set your email address for commits.
- `git config --list`  
  Display your current Git configuration.

### Starting a Repository
- `git init`  
  Turn a folder into a Git repository.
- `git clone [url]`  
  Copy an existing repository to your local machine.

---

## Tracking and Managing Changes

### Staging and Committing Changes

Prepare and save your changes with these commands:

- `git status`  
  View the status of your working directory and staged files.
- `git add [file]`  
  Stage specific changes.
- `git add .`  
  Stage all changes in the current directory.
- `git commit -m "[message]"`  
  Create a commit with a message describing the changes.
- `git commit --amend`  
  Modify the most recent commit (e.g., to fix a message).

### Removing or Unstaging Changes
- `git restore [file]`  
  Discard changes in a file (unstaged).
- `git restore --staged [file]`  
  Unstage changes while keeping them in your working directory.

---

## Branching and Collaboration

### Working with Branches

Branches allow parallel development:
- `git branch`  
  List all branches.
- `git branch -r`  
  List all remote branches.
- `git branch [branch-name]`  
  Create a new branch.
- `git switch [branch-name]`  
  Switch to a different branch.
- `git checkout [branch-name]`  
  Switch to a specific branch.  
- `git checkout -b [branch-name]`  
  Create a new branch and switch to it in one step.
- `git switch -c [branch-name]`  
  Create a new branch and switch to it.
- `git branch -d [branch-name]`  
  Delete a branch.
- `git branch -D [branch-name]`  
  Force delete a branch.
- `git branch -m [new-branch-name]`  
  Rename the current branch.

### Merging and Applying Changes
Combine changes from branches or commits into your current branch to integrate updates.
- `git cherry-pick [commit-hash]`  
  Apply changes from a specific commit to the current branch.
- `git merge [branch-name]`  
  Merge the specified branch into the current branch.
- `git rebase [branch-name]`  
  Reapply commits from the current branch onto the specified branch to maintain a linear history.
- `git rebase --continue`  
  Resume an interrupted rebase after resolving conflicts.
- `git rebase -i HEAD~N`  
  Start an interactive rebase for the last N commits, allowing you to edit, reorder, squash, or drop commits.
### Pushing and Pulling Changes

Collaborate with others using remote repositories:
- `git remote add origin [url]`  
  Add a remote repository to your project.
- `git push origin [branch-name]`  
  Push local changes from the specified branch to a remote repository.
- `git push -u origin [branch-name]`  
  Push changes to a remote branch and track it.
- `git fetch origin`  
  Download updates from the remote repository without merging them into your current branch.
- `git pull origin [branch-name]`  
  Fetch and merge changes from a remote branch.
---

## Undoing and Modifying Changes

### Reverting or Resetting Commits

These commands help you modify commit history carefully:
- `git revert [commit-hash]`  
  Create a new commit that undoes changes from a specific commit.
- `git reset --soft [commit]`  
  Move the HEAD pointer but keep staged changes.
- `git reset --hard [commit]`  
  Undo commits and discard all uncommitted changes.

---

## **Exploring and Comparing**

### **Viewing Logs and Diffs**

Understand and analyze changes in your repository with these commands:

- `git log --oneline`  
  Display a compact commit history.  

- `git diff`  
  Compare unstaged changes with the most recent commit.  

- `git diff [branch-name]`  
  Compare your current branch with another branch.  

- `git diff commit1..commit2`  
  Compare changes between two commits.  

- `git diff branch1..branch2`  
  Compare the differences between two branches.  

- `git diff --staged`  
  Show differences between staged changes and the last commit.  

- `git diff --cached`  
  Show differences between staged changes and the last commit (same as `--staged`).  

- `git show [commit-hash]`  
  Show the details of a specific commit.  

- `git reflog`  
  Show a log of all reference updates (e.g., branch checkouts, commits, resets, and rebases).

### **Working with Tags**

Use tags to mark important commits:

- `git tag [tag-name]`  
  Create a lightweight tag for the current commit.  

- `git tag -l`  
  List all tags in the repository.  

- `git tag -a [tag-name] -m "[message]"`  
  Create an annotated tag with a message for the current commit.  

- `git tag -d [tag-name]`  
  Delete a tag locally.  

---

## Ignoring Files

### Using `.gitignore`

Control which files Git should ignore:
- Save patterns in `.gitignore`:
  ```plaintext
  # Ignore compiled files
  *.o
  *.class
  ```
  
---

## Stashing Changes

### Temporarily Saving Progress

Stash allows you to save your changes without committing:
- `git stash`  
  Temporarily store your uncommitted changes.
- `git stash apply`  
  Apply the most recent stash without removing it.
- `git stash drop`  
  Delete the most recent stash.
- `git stash clear`  
  Remove all stashes from your repository.
- `git stash -u`  
  Stash tracked and untracked changes.  
- `git stash list`  
  Show saved stashes.
---
