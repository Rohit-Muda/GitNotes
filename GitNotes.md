# Git Workflow

The basic Git workflow:

- Initialize the repository

- Stage files

- Commit changes

- Push to GitHub

---

### Creating a Repository

A repository is a normal project folder that Git tracks to record changes.

```bash
git init

git status
```
### Staging Files

Staging means selecting files that are ready to be committed.

```bash
git add <file> <file2>

git status
```

Add all files:
```bash
git add .
```

### Commit

A commit saves the staged changes permanently.

```bash
git commit -m "commit message"

git status
```

- Commit messages should clearly describe the change

### View Commit History

To get Detailed log of commits

```bash
git log
```

Short format:

One line Summary of each commit

```bash
git log --oneline
```

### .gitignore

The .gitignore file tells Git which files or folders to ignore.

Example:

```text
node_modules
.env
.vscode
```
- Ignored files will not appear in git status.

<br>
<br>


# Branches in Git

## What is a Branch?

A branch is a separate version of your project.  
It allows you to work on new features or bug fixes without affecting the main code.

Multiple developers can work in parallel using branches.

---

## HEAD in Git

`HEAD` points to the branch you are currently working on.

- It always points to the latest commit of the active branch
- When you switch branches, `HEAD` moves with it

The default branch is called `main`.

---

## Create and Switch Branches

Common commands:

```bash
git branch 
git branch BugFix
git switch BugFix
git switch main
git switch -c newFeature
git checkout newFeature
```

Explanation:

- git branch -> list all branches

- git branch BugFix -> create a new branch

- git switch BugFix -> switch to a branch

- git switch -c newFeature -> create and switch to a new branch

- git checkout newFeature -> switch to a branch


## Merging Branches

Merging brings changes from one branch into another.

### Fast-Forward Merge

Used when the main branch has no new commits.
```bash
git checkout main

git merge bug-fix
```

- No conflicts

- No merge commit

### 3-Way Merge

Used when both branches have new commits.

```bash
git checkout main
git merge bug-fix
```

- Git creates a merge commit
- Conflicts may occur


### Rename a Branch

```bash
git branch -m <old-branch-name> <new-branch-name>
```

## Delete a Branch

```bash
git branch -d <branch-name>
```

## List All Branches

```bash
git branch
```
