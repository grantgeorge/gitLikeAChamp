# Incremental git

Git commits, like Trello cards, should be a reflection of incremental changes.

Think of a commit as snippet of code that might, at some point, need to be
cherry-picked or reverted independently of other commits.

## Cherry-picking

Cherry-picking allows you to apply a particular commit to your branch. It's
awesome for applying commits to a detached branch, applying hotfixes, etc. We
can do hotfixes by fixing master and then cherry-picking the commit to grab
the code that fixes it and applying it to a detached hotfix branch. This allows
us to "work off of master" and only detach for hotfixes. It also ensures that
the same commit hashes used for the hotfix are merged into master.

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

#### This is the title of my new thing

When you're doing git, you can do

```
git rebase -i master
```

for an interactive rebase!
