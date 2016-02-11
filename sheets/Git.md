Git
===

- [Remove branch](/sheets/Git.md#remove-branch)
- [Push specific commit](/sheets/Git.md#all-commits-up-to-specific-sha)

## Branches
### Remove branch

```
git push origin --delete <branchName>
```
or
```
git push origin :<branchName>
```

## Push
### All commits up to specific SHA

```
git push <remotename> <commit SHA>:<remotebranchname>
```
