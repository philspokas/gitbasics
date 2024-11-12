# Exploring HEAD and refs


git log --oneline --decorate --graph --all


## Review refs

```
git checkout main
git cat-file -p HEAD
git checkout 
git show-ref
```

## Tagging

Create, list and delete tags with the git tag command

```
git tag
```

You can "go back in time" to inspect a commit and tag it

```
git checkout <commit hash>
git tag -m 'going back in time' 'v0.0.1'
git checkout main
git log
```
