# Stash local changes
Sometimes you're in the middle of changes for a feature, but are redirected. What do you do with your in process changes? One approach is to stash them. In the following exercises we'll explore some of the uses of stash.

Using the newrepo we created, first make some changes to the readme.md. Then add a new file.

```
echo "get ready to stash" >>readme.md
echo "#File to stash" >stash.md
git status
git stash push
git status
git stash list
```

Note that the untracked file was not included in the stash. the pop command will remove the stash and apply it to your workspace. We then re-stash witht the -u option to include untracked files.

```
git stash pop
git stash push -u
git status
git stash
```

* This technique can be used to apply changes to a different branch. Simply switch branches before applying the stash
* To restage files previously staged, use --index on the apply
* To create a branch using the stash, use the branch command:
```
git stash branch new-branch-from-stash
```





