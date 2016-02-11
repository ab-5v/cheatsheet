Git
===

- [Remove branch](/sheets/Git.md#remove-branch)

## Push
### All commits up to specific SHA

```
git push <remotename> <commit SHA>:<remotebranchname>
```

## Branches
### Remove branch

```
git push origin --delete <branchName>
```
or
```
git push origin :<branchName>
```
