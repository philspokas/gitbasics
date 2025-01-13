# Resolving Merge Conflicts

In the following exercise, we will create a merge conflict so that we can resolve it. We'll use the command line so that we become familiar with what is happening and the commands executed. Under normal circumstances, a text editor such as VS Code is a much more effetive tool for resolving conflicts.

We'll use the newrepo to create a merge conflict we can resolve.

First verify we are on main and the repo is committed.
```
git checkout main
git status
```

Now create a file for our conflict:

```
echo "let's crreate a conflict" > merge.md
git add merge.txt
git commit -m "adding merge file"
git status
```

Next create new branch to use for our merge
```
git checkout -b merge-me
echo "new content to merge" > merge.md
git add *
git commit -m "updated merge text"
git status
```
Switch back to main and add some content to our file:
```
git checkout main
echo "add content to merge " >> merge.md
git add *
git commit -m "update merge file"
git status
```

Now try to merge:
```
git merge merge-me
git status
```
Note that a conflict should be created. Inspect merge.md and notice that merge 'conflict dividers' have been added:
```
type merge.md
```
The most direct way to resolve the conflict is to edit the file in a text editor.







