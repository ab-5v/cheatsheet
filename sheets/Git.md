Git
===

- [Remove branch](/sheets/Git.md#remove-branch)
- [Push specific commit](/sheets/Git.md#all-commits-up-to-specific-sha)
- [Checkout file from specific commit](/sheets/Git.md#checkout-file-from-specific-commit)

## Branch
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

## Checkout
#### Checkout file from specific commit

```
git checkout <commit SHA> <file>
```
