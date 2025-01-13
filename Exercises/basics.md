# Git Basics
These exercises cover the basics inclduing creating a git repo, cloning a repo, pulling remotes and pushing updates


## Clone a repo
Clone the gitbasics repo from BitBucket by navigating to the repo and retrieving the clone URL. Note the URL and use it for clone path. You can optionally specify a different local folder to clone into. The repo name will be used by default.

```
git clone <clone path> <local-name>
```

Use the status command to check the status of your local repo:
```
git status
```


## Remotes

Review the remote using remote command. Use the --verbose (-v) option to return full details
```
git remote --verbose
```

 * Note the name "origin" is the default remote
 * Additional remotes can be added 


## Create a new repo

Create a new folder, add a file, then create a repo and review. Be sure to change directory into a working folder location.

For example ```c:\dev``` or ```$HOME/repos``` or similar.

```
cd <working folder>
mkdir newrepo
cd newrepo
echo "# New Repo" >> readme.md
git init
git status

```

* Note the readme.md is Untracked
* Explore .git folder which may be hidden

