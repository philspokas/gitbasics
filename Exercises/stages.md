# Explore Git File Stages

## Add files to a repo
We created a new repo in a previous exercise, now let's add files and commit them. We add and commit a file, checking status in between steps:

```
git status
git add readme.md
git status
git commit -m "first commit"
git status
```

We now have a commit that can be reviewed with git log. Note the commit and it's hash.
```
git log
```

## Remove files from a repo

Use the local repo to explore removing files using git rm

First create a new file and add it to staging. 

```
echo "get rid of this file" >nope.md
git add .
git rm nope.md

```

* Note that since the file is staged, git rejects the command. Use "-f" to force the removal. 

Once you commit the file, git rm will update Stage to delete the file

```
echo "get rid of this file" >nope.md
git add .
git commmit -m "add file to remove"
git status
git log
git rm nope.md
git status
```

* a final git commit will commit the change and update the log

```
git commit -m "finsh remove"
```

## Restoring files in your repo
Note that git restore is a new command and the preferred method over git reset.

Edit the readme.md and then perform the following to demonstrate reset

```
echo "added to readme " >> readme.md
git add readme.md
git status
git restore --staged readme.md
git status
git restore readme.md 
```




