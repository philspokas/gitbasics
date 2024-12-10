# Exploring HEAD and refs

In the following exercise we'll review HEAD and refs. we'll use git log commands. The following command is helpful as it displays each commit on oneline, includes a graph and displays all commits.

```
git log --oneline --decorate --graph --all
```
Creating an alias makes it much easier to use. The following setting creates an alias command "loga" on *newer versions of git (~1.47)*

```
git config set --global alias.loga "log --oneline --decorate --graph --all"    
```
Older versions of git will need to use the --add command as follows:
```
git config --add --global alias.loga "log --oneline --decorate --graph --all"
```
Either way, you should end up with a new command "loga":
```
git loga
```

## Review refs
The cat-file command displays the contents of the HEAD object.

```
git checkout main
git cat-file -p HEAD
```
Here we use cat-file to display the contents of the parent commit given to us in HEAD. Note we can use the first 7 characters of the commit hash. Note your commit hash will be different. Simply copy it from the output of the previous command.
```
git cat-file -p 61842dc8
```
The show-ref to displays references in your repository
```
git show-ref
```

## Tagging

Create, list and delete tags with the git tag command

```
git tag
```

You can "go back in time" to inspect a commit and tag it. First we use the log command to display our commits, then we use an earlier commit and check it out. Finally we tag that commit for future reference.

```
git loga
git checkout <commit hash>
git tag -m 'going back in time' 'v0.0.1'
git checkout main
git loga
git show-ref
```

