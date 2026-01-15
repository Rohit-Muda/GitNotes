# More Git

## Git Diff, Stash, and Tags

This section covers useful Git commands for comparing changes, saving temporary work, and marking versions.

## Git Diff

`git diff` shows the difference between file versions.

Check unstaged changes:
```bash
git diff
```

Check staged changes:

```bash
git diff --staged
```

Compare branches:

```bash
git diff branch1 branch2
```

Compare commits:

```bash
git diff <commit1> <commit2>
```

## Git Stash

- Git stash is used to temporarily save uncommitted changes.  
- It is helpful when you need to switch branches without committing your work.

Save current changes:
```bash
git stash
```

View all stashes:
```bash
git stash list
```

Apply the most recent stash:
```bash
git stash apply
```

Apply a specific stash:
```bash
git stash apply stash@{0}
```

Apply and remove the stash:
```bash
git stash pop
```

Delete a specific stash:
```bash
git stash drop stash@{0}
```

Clear all stashes:
```bash
git stash clear
```

## Git Tag

Git tags are used to mark specific points in a repository's history, typically used for release versions (e.g., v1.0.0).

---

### Create a Lightweight Tag
A simple pointer to a commit.
```bash
git tag v1.0
```

### Create an Annotated Tag
Stored as a full object, including a message, tagger name, and date.

```bash
git tag -a v1.0 -m "Release 1.0"
```

### List All Tags
Lists the existing tags in the repository.

```bash
git tag
```


### Tag a Specific Commit
Apply a tag to a previous commit using its hash.

```bash
git tag v1.0 <commit-hash>
```

### Push a Tag to Remote
Transfers a specific tag to the remote server.

```bash
git push origin v1.0
```

### Delete a Local Tag
Removes the tag from your local environment.

```bash
git tag -d v1.0
```

### Delete a Remote Tag
Removes the tag from the remote repository.

```bash
git push origin :v1.0
```


## Managing Git History (Simple Guide)

This section explains how Git manages history in a safe and easy-to-understand way.


### Merge Commits

A merge commit is created when you combine one branch into another.

- It keeps changes from both branches
- It preserves full history
- It is the safest and most beginner-friendly approach

Example:
```bash
git checkout main

git merge feature-branch
```

### Rebase (Concept Only)

- Rebase moves your branch commits on top of another branch.

- It makes history look clean and linear

- It rewrites history

- It can cause confusion if used incorrectly

⚠️ Recommendation:
Beginners should avoid using rebase unless they clearly understand it.
Merge is safer in most cases.

Basic idea:

```bash
git checkout feature-branch

git rebase main
```

If conflicts occur, Git pauses and asks you to fix them.



### Git Reflog

git reflog shows a log of recent actions in your repository.

It helps when:
- A commit seems lost
- A branch was deleted by mistake

View reflog:

```bash
git reflog
```

Each entry has a reference like HEAD@{1}.

### Recover Lost Work (Basic Idea)

If something goes wrong, you can reset to a previous state.

```bash
git reset --hard HEAD@{1}
```

This restores your project to an earlier point.

⚠️ Use carefully. This command permanently removes newer changes.

