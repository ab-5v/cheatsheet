Git
===

- [Remove branch](/sheets/Git.md#remove)
- [Cleanup local branches](/sheets/Git.md#cleanup-local-branches)
- [Push specific commit](/sheets/Git.md#all-commits-up-to-specific-sha)
- [Checkout file from specific commit](/sheets/Git.md#file-from-specific-commit)

## Branch
#### Remove

```
git push origin --delete <branchName>
```
or
```
git push origin :<branchName>
```

#### Cleanup local branches
```
git branch -d $(git branch --merged)
git remote prune origin
```

## Push
#### All commits up to specific SHA

```
git push <remotename> <commit SHA>:<remotebranchname>
```

## Checkout
#### File from specific commit

```
git checkout <commit SHA> <file>
```
