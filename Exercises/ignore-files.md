# Configuring .gitignore

You can create a .gitignore by hand, or, create one automatically when you initialize a repo in a git service such as BitBucket. When creating a repo, you will be given an option to initialize the repo with a .gitignore for a selected language type

## Create .gitignore manually
In this exercise, create a simple .gitignore that ignores all log files. Then, create some sample log files and note they do not show up as untracked

```
echo "*.log" > .gitignore
echo "test log" > test.log
git status
md logs
cd logs
echo "log 1"  >> 1.log
echo "more logs" >> log2.log
git status
```

## Force an ignored file to be added and committed
The .gitignore can be overriden during the add using the --force option 

```
git add test.log --force

```

## Review generated .gitignore
Review a template .gitignore by creating a new repo in BitBucket. Note that any files that meet the criteria will not be tracked by default.



