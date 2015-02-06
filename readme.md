# This is a read.me

Git commits, like Trello cards, should be done in "increments"

Think of a commit as shipment of code that might, at some point, need to be
cherry-picked or reverted independent of the other commits that it's associated
with.

## Cherry-picking

Cherry-picking allows you to apply a particular commit to your branch. It's
awesome for applying commits to a detached branch, applying hotfixes, etc. We
can do hotfixes by fixing master and then cherry-picking the commit to grab
the code that fixes it and applying it to a detached hotfix branch.

```
git cherry-pick <hash>
```

## Reverting

Like cherry-picking, you can revert hashes. This is critically important for
reverting state of the master branch for hotfixes. If we can ID a commit that's
breaking a feature or causes a significant bug by it's hash, we can revert
that particular hash instead of the entire branch.

```
git revert <hash>
```
