# Git

A minimal list of useful Git commands

## Config

### Global

```bash
git config --global user.email "e-mail"
git config --global user.name "first name last name"
```

### Local

```bash
git config user.email "e-mail"
git config user.name "first name last name"
```

### Difference between local and global

- local means only in corresponding repository
- global means general config, for every repository with no local config

## Branches
```bash
git checkout -b <branch>
```
Create a new branch and switch to it

```bash
git switch origin/<branch>
```
You are in Detached HEAD right now<br>
this means git shows you origin/<branch> without creation of a local branch<br>
you can not contribute if you want, this is a read only-view<br>
if you want to contribute you need to use -t switch<br>

```bash
git switch -t origin/<branch>
```
creates a new local branch with the same name as origin/<branch><br>
automatically sets upstream-tracking<br>
use this command if you want to checkout a locally non-existing branch from a remote repo with upstream-tracking<br>

## Sync with remote

```bash
git fetch --all --prune
```
Fetch all remote branches and remove deleted ones (prune = clean up)<br>
only downloads data to your local repository<br>
it doesn’t automatically merge it with any of your work or modify what you’re currently working on<br>
You have to merge it manually into your work when you’re ready

```bash
git pull
```
Get the latest changes from the remote branch

```bash
git commit -m <message>
```
Send local changes to staging area with a message

```bash
git push
```
Send staged local commits to the remote branch, if exists

```bash
git push --set-upstream origin <branch>  
```
after creating locally a new branch, which does not exist on a remote it must be introduced manually<br>
to do so, we manually set the upstream to origin with this command
