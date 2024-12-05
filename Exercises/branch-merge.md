# Branching and Merging
Branching and merging branches are key features and functions of git.

We'll create some branches and merge the changes.

## Basic branching
Using newrepo create a branch and add a file to it.

## Merge no fast forward

In this exercise we'll create a branch on which to do some work and then merge the changes using a standard merge. In order to represent a good tree, we'll need to diverge the branches

```
git checkout -b newstuff
echo "new stuff" >newstuff.md
git add .
git commit -m "add new stuff"
echo "more stuff " >> newstuff.md
git commit -am "more stuff"
```
Now we go back to main, do an update and merge
```
git checkout main
echo "more readme" >>readme.md
git commit -am "add to readme"
git log --oneline --decorate --graph --all
```
Now we're read to merge. the --no-ff will insure the pointer is not fast forwarded recording our merge commit.
```
git merge newstuff --no-ff
git commit -m "include new stuff"
git log --oneline --decorate --graph --all
```
## Squash merge
Repeat the steps in the previous exercise but perform a squash merge and note the differences in history

Create a new branch and add some commits
```
git status
git checkout -b evenmorestuff
echo "#Even more new stuff" > evenmore.md
git add .
git commit -m "even more stuff"
git status
echo "add a line" >> evenmore.md
git commit -am "more and more"
git log --oneline
```
Switch back to main and add a commit
```
git checkout main
git log --oneline
echo "adding even more" >> readme.md
git log --oneline
git branch
git merge --squash evenmorestuff
git commit -am "merge evenmorestuff"
```
Note the merge tree represents the merge of all of the above
