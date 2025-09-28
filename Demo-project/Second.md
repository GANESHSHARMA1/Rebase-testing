# How to Use Cherry Pick in GitHub Using VSCode Command Line

## 1. Open VSCode and Terminal

- Open your project folder in VSCode.
- Open the integrated terminal (`Ctrl + ``).

## 2. Fetch Latest Changes

```sh
git fetch origin
```

## 3. Checkout to Target Branch

```sh
git checkout <target-branch>
```

## 4. Find Commit Hash to Cherry-Pick

- Use the following command to view commit history:

```sh
git log --oneline
```

- Copy the commit hash you want to cherry-pick.

## 5. Cherry-Pick the Commit

```sh
git cherry-pick <commit-hash>
```

## 6. Resolve Conflicts (If Any)

- If there are conflicts, VSCode will highlight them.
- Edit the conflicted files, then stage the changes:

```sh
git add <file>
```

- Continue cherry-pick:

```sh
git cherry-pick --continue
```

## 7. Push Changes to GitHub

```sh
git push origin <target-branch>
```

---

**Note:** Replace `<target-branch>` and `<commit-hash>` with your actual branch name and commit hash.
