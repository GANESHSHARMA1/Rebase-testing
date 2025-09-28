# Understanding Rebase in GitHub

## What is Rebase?

Rebase is a Git command that allows you to move or combine a sequence of commits to a new base commit. It is commonly used to maintain a clean, linear project history.

## Why Use Rebase?

- Keeps commit history clean and linear
- Makes it easier to review changes
- Avoids unnecessary merge commits

## How to Rebase

1. **Fetch the latest changes:**
    ```bash
    git fetch origin
    ```
2. **Switch to your feature branch:**
    ```bash
    git checkout feature-branch
    ```
3. **Rebase onto the main branch:**
    ```bash
    git rebase origin/main
    ```
4. **Resolve any conflicts, then continue:**
    ```bash
    git add .
    git rebase --continue
    ```

## Best Practices

- Use rebase for local changes before merging to main
- Avoid rebasing shared branches

## Resources

- [GitHub Docs: About Git Rebase](https://docs.github.com/en/get-started/using-git/about-git-rebase)
- [Atlassian: Git Rebase](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)