# Getting Started

## Installing Git

If you've already installed Git, check the verion as follows:

```
git --version
```

Install or upgrade as needed
See https://git-scm.com/downloads for instructions

## Code Editor

Visual Studio Code will have Git support enabled by default if you have Git installed.

Open Visual Studio Code and verify that Git is installed.

## Configuring Git

Git options and defaults are configured with the ```git config ``` command. Review local, global and system settings. 

<i>Note that the synax of git config changed recently such that the option specifier ```--``` is no longer required in front of the git config command. If you encounter errors when executing the following commands, we recommend upgrading your git version to the latest available for your OS.</i>

```
git config list --local
git config list --global
git config list --system
git config list -–show-origin
```

In order to record your identity in commits, Git will have your name and email to be set. Set your username and email.
Note if you do not specify a location, local will be the default.

Check to see if you username and email are set and if not, set them appropriately.

To set for a specific repo:
```
git config set user.name phil
git config set user.email phil@intellitect.com
```

To set the default for all of my repos:
```
git config set --global user.name phil
git config set --global user.email phil@intellitect.com
```

Set the global default initial branch name:
```
git config set --global init.defaultbranch main
```
* Use git config to verify where the setting was made (git config list --show-origin)

## Getting Help

```
git help
git <command> --help 
git <command> -h
```




