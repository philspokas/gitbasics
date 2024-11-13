# Stash local changes
Sometimes you're in the middle of changes for a feature, but are redirected. What do you do with your in process changes? One approach is to stash them. In the following exercises we'll explore some of the uses of stash.

Using the newrepo we created, first make some changes to the readme.md. Then add a new file.

```
echo "#File to stash" >stash.md
git status
git stash push
git status
git stash list
```

Note that the untracked file was not included in the stash

```
git stash pop
git stash push -u
git status
git stash
```


