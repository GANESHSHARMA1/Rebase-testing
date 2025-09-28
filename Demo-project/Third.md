# How to Use Rebase in GitHub

## What is Rebase?

Rebase is a Git command that allows you to move or combine a sequence of commits to a new base commit. It is commonly used to maintain a clean, linear project history.

---

## Why Use Rebase?

- Keeps commit history linear and readable.
- Integrates upstream changes before merging.
- Avoids unnecessary merge commits.

---

## Basic Rebase Workflow

### 1. Clone the Repository

```bash
git clone https://github.com/username/repo.git
cd repo
```

### 2. Create and Switch to a Feature Branch

```bash
git checkout -b feature-branch
```

### 3. Make Changes and Commit

```bash
# Edit files
git add .
git commit -m "Add new feature"
```

### 4. Fetch Latest Changes from Main Branch

```bash
git fetch origin
```

### 5. Rebase Your Branch onto Main

```bash
git rebase origin/main
```

- This applies your commits on top of the latest `main` branch.

### 6. Resolve Conflicts (if any)

- Git will pause and show conflicted files.
- Edit the files to resolve conflicts.
- After resolving, continue rebase:

```bash
git add <resolved-file>
git rebase --continue
```

- Repeat until rebase completes.

### 7. Push Changes

If you already pushed your branch before rebasing, you need to force push:

```bash
git push --force-with-lease
```

---

## Using Rebase in GitHub Pull Requests

1. **Open a Pull Request** as usual.
2. If the base branch has changed, use GitHub’s “Update branch” or rebase locally as above.
3. After rebasing and force-pushing, the pull request will update automatically.

---

## Best Practices

- Use rebase for local feature branches.
- Avoid rebasing shared branches.
- Communicate with your team before force-pushing.

---

## References

- [GitHub Docs: About Git rebase](https://docs.github.com/en/get-started/using-git/about-git-rebase)
- [Atlassian: Git Rebase](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)
